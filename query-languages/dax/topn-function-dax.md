---
title: "TOPN Function (DAX) | Microsoft Docs"
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
  - "sql13.as.daxref.TOPN.f1"
helpviewer_keywords: 
  - "TOPN Function (DAX)"
ms.assetid: bded419b-a60f-445a-999e-1360cb7ad610
caps.latest.revision: 5
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
---
# TOPN Function (DAX)
Returns the top N rows of the specified table.  
  
## Syntax  
  
```  
TOPN(<n_value>, <table>, <orderBy_expression>, [<order>[, <orderBy_expression>, [<order>]]…])  
```  
  
#### Parameters  
n_value  
The number of rows to return. It is any DAX expression that returns a single scalar value, where the expression is to be evaluated multiple times (for each row/context).  
  
See the remarks section to understand when the number of rows returned could possible be larger than *n_value*.  
  
See the remarks section to understand when an empty table is returned.  
  
table  
Any DAX expression that returns a table of data from where to extract the top ‘n’ rows.  
  
orderBy_expression  
Any DAX expression where the result value is used to sort the table and it is evaluated for each row of *table*.  
  
order  
(Optional) A value that specifies how to sort *orderBy_expression* values, ascending or descending:  
  
||||  
|-|-|-|  
|**value**|**alternate value**|**Description**|  
|0 (zero)|FALSE|Sorts in descending order of values of *order_by*.<br /><br />This is the default value when *order* parameter is omitted.|  
|1|TRUE|Ranks in ascending order of *order_by*.|  
  
## Return Value  
A table with the top N rows of *table* or an empty table if *n_value* is 0 (zero) or less. Rows are not necessarily sorted in any particular order.  
  
## Remarks  
  
-   If there is a tie, in *order_by* values, at the N-th row of the table, then all tied rows are returned. Then, when there are ties at the N-th row the function might return more than n rows.  
  
-   If n_value is 0 (zero) or less then TOPN returns an empty table.  
  
-   TOPN does not guarantee any sort order for the results.  
  
## Example  
The following sample creates a measure with the sales of the top 10 sold products.  
  
```  
=SUMX(TOPN(10, SUMMARIZE(Product, [ProductKey], “TotalSales”, SUMX(RELATED(InternetSales_USD[SalesAmount_USD]), InternetSales_USD[SalesAmount_USD]) + SUMX(RELATED(ResellerSales_USD[SalesAmount_USD]), ResellerSales_USD[SalesAmount_USD]))  
```  