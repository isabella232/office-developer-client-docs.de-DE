---
title: Recordset.BatchCollisionCount Property (DAO)
TOCTitle: BatchCollisionCount Property
ms:assetid: 9d166463-8313-c0f5-8389-5d5ad933eb33
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198240(v=office.15)
ms:contentKeyID: 48546617
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101181
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2c2cc3e9351eba04d1c05555b2f6b22284a8e6c0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475626"
---
# <a name="recordsetbatchcollisioncount-property-dao"></a>Recordset.BatchCollisionCount Property (DAO)


**Betrifft**: Access 2013 | Office 2013

## <a name="syntax"></a>Syntax

*Ausdruck* . BatchCollisionCount

*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt die Anzahl von Datensätzen an, bei denen Konflikte oder andere Fehler beim letzten Versuch einer Batchaktualisierung auftraten. Der Wert dieser Eigenschaft entspricht der Anzahl von Textmarken in der **[BatchCollisions](recordset-batchcollisions-property-dao.md)** -Eigenschaft.

Wenn Sie die **[Bookmark](recordset-object-dao.md)** -Eigenschaft des aktiven **[Recordset](recordset-bookmark-property-dao.md)** -Objekts auf Textmarkenwerte im **BatchCollisions**-Array festlegen, können Sie zu jedem Datensatz wechseln, bei dem die letzte **[Update](recordset-update-method-dao.md)** -Batchoperation nicht abgeschlossen werden konnte.

Nachdem die Datensätze, die einen Konflikt verursacht haben, korrigiert wurden, kann erneut eine **Update**-Methode im Batchmodus aufgerufen werden. DAO versucht eine weitere Batchaktualisierung, und die **BatchCollisions**-Eigenschaft spiegelt die Datensatzgruppe wider, die beim zweiten Versuch nicht verarbeitet werden konnte. Alle Datensätze, die in der vorherigen Versuch erfolgreich abgeschlossen werden nicht in der aktuellen Versuch gesendet, da sie nun eine **[RecordStatus](recordset-recordstatus-property-dao.md)** -Eigenschaft der Wert DbRecordUnmodified aufweisen. Dieser Vorgang wird so lange fortgesetzt, bis keine Konflikte mehr auftreten oder bis Sie die Aktualisierung abbrechen und die Ergebnismenge schließen.

## <a name="example"></a>Beispiel

Dieses Beispiel verwendet die **BatchCollisionCount**-Eigenschaft und die **Update**-Methode und zeigt eine Batchaktualisierung, bei der Konflikte durch Erzwingen der Aktualisierung gelöst werden.

```vb 
Sub BatchX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
 Dim intLoop As Integer 
 Dim strPrompt As String 
 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 ' This DefaultCursorDriver setting is required for 
 ' batch updating. 
 wrkMain.DefaultCursorDriver = dbUseClientBatchCursor 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' The following locking argument is required for 
 ' batch updating. It is also required that a table 
 ' with a primary key is used. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Modify data in local recordset. 
 Do While Not .EOF 
 .Edit 
 If !royalty <= 20 Then 
 !royalty = !royalty - 4 
 Else 
 !royalty = !royalty + 2 
 End If 
 .Update 
 .MoveNext 
 Loop 
 
 ' Attempt a batch update. 
 .Update dbUpdateBatch 
 
 ' If there are collisions, give the user the option 
 ' of forcing the changes or resolving them 
 ' individually. 
 If .BatchCollisionCount > 0 Then 
 strPrompt = "There are collisions. " & vbCr & _ 
 "Do you want the program to force " & _ 
 vbCr & "an update using the local data?" 
 If MsgBox(strPrompt, vbYesNo) = vbYes Then _ 
 .Update dbUpdateBatch, True 
 End If 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

