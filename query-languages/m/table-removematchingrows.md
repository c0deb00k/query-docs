---
title: "Table.RemoveMatchingRows | Microsoft Docs"
ms.custom: ""
ms.date: "01/19/2018"
ms.prod: "powerbi"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "mlang"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
ms.assetid: 1d463a27-1daf-43f6-b2da-37887cc5e8a3
caps.latest.revision: 7
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
---
# Table.RemoveMatchingRows

  
## About  
Removes all occurrences of rows from a table.  
  
```  
Table.RemoveMatchingRows(table as table, rows as list, optional equationCriteria as any) as table  
```  
  
## Arguments  
  
|Argument|Description|  
|------------|---------------|  
|table|The Table to modify.|  
|rows|The List of rows to remove.|  
|optional equationCriteria|An optional value that specifies how to control comparison between the rows of the table.|  
  
## <a name="__toc360789692"></a>Remarks  
Table.RemoveMatchingRows is similar to List.RemoveMatchingItems but requires a table as input.  
  
## Example  
  
```  
Table.RemoveMatchingRows(Table.FromRecords(  
  
{  
  
      [OrderID = 1, CustomerID = 1, Item = "Fishing rod", Price = 100.0],  
  
      [OrderID = 2, CustomerID = 1, Item = "1 lb. worms", Price = 5.0],  
  
      [OrderID = 3, CustomerID = 2, Item = "Fishing net", Price = 25.0],  
  
      [OrderID = 4, CustomerID = 3, Item = "Fish tazer", Price = 200.0],  
  
      [OrderID = 5, CustomerID = 3, Item = "Bandaids", Price = 2.0],  
  
      [OrderID = 6, CustomerID = 1, Item = "Tackle box", Price = 20.0],  
  
      [OrderID = 7, CustomerID = 5, Item = "Bait", Price = 3.25],  
  
      [OrderID = 8, CustomerID = 5, Item = "Fishing Rod", Price = 100.0],  
  
      [OrderID = 9, CustomerID = 6, Item = "Bait", Price = 3.25]  
  
}  
  
), {[CustomerID = 3]}, "CustomerID")  
```  
  
|OrderID|CustomerID|Item|Price|  
|-----------|--------------|--------|---------|  
|1|1|Fishing rod|100|  
|2|1|1 lb. worms|5|  
|3|2|Fishing net|25|  
|6|1|Tackle box|20|  
|7|5|Bait|3.25|  
|8|5|Fishing Rod|100|  
|9|6|Bait|3.25|  
  