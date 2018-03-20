---
title: "DateTime.FromText | Microsoft Docs"
ms.custom: ""
ms.date: "01/19/2018"
ms.prod: "powerbi"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "mlang"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
ms.assetid: 932b161e-7aa4-4056-9b49-cb35655ac3cf
caps.latest.revision: 6
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
---
# DateTime.FromText

  
## About  
Returns a DateTime value from a set of date formats and culture value.  
  
```  
DateTime.FromText(dateTime as nullable text, optional culture as nullable text) as nullable date  
```  
  
## Arguments  
  
|Argument|Description|  
|------------|---------------|  
|dateTime|The text value to convert.|  
|Culture|A text value corresponding to the culture values supported on your version of Windows, such as "en-US". If the culture is not specified, the current user culture is used. For a list of culture names, see [National Language Support (NLS) API Reference](http://msdn.microsoft.com/en-us/goglobal/bb896001.aspx).|  
  
### DateTime formats  
  
-   YYYY-MM-DDThh:mm  
  
-   YYYYMMDDThh:mm  
  
-   YYYY-MM-DDThh:mm:ss  
  
-   YYYYMMDDThh:mm:ss  
  
-   YYYY-MM-DDThh:mm:ss.nnnnnnn  
  
-   YYYYMMDDThh:mm:ss.nnnnnnn  
  
### Terms  
  
-   Y = years  
  
-   M = months  
  
-   D = days  
  
-   h = hours  
  
-   m = minutes  
  
-   s = seconds  
  
-   n = fractional seconds  
  
## Example  
  
```  
DateTime.FromText("2010-12-31T01:30:00") equals YYYY-MM-DDThh:mm:ss  
```  