---
title: "CROSSJOIN  Function (DAX) | Microsoft Docs"
ms.custom: ""
ms.date: "12/28/2017"
ms.prod: "powerbi"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "analysis-services"
  - "daxlang"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
f1_keywords: 
  - "sql13.as.daxref.CROSSJOIN.f1"
helpviewer_keywords: 
  - "CROSSJOIN Function (DAX)"
ms.assetid: 655ce02d-cfdb-4a22-923a-34c78fd1759b
caps.latest.revision: 6
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
---
# CROSSJOIN  Function (DAX)
Returns a table that contains the Cartesian product of all rows from all tables in the arguments. The columns in the new table are all the columns in all the argument tables.  
  
## Syntax  
  
```  
CROSSJOIN(<table>, <table>[, <table>]…)  
```  
  
#### Parameters  
table  
Any DAX expression that returns a table of data  
  
## Return Value  
A table that contains the Cartesian product of all rows from all tables in the arguments.  
  
## Remarks  
  
-   Column names from *table* arguments must all be different in all tables or an error is returned.  
  
-   The total number of rows returned by CROSSJOIN() is equal to the product of the number of rows from all tables in the arguments; also, the total number of columns in the result table is the sum of the number of columns in all tables. For example, if **TableA** has **rA** rows and **cA** columns, and **TableB** has **rB** rows and **cB** columns, and **TableC** has **rC** rows and **cC** column; then, the resulting table has **rA × rb × rC** rows and **cA + cB + cC** columns.  
  
## Example  
The following example shows the results of applying CROSSJOIN() to two tables: **Colors** and **Stationery**.  
  
The table **Colors** contains colors and patterns:  
  
|Color|Pattern|  
|---------|-----------|  
|Red|Horizontal Stripe|  
|Green|Vertical Stripe|  
|Blue|Crosshatch|  
  
The table **Stationery** contains fonts and presentation:  
  
|Font|Presentation|  
|--------|----------------|  
|serif|embossed|  
|sans-serif|engraved|  
  
The expression to generate the cross join is presented below:  
  
```  
CROSSJOIN( Colors, Stationery)  
```  
When the above expression is used wherever a table expression is expected, the results of the expression would be as follows:  
  
|Color|Pattern|Font|Presentation|  
|---------|-----------|---------|-----------|  
|Red|Horizontal Stripe|serif|embossed|  
|Green|Vertical Stripe|serif|embossed|  
|Blue|Crosshatch|serif|embossed|  
|Red|Horizontal Stripe|sans-serif|engraved|  
|Green|Vertical Stripe|sans-serif|engraved|  
|Blue|Crosshatch|sans-serif|engraved|  
  