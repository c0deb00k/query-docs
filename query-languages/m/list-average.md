---
title: "List.Average | Microsoft Docs"
ms.custom: ""
ms.date: "01/19/2018"
ms.prod: "powerbi"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "mlang"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
ms.assetid: 04adad51-5731-481a-b022-79b7abb2ccc9
caps.latest.revision: 5
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
---
# List.Average

  
## About  
Returns an average value from a list in the datatype of the values in the list.  
  
```  
List.Average(list as list) as any  
```  
  
## Arguments  
  
|Argument|Description|  
|------------|---------------|  
|list|The List to check.|  
  
## <a name="__toc360789372"></a>Remarks  
  
-   If the list is empty, an Expression.Error is thrown.  
  
## Examples  
  
```  
List.Average({1, 2, 3}) equals 2  
```  
  
```  
List.Average({#duration(0, 0, 30, 0), #duration(0, 0, 40, 0)}) equals #duration(0, 0, 35, 0)  
```  
  
```  
List.Average({#date(2011,1,1), #date(2011,1,2), #date(2011,1,3)})  equals #datetime(2011,1,2)  
```  
  
```  
List.Average({}) equals null  
```  