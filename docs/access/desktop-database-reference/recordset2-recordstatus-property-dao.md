---
title: Recordset2.RecordStatus Property (DAO)
TOCTitle: RecordStatus Property
ms:assetid: 178872a9-e361-f277-627d-f91b01ceb6d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845575(v=office.15)
ms:contentKeyID: 48543451
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a13f9f64ab6f699979633c70fb2e8a9386ce2134
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472641"
---
# <a name="recordset2recordstatus-property-dao"></a>Recordset2.RecordStatus Property (DAO)


**Betrifft**: Access 2013 | Office 2013

## <a name="syntax"></a>Syntax

*Ausdruck* . RecordStatus

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Der Wert der **RecordStatus**-Eigenschaft gibt an, ob und wie der aktuelle Datensatz an der nächsten optimistischen Batchaktualisierung beteiligt ist.

Wenn ein Benutzer einen Datensatz ändert, wird die **RecordStatus**-Eigenschaft für diesen Datensatz automatisch in **dbRecordModified** geändert. Wenn ein Datensatz hinzugefügt oder gelöscht wird, enthält **RecordStatus** ebenfalls die entsprechende Konstante. Wenn Sie dann eine **[Update](recordset2-update-method-dao.md)** -Methode im Batchmodus verwenden, sendet DAO für jeden Datensatz, basierend auf der **RecordStatus**-Eigenschaft des Datensatzes, einen geeigneten Vorgang an den Remoteserver.

## <a name="example"></a>Beispiel

In diesem Beispiel werden die Eigenschaften RecordStatus und DefaultCursorDriver verwendet, um zu zeigen, wie Änderungen eines lokalen Recordset-Objekts während einer Batchaktualisierung verfolgt werden. Zum Ausführen dieser Prozedur ist die RecordStatusOutput-Funktion erforderlich.

```vb 
Sub RecordStatusX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset2 
 
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
 ' batch updating. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM authors", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 .MoveFirst 
 Debug.Print "Original record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 .Edit 
 !au_lname = "Bowen" 
 .Update 
 Debug.Print "Edited record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 .AddNew 
 !au_lname = "NewName" 
 .Update 
 Debug.Print "New record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 .Delete 
 Debug.Print "Deleted record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 ' Close the local recordset without updating the 
 ' data on the server. 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
Function RecordStatusOutput(lngTemp As Long) As String 
 
 Dim strTemp As String 
 
 strTemp = "" 
 
 ' Construct an output string based on the RecordStatus 
 ' value. 
If lngTemp = dbRecordUnmodified Then _ 
 strTemp = "[dbRecordUnmodified]" 
 If lngTemp = dbRecordModified Then _ 
 strTemp = "[dbRecordModified]" 
 If lngTemp = dbRecordNew Then _ 
 strTemp = "[dbRecordNew]" 
 If lngTemp = dbRecordDeleted Then _ 
 strTemp = "[dbRecordDeleted]" 
 If lngTemp = dbRecordDBDeleted Then _ 
 strTemp = "[dbRecordDBDeleted]" 
 
 RecordStatusOutput = strTemp 
 
End Function 
 
```
