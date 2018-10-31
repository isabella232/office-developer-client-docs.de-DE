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
ms.openlocfilehash: 573ec86a573697ebe52886535f8544bbaab61d7d
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861464"
---
# <a name="create-procedure-statement-microsoft-access-sql"></a>CREATE PROCEDURE-Anweisung (Microsoft Access SQL)

**Betrifft**: Access 2013 | Office 2013 

Erstellt eine gespeicherte Prozedur.

> [!NOTE]
> [!HINWEIS] Vom Microsoft Access-Datenbankmodul wird die Verwendung der CREATE PROCEDURE- oder anderer DDL-Anweisungen in Datenbanken, die nicht aus dem Microsoft Jet-Datenbankmodul stammen, nicht unterstützt.

## <a name="syntax"></a>Syntax

CREATE PROCEDURE *Prozedur* \[ *param1 Datentyp*\[, *param2 Datentyp*\[,... \] \] Als SQL-Anweisung

Die CREATE PROCEDURE-Anweisung besteht aus drei Komponenten:

|Komponente|Beschreibung|
|:---|:----------|
|*Prozedur*|Ein Name für die Prozedur. Bei der Namensgebung müssen die Standardbenennungsregeln beachtet werden.|
|*Param1*, *Param2*|Einer von 255 Feldnamen oder Parametern. Beispiel:
<br/><br/>`CREATE PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/>Weitere Informationen zu Parametern finden Sie unter [Parameter](parameters-declaration-microsoft-access-sql.md).|
|*Datentyp*|Einer der wichtigsten [Microsoft Access SQL-Datentypen](sql-data-types.md) oder eines der Synonyme.|
|*SQL-Anweisung*|Eine SQL-Anweisung wie SELECT, UPDATE, DELETE, INSERT, CREATE TABLE, DROP TABLE usw.|


## <a name="remarks"></a>Hinweise

Eine SQL-Prozedur besteht aus einer PROCEDURE-Klausel, die den Namen der Prozedur angibt, einer optionalen Liste mit Parameterdefinitionen und einer einzelnen SQL-Anweisung.

Ein Prodezurname darf nicht mit dem Namen einer bestehenden Tabelle übereinstimmen.

## <a name="example"></a>Beispiel

In diesem Beispiel wird die Abfrage categoryList verwendet, und es wird die EnumFields-Prozedur, die Sie in diesem Beispiel wird die SELECT-Anweisung finden.

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
