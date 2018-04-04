---
title: "Table.SelectRows | Microsoft Docs"
ms.custom: ""
ms.date: "01/19/2018"
ms.prod: "powerbi"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "mlang"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
ms.assetid: 0631d2e0-3989-4bb4-a70b-1ab9203190b1
caps.latest.revision: 7
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
---
# Table.SelectRows

  
## About  
Returns a table containing only the rows that match a condition.  
  
```  
Table.SelectRows(table as table, condition as function) as table  
```  
  
## Arguments  
  
|Argument|Description|  
|------------|---------------|  
|table|The Table to check.|  
|condition|The condition to match.|  
  
## <a name="__toc360789530"></a>Remarks  
  
-   Table. SelectRows is similar to List. Select but requires a table as input.  
  
## Examples  
  
```  
Table.SelectRows(Table.FromRecords(  
  
{  
  
      [CustomerID = 1, Name = "Bob", Phone = "123-4567"],  
  
      [CustomerID = 2, Name = "Jim", Phone = "987-6543"] ,  
  
      [CustomerID = 3, Name = "Paul", Phone = "543-7890"] ,  
  
      [CustomerID = 4, Name = "Ringo", Phone = "232-1550"]  
  
}  
  
), each [CustomerID] > 2)  
```  
  
|CustomerID|Name|Phone|  
|--------------|--------|---------|  
|3|Paul|543-7890|  
|4|Ringo|232-1550|  
  