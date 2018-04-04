---
title: "DATEVALUE Function (DAX) | Microsoft Docs"
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
  - "sql13.as.daxref.DATEVALUE.f1"
helpviewer_keywords: 
  - "DATEVALUE function"
ms.assetid: 5dc1aeb8-211e-4cb9-84f9-fe42dccbbe06
caps.latest.revision: 4
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
---
# DATEVALUE Function (DAX)
Converts a date in the form of text to a date in datetime format.  
  
## Syntax  
  
```  
DATEVALUE(date_text)  
```  
  
#### Parameters  
  
|Term|Definition|  
|--------|--------------|  
|**date_text**|Text that represents a date.|  
  
## Property Value/Return Value  
A date in **datetime** format.  
  
## Remarks  
The DATEVALUE function uses the locale and date/time settings of the client computer to understand the text value when performing the conversion. If the current date/time settings represent dates in the format of Month/Day/Year, then the string, "1/8/2009", would be converted to a **datetime** value equivalent to January 8th of 2009. However, if the current date and time settings represent dates in the format of Day/Month/Year, the same string would be converted as a **datetime** value equivalent to August 1st of 2009.  
  
If the year portion of the **date_text** argument is omitted, the DATEVALUE function uses the current year from your computer's built-in clock. Time information in the **date_text** argument is ignored.  
  
## Example  
The following example returns a different **datetime** value depending on your computer's locale and settings for how dates and times are presented.  
  
-   In date/time settings where the day precedes the month, the example returns a **datetime** value corresponding to January 8th of 2009.  
  
-   In date/time settings where the month precedes the day, the example returns a **datetime** value corresponding to August 1st of 2009.  
  
```  
=DATEVALUE("8/1/2009")  
```  
  
## See Also  
[Date and Time Functions &#40;DAX&#41;](date-and-time-functions-dax.md)  
  