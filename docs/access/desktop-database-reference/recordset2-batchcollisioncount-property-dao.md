---
title: Recordset2. BatchCollisionCount-Eigenschaft (DAO)
TOCTitle: BatchCollisionCount Property
ms:assetid: 997dfbb3-673c-8813-f51b-ab8d95093c4f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197961(v=office.15)
ms:contentKeyID: 48546514
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 33650b9fdbaf7fbc9266c8c778199e1138cd5b21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307483"
---
# <a name="recordset2batchcollisioncount-property-dao"></a>Recordset2. BatchCollisionCount-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

## <a name="syntax"></a>Syntax

*Ausdruck* . BatchCollisionCount

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt an, wie viele Datensätze auf Konflikte gestoßen sind oder aus einem anderen Grund bei der letzten Aktualisierung nicht aktualisiert werden konnten. Der Wert dieser Eigenschaft entspricht der Anzahl der Lesezeichen in der **[BatchCollisions](recordset2-batchcollisions-property-dao.md)** -Eigenschaft.

Wenn Sie die [**Bookmark**](recordset2-bookmark-property-dao.md) -Eigenschaft des aktiven **Recordset**-Objekts so festlegen, dass Werte im **BatchCollisions**-Array mit einem Lesezeichen versehen werden, können Sie zu jedem Datensatz navigieren, der beim letzten **[Update](recordset2-update-method-dao.md)** -Batchvorgang nicht verarbeitet werden konnte.

Nachdem die Datensätze, die einen Konflikt verursacht haben, korrigiert wurden, kann erneut eine **Update**-Methode im Batchmodus aufgerufen werden. DAO versucht eine weitere Batchaktualisierung, und die **BatchCollisions**-Eigenschaft spiegelt die Datensatzgruppe wider, die beim zweiten Versuch nicht verarbeitet werden konnte. Alle Datensätze, die beim vorhergehenden Versuch erfolgreich verarbeitet wurden, werden nun nicht mehr gesendet, da ihre **[RecordStatus](recordset2-recordstatus-property-dao.md)** -Eigenschaft nun den Wert **dbRecordUnmodified** hat. Dieser Vorgang wird so lange fortgesetzt, bis keine Konflikte mehr auftreten oder bis Sie die Aktualisierung abbrechen und die Ergebnismenge schließen.

## <a name="example"></a>Beispiel

In diesem Beispiel wird mithilfe der **BatchCollisionCount**-Eigenschaft und der **Update**-Methode die Batchaktualisierung veranschaulicht. Konflikte werden durch das Erzwingen der Batchaktualisierung gelöst.

```vb 
Sub BatchX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset2 
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

