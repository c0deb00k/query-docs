---
title: "Text.FromBinary | Microsoft Docs"
ms.custom: ""
ms.date: "01/19/2018"
ms.prod: "powerbi"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "mlang"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
ms.assetid: 110a4629-a63d-4d4c-a966-7ba7a78fb183
caps.latest.revision: 6
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
---
# Text.FromBinary

  
## About  
Decodes data from a binary value in to a text value using an encoding.  
  
```  
Text.FromBinary(binary as nullable binary, optional encoding as nullable number) as nullable text  
```  
  
## Arguments  
  
|Argument|Description|  
|------------|---------------|  
|binary|The value to decode.|  
|optional encoding|Encoding option to apply.|  
  
Text encoding  
  
TextEncoding.Utf8 = 65001;  
  
TextEncoding.Utf16 = 1200;  
  
TextEncoding.Ascii = 20127;  
  
TextEncoding.Unicode = 1200;  
  
TextEncoding.BigEndianUnicode = 1201,  
  
TextEncoding.Windows = 1252;  
  