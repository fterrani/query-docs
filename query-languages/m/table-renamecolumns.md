---
title: "Table.RenameColumns | Microsoft Docs"
ms.custom: ""
ms.date: "01/19/2018"
ms.prod: "powerbi"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "mlang"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
ms.assetid: 74b26a6f-d7fa-4ed8-a143-2e0c450b1ebc
caps.latest.revision: 7
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
---
# Table.RenameColumns

  
## About  
Returns a table with the columns renamed as specified.  
  
```  
Table.RenameColumns(table as table, renames as list, optional missingField as nullable number) as table  
```  
  
## Arguments  
  
|Argument|Description|  
|------------|---------------|  
|table|The Table to modify.|  
|renames|The list of values to rename to.|  
|optional missingField|The default value of missingField is **MissingField.Error**. For more information, see Parameter Values.|  
  
## <a name="__toc360789580"></a>Remarks  
  
-   Table.RenameColumns is similar to Record.RenameFields applied to every row in a table.  
  
## Examples  
  
```  
Table.RenameColumns(Table.FromRecords({  
  
    [CustomerNum=1, Name="Bob", Phone = "123-4567"]}),  
  
    {"CustomerNum", "CustomerID"})  
```  
  
|CustomerID|Name|Phone|  
|--------------|--------|---------|  
|1|Bob|123-4567|  
  
```  
Table.RenameColumns(Table.FromRecords({  
  
    [CustomerID=1, Name="Bob", Phone = "123-4567"]}), {"NewCol", "NewColumn"}, MissingField.UseNull)  
```  
  
|CustomerID|Name|Phone|NewColumn|  
|--------------|--------|---------|-------------|  
|1|Bob|123-4567|null|  
  