---
title: Recordset2.NextRecordset-Methode (DAO)
TOCTitle: NextRecordset Method
ms:assetid: 33288131-d4f3-0159-1736-f401346087f3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192318(v=office.15)
ms:contentKeyID: 48544096
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053575
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ada4a573b691fc63a34a9daa5bd60d3aebe0c87d
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997070"
---
# <a name="recordset2nextrecordset-method-dao"></a>Recordset2.NextRecordset-Methode (DAO)


**Betrifft**: Access 2013, Office 2013

## <a name="syntax"></a>Syntax

*Ausdruck* . NextRecordset

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

## <a name="return-value"></a>Rückgabewert

Boolean

## <a name="remarks"></a>Hinweise

In einem ODBCDirect-Arbeitsbereich können Sie ein **Recordset-Objekt** mit mehr als eine select-Abfrage in das Argument Source der **OpenRecordset**oder die **[SQL](querydef-sql-property-dao.md)** -Eigenschaft des **[QueryDef](querydef-object-dao.md)** -Objekt, wie im folgenden Beispiel eine select-Abfrage öffnen.

```sql
    SELECT LastName, FirstName FROM Authors 
    WHERE LastName = 'Smith'; 
    SELECT Title, ISBN FROM Titles 
    WHERE Pub_ID = 9999 
```

Das zurückgegebene **Recordset** wird mit den Ergebnissen der ersten Abfrage geöffnet. Mit der **NextRecordset**-Methode können Sie die resultierenden Datensatzgruppen aus nachfolgenden Abfragen abrufen.

Sind mehrere Datensätze verfügbar (der **OpenRecordset**-Aufruf oder die **SQL**-Eigenschaft enthielt also eine weitere Auswahlabfrage), werden die von der nächsten Abfrage zurückgegebenen Datensätze in das **Recordset** geladen, und **NextRecordset** gibt **True** zurück, was die Verfügbarkeit der Datensätze angibt. Sind keine Datensätze mehr verfügbar (d. h. die Ergebnisse der letzten Auswahlabfrage wurden in das **Recordset**-Objekt geladen), dann gibt **NextRecordset** den Wert **False** zurück, und **Recordset** ist leer.

Zum Leeren des Inhalts eines [Recordset](connection-cancel-method-dao.md)-Objekts können Sie auch die ****Cancel**** -Methode verwenden. Mit **Cancel** werden auch die noch nicht geladenen Datensätze geleert.

## <a name="example"></a>Beispiel

Dieses Beispiel zeigt mit der **NextRecordset**-Methode die Daten aus einer SELECT-Verbundabfrage an. Die **DefaultCursorDriver**-Eigenschaft muss beim Ausführen solcher Abfragen auf **dbUseODBCCursor** festgelegt sein. Die **NextRecordset**-Methode gibt auch dann **True** zurück, wenn einige oder alle der SELECT-Anweisungen keine Datensätze zurückgeben; **False** wird erst zurückgegeben, nachdem jede einzelne SQL-Klausel überprüft wurde.

```vb
    Sub NextRecordsetX() 
     
     Dim wrkODBC As Workspace 
     Dim conPubs As Connection 
     Dim rstTemp As Recordset2 
     Dim intCount As Integer 
     Dim booNext As Boolean 
     
     ' Create ODBCDirect Workspace object and open Connection 
     ' object. The DefaultCursorDriver setting is required 
     ' when using compound SQL statements. 
     Set wrkODBC = CreateWorkspace("", _ 
     "admin", "", dbUseODBC) 
     wrkODBC.DefaultCursorDriver = dbUseODBCCursor 
     
     ' Note: The DSN referenced below must be set to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     Set conPubs = wrkODBC.OpenConnection("Publishers", , , _ 
     "ODBC;DATABASE=pubs;DSN=Publishers") 
     
     ' Construct compound SELECT statement. 
     Set rstTemp = conPubs.OpenRecordset("SELECT * " & _ 
     "FROM authors; " & _ 
     "SELECT * FROM stores; " & _ 
     "SELECT * FROM jobs") 
     
     ' Try printing results from each of the three SELECT 
     ' statements. 
     booNext = True 
     intCount = 1 
     With rstTemp 
     Do While booNext 
     Debug.Print "Contents of recordset #" & intCount 
     Do While Not .EOF 
     Debug.Print , .Fields(0), .Fields(1) 
     .MoveNext 
     Loop 
     booNext = .NextRecordset 
     Debug.Print " rstTemp.NextRecordset = " & _ 
     booNext 
     intCount = intCount + 1 
     Loop 
     End With 
     
     rstTemp.Close 
     conPubs.Close 
     wrkODBC.Close 
     
    End Sub 
```

<br/>

Diese Aufgabe können Sie auch dadurch durchführen, dass Sie eine vorbereitete Anweisung mit der verbundenen SQL-Anweisung erstellen. Die CacheSize-Eigenschaft des QueryDef-Objekts muss auf 1 festgelegt sein, und das Recordset-Objekt muss schreibgeschützt und vom Typ Vorwärts sein.

```vb 
Sub NextRecordsetX2() 
 
 Dim wrkODBC As Workspace 
 Dim conPubs As Connection 
 Dim qdfTemp As QueryDef 
 Dim rstTemp As Recordset2 
 Dim intCount As Integer 
 Dim booNext As Boolean 
 
 ' Create ODBCDirect Workspace object and open Connection 
 ' object. The DefaultCursorDriver setting is required 
 ' when using compound SQL statements. 
 Set wrkODBC = CreateWorkspace("", _ 
 "admin", "", dbUseODBC) 
 wrkODBC.DefaultCursorDriver = dbUseODBCCursor 
 
 ' Note: The DSN referenced below must be set to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkODBC.OpenConnection("Publishers", , , _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Create a temporary stored procedure with a compound 
 ' SELECT statement. 
 Set qdfTemp = conPubs.CreateQueryDef("", _ 
 "SELECT * FROM authors; " & _ 
 "SELECT * FROM stores; " & _ 
 "SELECT * FROM jobs") 
 ' Set CacheSize and open Recordset object with arguments 
 ' that will allow access to multiple recordsets. 
 qdfTemp.CacheSize = 1 
 Set rstTemp = qdfTemp.OpenRecordset(dbOpenForwardOnly, _ 
 dbReadOnly) 
 
 ' Try printing results from each of the three SELECT 
 ' statements. 
 booNext = True 
 intCount = 1 
 With rstTemp 
 Do While booNext 
 Debug.Print "Contents of recordset #" & intCount 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 booNext = .NextRecordset 
 Debug.Print " rstTemp.NextRecordset = " & _ 
 booNext 
 intCount = intCount + 1 
 Loop 
 End With 
 
 rstTemp.Close 
 qdfTemp.Close 
 conPubs.Close 
 wrkODBC.Close 
 
End Sub 
 
```

