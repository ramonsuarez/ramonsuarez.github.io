---
title: "Fabric notebook error \"XMLSyntaxError: Start tag expected, '<' not
  found, line 1, \""
date: 2024-03-22T11:35:35.042Z
description: Easy to fix xml weirdness with Pandas, Fabric notebooks and XML
---
T﻿o get around the lack of a native support of XML file import in Fabric, you can use Pandas and then convert it to PySpark to save the dataframe to your Delta table.

Y﻿ou may encounter the error "XMLSyntaxError: Start tag expected, '<' not found, line 1, " and be puzzled about how to fix it. 

I﻿f you get this error with a notebook that you have deployed or imported: 

1. C﻿hange the Lakehouse to the one in the current workspace. 
2. M﻿ake sure that the string of the relative URL of the file you are importing starts with ` /lakehouse/default/ `and that it ends with a `/` like this `/lakehouse/default/Files/file.xml/`.