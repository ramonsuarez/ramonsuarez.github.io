---
excerpt: ""
author: "@ramonsuarez"
date: 2024-03-22T11:35:35.042Z
status: publish
title: "How to fix Fabric notebook error \"XMLSyntaxError: Start tag expected,
  '<' not found, line 1, \""
tags:
  - Fabric
  - Notebooks
  - XML
  - Errors
  - Pandas
  - Pyspark
  - Databricks
type: post
categories:
  - Data engineering
description: Easy to fix xml weirdness with Pandas, Fabric notebooks and XML
---
T﻿o get around the lack of a native support of XML file import in Fabric, you can use Pandas and then convert it to PySpark to save the dataframe to your Delta table.

Y﻿ou may encounter the error "XMLSyntaxError: Start tag expected, '<' not found, line 1, " and be puzzled about how to fix it. 

I﻿f you get this error with a notebook that you have deployed or imported: 

1. Make sure that you have uploaded the files to import into the new lakehouse. 
2. Check if the Lakehouse for the notebook is the right one (you may still be linked to the lakehouse in the original Workspace)
3. C﻿hange the Lakehouse to the one in the current workspace. 
2. M﻿ake sure that the string of the relative URL of the file you are importing starts with `/lakehouse/default/ `and that it ends with a `/` like this `/lakehouse/default/Files/file.xml/`. If your Lakehouse is somewhere else just make sure that the path starts and ends with a "/". 
