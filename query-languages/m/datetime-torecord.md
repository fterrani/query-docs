---
title: "DateTime.ToRecord | Microsoft Docs"
ms.custom: ""
ms.date: "01/19/2018"
ms.prod: "powerbi"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "mlang"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
ms.assetid: 5134253e-f607-42c5-a53e-213702337e00
caps.latest.revision: 5
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
---
# DateTime.ToRecord

  
## About  
Returns a record containing parts of a DateTime value.  
  
```  
DateTime.ToRecord(dateTime as datetime) as record  
```  
  
## Arguments  
  
|Argument|Description|  
|------------|---------------|  
|dateTime|The DateTime to parse.|  
  
## Example  
  
```  
DateTime.ToRecord(#datetime(2013,1,3,12,4,5)) equals  
[             
Year = 2013,   Month = 1,   Day = 3,         
Hour = 12,  Minute = 4, Second = 5  
]  
```  