---
title: "CLOSINGBALANCEQUARTER Function (DAX) | Microsoft Docs"
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
  - "sql13.as.daxref.CLOSINGBALANCEQUARTER.f1"
helpviewer_keywords: 
  - "CLOSINGBALANCEQUARTER function"
ms.assetid: c7928e90-8ecc-4a31-8ab2-b2efa7614aef
caps.latest.revision: 8
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
---
# CLOSINGBALANCEQUARTER Function (DAX)
Evaluates the **expression** at the last date of the quarter in the current context.  
  
## Syntax  
  
```  
CLOSINGBALANCEQUARTER(<expression>,<dates>[,<filter>])  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Definition|  
|**expression**|An expression that returns a scalar value.|  
|**dates**|A column that contains dates.|  
|**filter**|(optional) An expression that specifies a filter to apply to the current context.|  
  
## Return Value  
A scalar value that represents the **expression** evaluated at the last date of the quarter in the current context.  
  
## Remarks  
The **dates** argument can be any of the following:  
  
-   A reference to a date/time column.  
  
-   A table expression that returns a single column of date/time values.  
  
-   A Boolean expression that defines a single-column table of date/time values.  
  
> [!NOTE]  
> Constraints on Boolean expressions are described in the topic, [CALCULATE Function &#40;DAX&#41;](calculate-function-dax.md).  
  
> [!NOTE]  
> The **filter** expression has restrictions described in the topic, [CALCULATE Function &#40;DAX&#41;](calculate-function-dax.md).  
  
This DAX function is not supported for use in DirectQuery mode. For more information about limitations in DirectQuery models, see  [http://go.microsoft.com/fwlink/?LinkId=219172](http://go.microsoft.com/fwlink/?LinkId=219172).  
  
## Example  
The following sample formula creates a measure that calculates the 'Quarter End Inventory Value' of the product inventory.  
  
To see how this works, create a PivotTable and add the fields, CalendarYear, CalendarQuarter and MonthNumberOfYear, to the **Row Labels** area of the PivotTable. Then add a measure, named **Quarter End Inventory Value**, using the formula defined in the code section, to the **Values** area of the PivotTable.  
  
## Code  
  
```  
=CLOSINGBALANCEQUARTER(SUMX(ProductInventory,ProductInventory[UnitCost]*ProductInventory[UnitsBalance]),DateTime[DateKey])  
```  
  
## See Also  
[Time Intelligence Functions &#40;DAX&#41;](time-intelligence-functions-dax.md)  
[CLOSINGBALANCEYEAR Function &#40;DAX&#41;](closingbalanceyear-function-dax.md)  
[CLOSINGBALANCEMONTH Function &#40;DAX&#41;](closingbalancemonth-function-dax.md)  
[Get Sample Data](http://go.microsoft.com/fwlink/?LinkId=164474)  
  