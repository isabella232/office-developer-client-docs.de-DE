---
title: TableDef.RefreshLink-Methode (DAO)
TOCTitle: RefreshLink Method
ms:assetid: 9f0059c6-3b7b-57e3-7527-ef674ad9417d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198349(v=office.15)
ms:contentKeyID: 48546674
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052980
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 88cd8083f8dc1b71c574be1e31a8b7b735595090
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876876"
---
# <a name="tabledefrefreshlink-method-dao"></a>TableDef.RefreshLink-Methode (DAO)

**Betrifft**: Access 2013, Office 2013
 
Aktualisiert die Verbindungsinformation für eine verknüpfte Tabelle (gilt nur für Microsoft Access-Arbeitsbereiche ).

## <a name="syntax"></a>Syntax

*Ausdruck* . RefreshLink

*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Wenn Sie die Verbindungsinformationen für eine verknüpfte Tabelle ändern möchten, müssen Sie die **[Connect](connection-connect-property-dao.md)** -Eigenschaft des entsprechenden **TableDef**-Objekts zurücksetzen und die Informationen anschließend mit der **RefreshLink**-Methode aktualisieren. Beim Verwenden von **RefreshLink** werden keine Änderungen an den Eigenschaften der verknüpften Tabelle und an **[Relation](relation-object-dao.md)** -Objekten vorgenommen.

Sie müssen für jede Auflistung die [**Refresh**](tabledefs-refresh-method-dao.md) -Methode verwenden, damit diese Verbindungsinformationen in allen Auflistungen vorhanden sind, die mit dem **TableDef**-Objekt verknüpft sind, das der verknüpften Tabelle entspricht.

## <a name="example"></a>Beispiel

In diesem Beispiel wird die RefreshLink-Methode verwendet, um die Daten in einer verknüpften Tabelle zu aktualisieren, nachdem sich deren Verbindung in Bezug auf die Datenquelle geändert hat. Zum Ausführen dieses Vorgangs ist die RefreshLinkOutput-Prozedur erforderlich.

```vb 
Sub RefreshLinkX() 
 
 Dim dbsCurrent As Database 
 Dim tdfLinked As TableDef 
 
 ' Open a database to which a linked table can be 
 ' appended. 
 Set dbsCurrent = OpenDatabase("DB1.mdb") 
 
 ' Create a linked table that points to a Microsoft 
 ' SQL Server database. 
 Set tdfLinked = _ 
 dbsCurrent.CreateTableDef("AuthorsTable") 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 tdfLinked.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 tdfLinked.SourceTableName = "authors" 
 dbsCurrent.TableDefs.Append tdfLinked 
 
 ' Display contents of linked table. 
 Debug.Print _ 
 "Data from linked table connected to first source:" 
 RefreshLinkOutput dbsCurrent 
 
 ' Change connection information for linked table and 
 ' refresh the connection in order to make the new data 
 ' available. 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 tdfLinked.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=NewPublishers" 
 tdfLinked.RefreshLink 
 
 ' Display contents of linked table. 
 Debug.Print _ 
 "Data from linked table connected to second source:" 
 RefreshLinkOutput dbsCurrent 
 
 ' Delete linked table because this is a demonstration. 
 dbsCurrent.TableDefs.Delete tdfLinked.Name 
 
 dbsCurrent.Close 
 
End Sub 
 
Sub RefreshLinkOutput(dbsTemp As Database) 
 
 Dim rstRemote As Recordset 
 Dim intCount As Integer 
 
 ' Open linked table. 
 Set rstRemote = _ 
 dbsTemp.OpenRecordset("AuthorsTable") 
 
 intCount = 0 
 
 ' Enumerate Recordset object, but stop at 50 records. 
 With rstRemote 
 Do While Not .EOF And intCount < 50 
 Debug.Print , .Fields(0), .Fields(1) 
 intCount = intCount + 1 
 .MoveNext 
 Loop 
 If Not .EOF Then Debug.Print , "[more records]" 
 .Close 
 End With 
 
End Sub 
 
```

