---
title: "ENDOFYEAR Function (DAX) | Microsoft Docs"
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
  - "sql13.as.daxref.ENDOFYEAR.f1"
helpviewer_keywords: 
  - "ENDOFYEAR function"
ms.assetid: 2526c88d-8566-4b29-a2b6-bfa327069798
caps.latest.revision: 7
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
---
# ENDOFYEAR Function (DAX)
Returns the last date of the year in the current context for the specified column of dates.  
  
## Syntax  
  
```  
ENDOFYEAR(<dates> [,<year_end_date>])  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Term|Definition|  
|**dates**|A column that contains dates.|  
|**year_end_date**|(optional) A literal string with a date that defines the year-end date. The default is December 31.|  
  
## Return Value  
A table containing a single column and single row with a date value.  
  
## Remarks  
The **dates** argument can be any of the following:  
  
-   A reference to a date/time column,  
  
-   A table expression that returns a single column of date/time values,  
  
-   A Boolean expression that defines a single-column table of date/time values.  
  
> [!NOTE]  
> Constraints on Boolean expressions are described in the topic, [CALCULATE Function &#40;DAX&#41;](calculate-function-dax.md).  
  
The **year_end_date** parameter is a string literal of a date, in the same locale as the locale of the client where the workbook was created. The year portion of the date is ignored.  
  
This DAX function is not supported for use in DirectQuery mode. For more information about limitations in DirectQuery models, see  [http://go.microsoft.com/fwlink/?LinkId=219172](http://go.microsoft.com/fwlink/?LinkId=219172).  
  
## Example  
The following sample formula creates a measure that returns the end of the fiscal year that ends on June 30, for the current context.  
  
To see how this works, create a PivotTable and add the field CalendarYear to the **Row Labels** area of the PivotTable. Then add a measure, named **EndOfFiscalYear**, using the formula defined in the code section, to the **Values** area of the PivotTable.  
  
```  
=ENDOFYEAR(DateTime[DateKey],"06/30/2004")  
```  
  
## See Also  
[Date and Time Functions &#40;DAX&#41;](date-and-time-functions-dax.md)  
[Time Intelligence Functions &#40;DAX&#41;](time-intelligence-functions-dax.md)  
[ENDOFMONTH Function &#40;DAX&#41;](endofmonth-function-dax.md)  
[ENDOFQUARTER Function &#40;DAX&#41;](endofquarter-function-dax.md)  
  