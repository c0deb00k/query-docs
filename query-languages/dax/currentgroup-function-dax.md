---
title: "CURRENTGROUP function (DAX) | Microsoft Docs"
ms.service: powerbi 
ms.date: 09/09/2020
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend

---
# CURRENTGROUP

Returns a set of rows from the table argument of a [GROUPBY](groupby-function-dax.md) expression that belong to the current row of the [GROUPBY](groupby-function-dax.md) result.

## Syntax  
  
```dax
CURRENTGROUP ( )
```
  
### Parameters  
  
None
  
## Return value

The rows in the table argument of the [GROUPBY](groupby-function-dax.md) function corresponding to one group of values of the groupBy_columnName arguments.

## Remarks

- This function can only be used within a [GROUPBY](groupby-function-dax.md) expression.

- This function takes no arguments and is only supported as the first argument to one of the following aggregation functions: [AVERAGEX](averagex-function-dax.md), [COUNTAX](countax-function-dax.md), [COUNTX](countx-function-dax.md), [GEOMEANX](geomeanx-function-dax.md), [MAXX](maxx-function-dax.md), [MINX](minx-function-dax.md), [PRODUCTX](productx-function-dax.md), [STDEVX.S](stdevx-s-function-dax.md), [STDEVX.P](stdevx-s-function-dax.md), [SUMX](sumx-function-dax.md), [VARX.S](varx-s-function-dax.md), [VARX.P](varx-p-function-dax.md).
  
## Example

See [GROUPBY](groupby-function-dax.md).