---
title: "CALENDAR Function (DAX) | Microsoft Docs"
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
ms.assetid: a9666506-d7e5-4441-b48b-379342c595a3
caps.latest.revision: 8
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
---
# CALENDAR Function (DAX)
  
Returns a table with a single column named “Date” that contains a contiguous set of dates. The range of dates is from the specified start date to the specified end date, inclusive of those two dates.  
  
## Syntax  
  
```  
CALENDAR(<start_date>, <end_date>)  
```  
  
#### Parameters  
  
|Term|Definition|  
|--------|--------------|  
|**start_date**|Any DAX expression that returns a datetime value.|  
|**end_date**|Any DAX expression that returns a datetime value.|  
  
## Return Value  
Returns a table with a single column named “Date” containing a contiguous set of dates. The range of dates is from the specified start date to the specified end date, inclusive of those two dates.  
  
## Remarks  
An error is returned if start_date is greater than end_date.  
  
## Examples  
The following formula returns a table with dates between January 1st, 2005 and December 31st, 2015.  
  
`=CALENDAR (DATE (2005, 1, 1), DATE (2015, 12, 31))`  
  
For a data model which includes actual sales data and future sales forecasts. The following expression returns the date table covering the range of dates in these two tables.  
  
`=CALENDAR (MINX (Sales, [Date]), MAXX (Forecast, [Date]))`  
  