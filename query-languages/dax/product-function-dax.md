---
title: "PRODUCT Function (DAX) | Microsoft Docs"
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
ms.assetid: 4e3f6062-c612-4efb-af81-d6666d853720
caps.latest.revision: 5
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
---
# PRODUCT Function (DAX)
  
Returns the product of the numbers in a column.  
  
To return the product of an expression evaluated for each row in a table, use [PRODUCTX Function &#40;DAX&#41;](productx-function-dax.md).  
  
## Syntax  
  
```  
PRODUCT(<column>)  
```  
  
#### Parameters  
  
|Term|Definition|  
|--------|--------------|  
|column|The column that contains the numbers for which the product is to be computed.|  
  
## Return Value  
A decimal number.  
  
## Remarks  
Only the numbers in the column are counted. Blanks, logical values, and text are ignored.  
  
PRODUCT( Table[Column] ) is equivalent to PRODUCTX( Table, Table[Column] )  
  
## Example  
The following computes the product of the AdjustedRates column in an Annuity table:  
  
```  
=PRODUCT( Annuity[AdjustedRates] )  
```  
  
## See Also  
[PRODUCTX Function &#40;DAX&#41;](productx-function-dax.md)  
  