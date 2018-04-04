---
title: "FLOOR Function (DAX) | Microsoft Docs"
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
  - "sql13.as.daxref.FLOOR.f1"
helpviewer_keywords: 
  - "FLOOR function"
ms.assetid: b4d0ee09-eca5-4c6d-a1f1-f41cd93faab4
caps.latest.revision: 4
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
---
# FLOOR Function (DAX)
Rounds a number down, toward zero, to the nearest multiple of significance.  
  
## Syntax  
  
```  
FLOOR(<number>, <significance>)  
```  
  
#### Parameters  
  
|Term|Definition|  
|--------|--------------|  
|**number**|The numeric value you want to round.|  
|**significance**|The multiple to which you want to round. The arguments**number** and **significance** must either both be positive, or both be negative.|  
  
## Return Value  
A decimal number.  
  
## Remarks  
If either argument is nonnumeric, FLOOR returns **#VALUE!**error value.  
  
If number and significance have different signs, FLOOR returns the **#NUM!**error value.  
  
Regardless of the sign of the number, a value is rounded down when adjusted away from zero. If the number is an exact multiple of significance, no rounding occurs.  
  
## Example  
The following formula takes the values in the [Total Product Cost] column from the table, InternetSales.and rounds down to the nearest multiple of .1.  
  
```  
=FLOOR(InternetSales[Total Product Cost],.5)  
```  
The following table shows the expected results for some sample values.  
  
|Values|Expected Result|  
|----------|-------------------|  
|10.8423|10.8|  
|8.0373|8|  
|2.9733|2.9|  
  
## See Also  
[Math and Trig Functions &#40;DAX&#41;](math-and-trig-functions-dax.md)  
  