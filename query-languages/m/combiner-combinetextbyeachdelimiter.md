---
title: "Combiner.CombineTextByEachDelimiter | Microsoft Docs"
ms.custom: ""
ms.date: "01/19/2018"
ms.prod: "powerbi"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "mlang"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
ms.assetid: 9d54afc5-dacb-4dda-951a-d630217b406e
caps.latest.revision: 6
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
---
# Combiner.CombineTextByEachDelimiter

  
## About  
Returns a function that combines a list of text into a single text using each specified delimiter in sequence.  
  
```  
Combiner.CombineTextByEachDelimiter(delimiters as list, optional quoteStyle as number) as function  
```  
  
## Arguments  
  
|Argument|Description|  
|------------|---------------|  
|delimiters|The delimiter characters are used to identify at what points to split the string.  The delimiter character is not included in the split values.  A trailing delimiter character will yield an additional empty text value.  The split values contain all characters between the delimiters.  This function will always produce at least one value.|  
|optional quoteStyle|Determines whether there is quoting within the value that should be used to preserve line breaks and for which delimiters are not significant.|  
  
## <a name="__toc360789938"></a>Remarks  
  
-   Combiner.CombineTextByEachDelimiter is similar to CombineTextByDelimiter except that each delimiter is used in turn.  
  
-   An error is thrown by the resulting function if the cardinality of the line passed to it exceeds the cardinality of the delimiters.  
  