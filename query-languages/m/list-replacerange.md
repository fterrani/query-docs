---
title: "List.ReplaceRange | Microsoft Docs"
ms.custom: ""
ms.date: "01/19/2018"
ms.prod: "powerbi"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "mlang"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
ms.assetid: d0477261-7dda-4668-a125-2b3409cd9d70
caps.latest.revision: 5
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
---
# List.ReplaceRange

  
## About  
Returns a list that replaces count values in a list with a replaceWith list starting at an index.  
  
```  
List.ReplaceRange(list as list,  index as number,  count as number,  replaceWith as list) as list  
```  
  
## Arguments  
  
|Argument|Description|  
|------------|---------------|  
|list|The List to modify.|  
|index|The index to start at.|  
|count|The number of values to replace.|  
|replaceWith|The value to replace with.|  
  
## Example  
  
```  
List.ReplaceRange({1, 2, 7, 8, 9, 5}, 2, 3, {3, 4}) equals {1, 2, 3, 4, 5}  
```  