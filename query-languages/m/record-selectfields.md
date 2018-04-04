---
title: "Record.SelectFields | Microsoft Docs"
ms.custom: ""
ms.date: "01/19/2018"
ms.prod: "powerbi"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "mlang"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
ms.assetid: 070f9273-f10f-4e7a-9d5c-87ac82a3df7c
caps.latest.revision: 6
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
---
# Record.SelectFields

  
## About  
Returns a new record that contains the fields selected from the input record. The original order of the fields is maintained.  
  
```  
Record.SelectFields(record as record,  fields as any,  optional missingField as nullable number) as record  
```  
  
## Arguments  
  
|Argument|Description|  
|------------|---------------|  
|record|The record to check.|  
|fields|A single field name or list of field names.|  
|optional missingField|A **MissingField** enum value to handle missing fields. The default value is MissingField.Error.|  
  
### MissingField enum  
  
-   MissingField.Error = 0;  
  
-   MissingField.Ignore = 1;  
  
-   MissingField.UseNull = 2;  
  
## Remarks  
  
-   The original order of the fields is maintained.  
  
## Examples  
  
```  
Record.SelectFields([A=1, B=2], "B") equals [B=2]  
```  
  
```  
Record.SelectFields([A=1, B=2, C=3], {"C", "B"}) equals [B=2, C=3]  
```  