---
title: CREATE PROCEDURE-Anweisung (Microsoft Access SQL)
TOCTitle: CREATE PROCEDURE statement (Microsoft Access SQL)
ms:assetid: 1fbb5267-9862-bfb4-6436-176152d7a6cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845861(v=office.15)
ms:contentKeyID: 48543649
ms.date: 10/18/2018
mtps_version: v=office.15
dev_langs:
- sql
ms.localizationpriority: high
ms.openlocfilehash: b54d85a655bcb6ef60560583e8cbe1e2852c603e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569216"
---
# <a name="create-procedure-statement-microsoft-access-sql"></a>CREATE PROCEDURE-Anweisung (Microsoft Access SQL)

**Gilt für**: Access 2013, Office 2013 

Erstellt eine gespeicherte Prozedur.

> [!NOTE]
> Vom Microsoft Access-Datenbankmodul wird die Verwendung der CREATE PROCEDURE- oder anderer DDL-Anweisungen in Datenbanken, die nicht aus dem Microsoft Jet-Datenbankmodul stammen, nicht unterstützt.

## <a name="syntax"></a>Syntax

CREATE PROCEDURE *procedure* \[*param1 datatype*\[, *param2 datatype*\[, …\]\] AS sqlstatement

Die CREATE PROCEDURE-Anweisung setzt sich wie folgt zusammen:

|Part|Beschreibung|
|:---|:----------|
|*Prozedur*|Ein Name für die Prozedur. Sie muss den Standardnamenskonventionen entsprechen.|
|*Parameter1*, *Parameter2*|1 bis 255 Feldnamen oder Parameter. Beispiel:<br/><br/>`CREATE PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/>Weitere Informationen zu Parametern finden Sie unter [PARAMETER](parameters-declaration-microsoft-access-sql.md).|
|*Datentyp*|Einer der wichtigsten [Microsoft Access SQL-Datentypen](sql-data-types.md) oder eines der Synonyme.|
|*SQL-Anweisung*|Eine SQL-Anweisung wie SELECT, UPDATE, DELETE, INSERT, CREATE TABLE, DROP TABLE usw.|


## <a name="remarks"></a>Bemerkungen

Eine SQL-Prozedur besteht aus einer PROCEDURE-Klausel,die den Namen der Prozedur angibt, einer optionalen Liste von Parameterdefinitionen und einer einzelnen SQL-Anweisung.

Der Name der Prozedur darf nicht mit dem Namen einer vorhandenen Tabelle übereinstimmen.

## <a name="example"></a>Beispiel

In diesem Beispiel wird die CategoryList-Abfrage benannt und die EnumFields-Prozedur aufgerufen, die im Beispiel für die SELECT-Anweisung enthalten ist.

```vb
    Sub ProcedureX() 
     
        Dim dbs As Database, rst As Recordset 
        Dim qdf As QueryDef, strSql As String 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        strSql = "PROCEDURE CategoryList; " _ 
            & "SELECT DISTINCTROW CategoryName, " _ 
            & "CategoryID FROM Categories " _ 
            & "ORDER BY CategoryName;" 
         
        ' Create a named QueryDef based on the SQL 
        ' statement. 
        Set qdf = dbs.CreateQueryDef("NewQry", strSql) 
     
        ' Create a temporary snapshot-type Recordset. 
        Set rst = qdf.OpenRecordset(dbOpenSnapshot) 
     
        ' Populate the Recordset. 
        rst.MoveLast 
                 
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 15 
         
        ' Delete the QueryDef because this is a 
        ' demonstration. 
        dbs.QueryDefs.Delete "NewQry" 
         
        dbs.Close 
     
    End Sub
```
