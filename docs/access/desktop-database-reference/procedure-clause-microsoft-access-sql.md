---
title: PROCEDURE-Klausel (Microsoft Access SQL)
TOCTitle: PROCEDURE Clause (Microsoft Access SQL)
ms:assetid: a718802c-9260-88d5-ec29-d5e5594927b0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821342(v=office.15)
ms:contentKeyID: 48546872
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277578
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 5ea21939115f31d760cd528a07922deeeaaef499
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473462"
---
# <a name="procedure-clause-microsoft-access-sql"></a>PROCEDURE-Klausel (Microsoft Access SQL)

**Betrifft**: Access 2013 | Office 2013

Definiert einen Namen und optionale Parameter für eine Abfrage.

> [!NOTE]
> [!HINWEIS] Die PROCEDURE-Klausel wurde durch die PROCEDURE-Anweisung abgelöst. Zwar wird die PROCEDURE-Klausel noch unterstützt, doch die PROCEDURE-Anweisung stellt eine Übermenge der Funktionen der PROCEDURE-Klausel bereit und wird als Syntax empfohlen.

## <a name="syntax"></a>Syntax

*Name* der Prozedur \[ *param1 Datentyp*\[, *param2 Datentyp*\[,...\]\]

Die PROCEDURE-Klausel enthält die folgenden Bestandteile:

|Argument |Beschreibung |
|:----|:-----------|
|*name* |Ein Name für die Prozedur. Bei der Namensgebung müssen die Standardbenennungsregeln beachtet werden.|
|*Param1*, *Param2* |Ein oder mehrere Feldnamen oder Parameter. Beispiel:
<br/><br/>`PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/>Weitere Informationen zu Parametern finden Sie unter [Parameter](parameters-declaration-microsoft-access-sql.md).|
|*Datentyp* | Einer der wichtigsten [Microsoft Access SQL-Datentypen](sql-data-types.md) oder eines der Synonyme. |


## <a name="remarks"></a>Hinweise

Eine SQL-Prozedur besteht aus einer PROCEDURE-Klausel (die den Namen der Prozedur angibt), einer optionalen Liste mit Parameterdefinitionen und einer einzelnen SQL­Anweisung. Das Verfahren Get\_Teil\_Anzahl möglicherweise führen Sie eine Abfrage, die eine angegebene Teilenummer abruft.

> [!NOTE]
> - Wenn die Klausel mehr als eine Felddefinition (d. h., *Param-Datentyp* -Paare) enthält, müssen Sie diese durch Kommas getrennt werden.
> - Auf die PROCEDURE-Klausel muss eine SQL-Anweisung folgen (z. B. eine [SELECT](select-statement-microsoft-access-sql.md)- oder eine [UPDATE](update-statement-microsoft-access-sql.md)-Anweisung).

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
