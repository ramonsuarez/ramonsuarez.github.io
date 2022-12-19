		---
title: "Walmart Sales Analysis: Trends and Seasonality"
date: 2022-12-19T14:07:01+01:00
author: "Ramon Suarez"
categories: [portfolio]
tags: []
draft: true
type: post
---

As part of my [Data Analytics and Visualization course](https://dorifor.be/formation/9277) I decide to do my final project on a [Walmart Dataset found on Kaggle](https://www.kaggle.com/competitions/walmart-recruiting-store-sales-forecasting/data). 

![Kaggle at Walmart](../images/kaggle-walmart.jpg)
Finding a dataset was not easy, and I went through a lot of pages looking for an interesting dataset that would: 
- Include time series
- Be about a business

At the end it came down to two dataset, but the [French bakery](https://www.kaggle.com/datasets/matthieugimbert/french-bakery-daily-sales) lost because I thought it would be more interesting to have data from multiple stores and different locations. 

## Why I choose the Walmart dataset
Choose Walmart stores dataset: 
- Business. 
- Time series (2010-02-05 to 2012-11-01):
    - Seasonality?
    - Holiday impact? 
    - Impact of promos?
~~- Geographic data.~~ 
- Extra: 
    - Weather influence. 
    - Impact of unemployment profiles. 

## About Walmart
Launched by Sam Walton in 1962
10,586 stores
24 countries
$570 billion annual revenue
2.2 million employees
10,586 stores and clubs 
24 countries
$570 billion in annual revenue (65% USA)
Largest employer in the world: 2.2 million employees
Walton family controls over 50% of Walmart
### Stores
USA store brands: 
- Walmart
- Sam's Club

USA divisions: 
- Supercenters
- Discount Stores
- Neighborhood markets

## Data
45 USA stores
3 types of store
400K+ rows
Feb 5 2010 to Nov 1 2012*
\* Markdown data is only available after Nov 2011, and is not available for all stores all the time

## Source Data
1. Downloaded from [Kaggle](https://www.kaggle.com/competitions/walmart-recruiting-store-sales-forecasting/data). 
2. 4 useful CSV files: 
    - features.csv
    - stores.csv
    - test.csv
    - train.csv
3. Info Train & Test (SALES): 
    - Store - the store number
    - Dept - the department number
    - Date - the week
    - **Weekly**\_Sales -  sales for the given department in the given store
    - IsHoliday - whether the week is a special holiday week
    - Test does not have sales data, so I ignore it. 
    - Sales go from Feb 05 2010 to October 26 2012. 
      ![images/20221212160037.png](../images/20221212160037.png)
4. Info Features:
    - Store - the store number
    - Date - the week
    - Temperature - average temperature in the region
    - Fuel_Price - cost of fuel in the region
    - MarkDown1-5 - anonymized data related to promotional markdowns that Walmart is running. MarkDown data is only available after Nov 2011, and is not available for all stores all the time. Any missing value is marked with an NA.
    - CPI - the consumer price index
    - Unemployment - the unemployment rate
    - IsHoliday - whether the week is a special holiday week:
	    - Super Bowl: 12-Feb-10, 11-Feb-11, 10-Feb-12, 8-Feb-13  
	    - Labor Day: 10-Sep-10, 9-Sep-11, 7-Sep-12, 6-Sep-13  
	    - Thanksgiving: 26-Nov-10, 25-Nov-11, 23-Nov-12, 29-Nov-13  
	    - Christmas: 31-Dec-10, 30-Dec-11, 28-Dec-12, 27-Dec-13

## Initial import and wrangling
### Assumptions
* The resulting SQL DB will emulate a production DB, so the import of the original files will only have to be made once. 
* Stores is the main table, the others connect via it. 
* Negative sales mean that there have been more returns than sales.
* Store size is in square feet
* Temperature is in degrees Farenheit.
* Money is US$
* Long numbers in Unemployment ant CPI are decimal numbers missing the separator. 
* US formatting of dates and numbers. 
* Department numbers refere to the[ same department across all stores](https://www.kaggle.com/competitions/walmart-recruiting-store-sales-forecasting/discussion/7159#39217).
### Things to take into consideration
> [**anonymized data**](https://www.kaggle.com/competitions/walmart-recruiting-store-sales-forecasting/discussion/7631#41591) related to promotional markdowns that Walmart is running. MarkDown data is only available after Nov 2011, and is not available for all stores all the time.

- 
### ``cat`` csv files
Did not work because the headers get added and that breaks the import. It is better anyway to import directly with SSIS to be able to reproduce and automate. 
 ~~Union of ``test.csv`` and ``train.csv`` into ``all-sales.csv`` using ``cat`` in a Git Bash terminal on VSCode.~~ 
### Preview CSV files
Explored CSV files with Libre Office to get a feel for the data, check data types, look for inconsistencies, and find keys to link them. 
	- sampleSubmissio.csv: 
		- Discarded, not useful data, zero sales. 
	- stores.csv (headers + 45 lines):
		- Store: Int 🔑.
		- Type: Category or String.
		- Size: Int.
	- all-sales.csv (headers + 536_635 lines): 
		- Store: Int 🔑.
		- Dept: Int.
		- Date: Date 🔑.
		- Weekly Sales: $. 
		- Is Holiday: Boolean 🔑.
	- features.csv (headers + 8190 lines): 
		- Store: Int 🔑.
		- Date: Date 🔑.
		- Temperature: Decimal. 
		- Fuel Price: ⚠️ Pricing not uniform, mix of Int and Dec as string. 
		- Markdown 1 to 5: Decimal, lots of NA. 
		- CPI: Float.
		- Unemployment: not uniform, mix of Int and Dec as string.
		- Is Holiday: Boolean 🔑.
### Create DB
Created database ``Walmart`` with SSMS. 
### Create SSIS project
Create SSIS project ``Walmart Source Data`` to import data. 
### Import CSV files
#### Stores
Import stores table and check that the same number of rows is present: 
```sql
CREATE TABLE [Stores] (
    [Store] smallint IDENTITY(1,1),
    [Type] varchar(1),
    [Size] int
)
```
![images/20221206114256.png](../images/20221206114256.png)
#### Sales
Only imported the ``train.csv`` dataset because the ``test.csv`` dataset did not have any sales data (the column does not exists). I guess this was part of the ML challenge. 

Create table on SSMS:
```sql
USE Walmart
GO

CREATE TABLE Sales(
	Store smallint not null, 
	Dept smallint, 
	[Date] datetime, 
	isHoliday bit,
	weeklySales DEC
)
````
Dates have been converted to DateTime. 

Import through SSIS. 
![images/20221209111146.png](../images/20221206114256.png)
#### Features
Import the columns that SSIS has trouble with (Markdown, Unemployment, CPI) as string, clean up and then convert to ``flottant [DT_R4]``. 
##### NA to NULL
Pay attention to the original text, it was not NaN. 
```sql
MarkDown1 == "NA" ? NULL(DT_I4) : (DT_I4)MarkDown1
MarkDown2 == "NA" ? NULL(DT_I4) : (DT_I4)MarkDown2
MarkDown3 == "NA" ? NULL(DT_I4) : (DT_I4)MarkDown3
MarkDown4 == "NA" ? NULL(DT_I4) : (DT_I4)MarkDown4
MarkDown5 == "NA" ? NULL(DT_I4) : (DT_I4)MarkDown5
CPI == "NA" ? NULL(DT_I4) : (DT_I4)CPI
Unemployment == "NA" ? NULL(DT_I4) : (DT_I4)Unemployment
```

![images/20221206145951.png](../images/20221206114256.png)

![images/20221206141007.png](../images/20221206141007.png)

### . to , 
I did not manage to make the derived column to work, so I changed it with a search replace on LibreOffice. 
### Left over "
Made new connection manager to take care of some left over ".
![images/20221207085121.png](../images/20221207085121.png)

It was causing the error with the ``NA to NULL`` task. 
### Set Keys
Cannot do it via de interface because Null values are allowed on Stores: 
![images/20221207090427.png](../images/20221207090427.png)
So I remove the allow nulls in all columns of the table via SSMS: 
![images/20221207091350.png](../images/20221207091350.png)
And I set ``Store`` as the Primary Key (PK) in ``Stores`` and as Foreign Key (FK) in the others: 
![images/20221207092001.png](../images/20221207092001.png)
All tables are saved without errors. 

## Data Warehouse (DW)
### Dimensional Model
![images/20221207155826.png](../images/20221207155826.png)
### Create DW DB
Create ``Walmart_DW`` via the SSMS interface. 
### Create SSIS project
Create SSIS project in Visual Studio and immediately change the Run64BitRuntime to false. 
![images/20221207092447.png](../images/20221207092447.png)
### Create DimDate from script
Populate DimDate from script we got in class. 
Script fails because the table ``[dbo].[dimdate]`` does not exist. 
So I saved a `Create` script from one of the exercises to recreate the table and then run the script to populate it. 
### Check if holidays match
[[holiday-check.sql]] exploration shows that not a single one matches (tested for 2010): 

**Walmart operational DB**
> Date	IsHoliday
> 2010-02-12 00:00:00.000	1
> 2010-09-10 00:00:00.000	1
> 2010-11-26 00:00:00.000	1
> 2010-12-31 00:00:00.000	1

**Walmart DW dimensional DB**
> Date	IsHolidayUSA
> 2010-01-01 00:00:00.000	1
> 2010-02-14 00:00:00.000	1
> 2010-03-17 00:00:00.000	1
> 2010-07-04 00:00:00.000	1
> 2010-10-31 00:00:00.000	1
> 2010-12-25 00:00:00.000	1

Focus on dates provided in Kaggle's description and keep the other ones to run extra analysis if there's any time left. 

### Create DimStore
Via SSMS. 
```sql
USE Walmart_DW
GO

CREATE TABLE DimStore(
	SkStore INT PRIMARY KEY,
	BkStore INT NOT NULL, 
	[Type] VARCHAR(1) NOT NULL,
	Size INT NOT NULL,
)
```

### Populate DimStore
Derived column is used to create the BKStore column

![images/20221209100420.png](../images/20221209100420.png)
### Create DimDepartment
Via SSMS.
```sql
USE Walmart_DW
GO

CREATE TABLE DimDepartment(
	SKDepartment smallint,
	BKDepartment smallint
)
```
### Populate DimDepartment
SSIS. 
![images/20221209101242.png](../images/20221209101242.png)

### Create FactSales
On SSMS. 
```sql
USE Walmart_DW
GO

CREATE TABLE FactSales(
	FKStore smallint,
	FKDepartment smallint,
	FKDateKey int not null,
	WeeklySales decimal(18,0),
	MarkdownSum float,
	isHoliday bit,
	Temperature real,
	FuelPrice real,
	CPI varchar(50),
	Unemployment varchar(50),
)
```
### Populate FactSales
The Markdown data is not understandable, so I've decided to create a column that adds up all the markdowns and keeps null if there are none. 
Not working Derived column transformations: 
```sql
/* Says that OR cannot be used   */
ISNULL(MarkDown1_DT_R4) ==  FALSE | ISNULL(MarkDown2_DT_R4) ==  FALSE | ISNULL(MarkDown3_DT_R4) ==  FALSE | ISNULL(MarkDown4_DT_R4) ==  FALSE | ISNULL(MarkDown5_DT_R4) ==  FALSE ? 1 : 0

/* No error but it goes into a loop and does not finish loading */
ISNULL(MarkDown1_DT_R4 + MarkDown2_DT_R4 + MarkDown3_DT_R4 + MarkDown4_DT_R4 + MarkDown5_DT_R4) ? 1 : 0
```

Workaround: used SQL request with Source OLE DB component to create a column with the sum of all markdowns (5 * null = null): 
```sql
SELECT *, (MarkDown1_DT_R4 + MarkDown2_DT_R4 + MarkDown3_DT_R4 + MarkDown4_DT_R4 + MarkDown5_DT_R4) AS MS
FROM Features
````

Visual Studio did not execute it: no error but goes on forever, does not even show the data viewer with a union. It ended up being the orphan Sales OLE DB source and that somehow the debugging 64bits option was reset to true. 

Final SSIS flow: 

![images/20221212093416.png](../images/20221209101242.png)
![images/20221212093635.png](../images/20221209101242.png)

### Add fictional dwarf store names
#### Generate names

Used ChatGPT to generate the names of towns: 
```list
1.  Ironforge
2.  Hammerfall
3.  Silvermoon
4.  Khaz Modan
5.  Mount Ironbeard
6.  Iron Summit
7.  Ironforge Heights
8.  Ironwood
9.  Forgefire
10.  Ironhall
11.  Ironhold
12.  Ironfort
13.  Ironpass
14.  Ironpeak
15.  Ironbridge
16.  Ironroot
17.  Ironfist
18.  Ironmoor
19.  Ironmoore
20.  Ironcliff
21.  Ironhearth
22.  Ironhaven
23.  Ironholt
24.  Ironwall
25.  Ironward
26.  Ironstone
27.  Ironmount
28.  Ironpeak
29.  Ironwood
30.  Ironwell
31.  Ironbark
32.  Ironfurrow
33.  Ironhollow
34.  Ironholdfast
35.  Ironbrow
36.  Ironbeard
37.  Ironforge Point
38.  Ironforge Vale
39.  Ironforge Ridge
40.  Ironforge Pass
41.  Ironforge Canyon
42.  Ironforge Creek
43.  Ironforge Lake
44.  Ironforge River
45.  Ironforge Stream
46.  Ironforge Valley
47.  Ironforge Heights
48.  Ironforge Meadows
49.  Ironforge Woods
50.  Ironforge Forest
```
Too much "Iron"

Used an online generator: 
```list
Atallvǫllr

Dagsmejam

Skadi Pass

Vættfanggur

Runehold

Essemjöll

Jǫkullheim

Heillfell

Thornför

Kerlinghelm

Espenfell

Fjallborgg
Félagi Mountain

Jǫtunnbjorg

Apalholm

Vondarahm

Bhildaral

Dhamdorallur

Snærósgar

Dagsmejan

Eyrrlundr

Bhurtarihr

Frodemount

Nindun
Hárför

Izazdun

Terrandel

Jagafell

Nindun

Skadi Pass

Karizaz

Kvennaharr

Anganför

Kerlinghelm

Atallvǫllr

Falgrkelle
Hyllihelm

Banborad

Dvallinstanda

Happholt

Draugrskáli

Nysnögata

Thornför

Efjaheim

Mig Boldor

Harrhǫrgr

Kvennaholl

Skaregar
```
45 names stored in `xls` file with an ID column to use for the join. 
#### Add column to DimStores
```sql
USE [Walmart_DW]
GO

ALTER TABLE DimStore
	ADD StoreName nvarchar(25)
GO
```

#### Import dwarven names
I have encountered a lot of problems with SSIS and SSMS. I've decided to add the Store and Type names to the original sources tables to see if I can import them at the same time as I redo the Dimensions. 

First I truncate DimStore and make sure that all the columns needed are there.

![images/20221212133858.png](../images/20221212133858.png)

![images/20221212134038.png](../images/20221212134038.png)

## Reporting
Connect PowerBI to `DESKTOP-BRU3ORB\DATAVIZ` and import all of `Walmart_DW` tables.
### Check tables
All OK. Only had to change data types for DimDepartment from float to int. No errors on any table. 
![images/20221212135741.png](../images/20221212135741.png)
![images/20221212135803.png](../images/20221212135803.png)
![images/20221212135818.png](../images/20221212135818.png)
![images/20221212135845.png](../images/20221212135845.png)
### Link tables in the model

Because the DimDepartment link required a many to many relationship and it is not needed, I removed it from the data. I also renamed and deleted some columns, including the Type Name that I had incorrectly tagged (it is not a department). 
OLD: 
![images/20221212143416.png](../images/20221212143416.png)
NEW: 
![images/20221212144127.png](../images/20221212144127.png)

### Are Store types linked to size? 
A and B seem to follow a size pattern, but a few of both share size with group C stores: 
![images/20221212150010.png](../images/20221212150010.png)

* Are C stores a new type of store? 
* Are the outliers errors in the data? 
* C Stores do make less money, but so do a couple of type A and a few of type B
   ![images/20221212150228.png](../images/20221212150228.png)
* Type C stores use less markdowns
  ![images/20221212150449.png](../images/20221212150449.png)
* **The type reflects the sales of the stores**: 
![images/20221212152503.png](../images/20221212152503.png)
![images/20221212152620.png](../images/20221212152620.png)


### Fix problems with CPI, Unemployment, Temperature
There are numbers in % and others are included without being divided by 100 and also without ".", so I created new conditional columns to clean up. 
```dax
= Table.AddColumn(#"Colonnes permutées1", "Unemployment", each if [Unemployment_to_fix] > 9999 then [Unemployment_to_fix]/10000 else if [Unemployment_to_fix] > 999 then [Unemployment_to_fix]/1000 else [Unemployment_to_fix])

= Table.AddColumn(#"Colonnes renommées3", "CPI", each if [CPI_to_fix] > 1000 then [CPI_to_fix]/1000 else if [CPI_to_fix] > 100 then [CPI_to_fix]/100 else [CPI_to_fix])
```
#### Add Friday Week
Added a column with the number of the week in that year starting on Saturday and ending on Friday  (the day of the sales report) with an SQL query on Sales & Features, to be able to link weeks with IsHoliday to WeeklySales.  
![images/20221215135819.png](../images/20221215135819.png)

> [! Attention] When updating a table, go to the editor and click on Refresh view (actualiser l'apperçu)
> ![images/20221215140500.png](../images/20221215140500.png)


## Issues
### LocaleID not installed
 Issue: *LocaleID 9 is not installed on this system*
![images/20221206105949.png](../images/20221206105949.png)
	    Due to locale chosen for import (English instead of default French Belgium). Fixed recreating with the local locale and deleting previous connection managers: 
![images/20221206110827.png](../images/20221206110827.png) 
![images/20221206111107.png](../images/20221206111107.png)
### IF Exists does not work as in SSMS
Discarded code for the time being. 
### DB creation and population in same Data Flow
![images/20221206130735.png](../images/20221206130735.png)
First run creates the table with our script and sometimes it is populated, others it needs a second run without changing anything to populate. The script to create the DB is no longer present, the connection is made. 

### Data Viewer not displayed. 
Change Project>Properties>Config>Debugging>Run64bitRuntime to False. 

### . to , not working
Done manually with LibreOffice
### Temperature conversion

> Import Features with some columns as strings to deal with NaN 36 Error: Échec de la conversion de données. La conversion de données de la colonne « Temperature » a retourné la valeur d'état 2 et le texte d'état « La valeur n'a pas pu être convertie en raison d'une perte potentielle de données. ».