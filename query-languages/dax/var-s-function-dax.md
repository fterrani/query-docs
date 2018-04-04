---
title: "VAR.S Function (DAX) | Microsoft Docs"
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
  - "sql13.as.daxref.VAR.S.f1"
helpviewer_keywords: 
  - "VAR.S Function (DAX)"
ms.assetid: 0f96022f-a657-4808-9665-92221c42ed40
caps.latest.revision: 7
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
---
# VAR.S Function (DAX)
Returns the variance of a sample population.  
  
## Syntax  
  
```  
VAR.S(<columnName>)  
```  
  
#### Parameters  
columnName  
The name of an existing column using standard DAX syntax, usually fully qualified. It cannot be an expression.  
  
## Return Value  
A number with the variance of a sample population.  
  
## Exceptions  
  
## Remarks  
  
1.  VAR.S assumes that the column refers to a sample of the population. If your data represents the entire population, then compute the variance by using VAR.P.  
  
2.  VAR.S uses the following formula:  
  
    ∑(x - x̃)²/(n-1)  
  
    where x̃ is the average value of x for the sample population  
  
    and n is the population size  
  
3.  Blank rows are filtered out from *columnName* and not considered in the calculations.  
  
4.  An error is returned if *columnName* contains less than 2 non-blank rows.  
  
This DAX function may return different results when used in a model that is deployed and then queried in DirectQuery mode. For more information about semantic differences in DirectQuery mode, see  [http://go.microsoft.com/fwlink/?LinkId=219171](http://go.microsoft.com/fwlink/?LinkId=219171).  
  
## Example  
The following example shows the formula for a measure that calculates the variance of the SalesAmount_USD column from the InternetSales_USD for a sample population.  
  
```  
=VAR.S(InternetSales_USD[SalesAmount_USD])  
```  