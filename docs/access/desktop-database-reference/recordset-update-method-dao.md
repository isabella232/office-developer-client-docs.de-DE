---
title: Recordset.Update-Methode (DAO)
TOCTitle: Update Method
ms:assetid: aad4171a-da95-ed72-86b3-714615ea0ac8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821467(v=office.15)
ms:contentKeyID: 48546961
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0fa0b6897ea148a57cc17fcc0f908e2fdcae6b26
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472969"
---
# <a name="recordsetupdate-method-dao"></a>Recordset.Update-Methode (DAO)

**Betrifft**: Access 2013 | Office 2013

## <a name="syntax"></a>Syntax

*Ausdruck* . Update (***UpdateType***, ***erzwingen***)

*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.

### <a name="parameters"></a>Parameter

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Erforderlich/Optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>UpdateType</p></td>
<td><p>Optional</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Eine <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> -Konstante, die den Aktualisierungstyp so angibt, wie er in den Einstellungen angegeben ist (nur ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p>Force</p></td>
<td><p>Optional</p></td>
<td><p><strong>Boolean</strong></p></td>
<td><p>Ein <strong>Boolean</strong> -Wert, der angibt, ob die Änderungen in der Datenbank unabhängig davon erzwungen werden sollen, ob die zugrunde liegenden Daten von einem anderen Benutzer seit dem <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong> -, <strong><a href="fields-delete-method-dao.md">Delete</a></strong> - oder <strong><a href="recordset-edit-method-dao.md">Edit</a></strong> -Aufruf geändert wurden. Falls <strong>True</strong>, werden die Änderungen erzwungen und Änderungen anderer Benutzer werden einfach überschrieben. Falls <strong>False</strong> (Standard), verursachen Änderungen eines anderen Benutzers, während die Aktualisierung noch aussteht, das Fehlschlagen der Aktualisierung für die Änderungen, die einen Konflikt verursachen. Es treten keine Fehler auf, aber die <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> - und <strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong> -Eigenschaften geben die Anzahl der Konflikte bzw. die Anzahl der Zeilen an, die von Konflikten betroffen sind (nur ODBCDirect-Arbeitsbereiche).  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Verwenden Sie **Update**, um den aktuellen Datensatz und alle daran vorgenommenen Änderungen zu speichern.

> [!IMPORTANT]
> [!WICHTIG] Änderungen an dem aktuellen Datensatz gehen in folgenden Fällen verloren:
> - Sie verwenden die **Edit**- oder **AddNew**-Methode und wechseln dann zu einem anderen Datensatz, ohne zuvor **Update** zu verwenden.
> - Sie verwenden **Edit** oder **AddNew** und dann erneut **Edit** oder **AddNew**, ohne zuvor **Update** zu verwenden.
> - Sie legen die **[Bookmark](recordset-bookmark-property-dao.md)** -Eigenschaft auf einen anderen Datensatz fest.
> - Sie schließen das **Recordset**, ohne zuvor **Update** zu verwenden.
> - Sie brechen den **Edit**-Vorgang ab, indem Sie **[CancelUpdate](recordset-cancelupdate-method-dao.md)** verwenden.

Wenn Sie einen Datensatz bearbeiten möchten, verwenden Sie die **Edit**-Methode, um den Inhalt des aktuellen Datensatzes in den Kopierpuffer zu kopieren. Ohne vorheriges Anwenden von **Edit** tritt ein Fehler auf, sobald Sie **Update** verwenden oder versuchen, den Wert eines Felds zu ändern.

In einem ODBCDirect-Arbeitsbereich können Sie Batchaktualisierungen vornehmen, wenn die Cursor-Bibliothek dies unterstützt und das **Recordset** mit der Option der optimistischen Batchsperre geöffnet wurde.

Ist in einem Microsoft Access-Arbeitsbereich die **LockEdits**-Eigenschafteneinstellung eines **Recordset**-Objekts in einer Mehrbenutzerumgebung auf **True** festgelegt (pessimistisch gesperrt), bleibt der Datensatz ab dem Moment gesperrt, in dem **Edit** verwendet wird, bis zu dem Zeitpunkt, zu dem die **Update**-Methode ausgeführt oder die Bearbeitung abgebrochen wird. Wenn die **LockEdits**-Eigenschafteneinstellung auf **False** festgelegt ist (optimistisch gesperrt), wird der Datensatz gesperrt und mit dem vorab bearbeiteten Datensatz verglichen, bevor er in der Datenbank aktualisiert wird. 

Wurde der Datensatz nach dem Verwenden der **Edit**-Methode geändert, schlägt der **Update**-Vorgang fehl. Die mit einem Microsoft Access-Datenbankmodul verbundenen ODBC- und installierbaren ISAM-Datenbanken verwenden immer optimistische Sperren. Verwenden Sie erneut die **Update**-Methode, um den **Update**-Vorgang mit Ihren Änderungen fortzusetzen. Zum Zurücksetzen auf als anderer Benutzer den Datensatz geändert, aktualisieren Sie den aktuellen Datensatz mit Move 0.


> [!NOTE]
> [!HINWEIS] Um einen Datensatz hinzuzufügen, zu bearbeiten oder zu löschen, muss es einen eindeutigen Index im Datensatz in der zugrunde liegenden Datenquelle geben. Andernfalls tritt ein "Berechtigung verweigert"-Fehler im **AddNew** -, **Delete** - oder **Edit** -Methodenaufruf in einem Microsoft Access-Arbeitsbereich auf, oder ein "Ungültiges Argument"-Fehler tritt beim **Update** -Aufruf in einem ODBCDirect-Arbeitsbereich auf.

## <a name="example"></a>Beispiel

Dieses Beispiel demonstriert die **Update** -Methode zusammen mit der **Edit** -Methode.

```vb
    Sub UpdateX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strOldFirst As String 
     Dim strOldLast As String 
     Dim strMessage As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     .Edit 
     ' Store original data. 
     strOldFirst = !FirstName 
     strOldLast = !LastName 
     ' Change data in edit buffer. 
     !FirstName = "Linda" 
     !LastName = "Kobara" 
     
     ' Show contents of buffer and get user input. 
     strMessage = "Edit in progress:" & vbCr & _ 
     " Original data = " & strOldFirst & " " & _ 
     strOldLast & vbCr & " Data in buffer = " & _ 
     !FirstName & " " & !LastName & vbCr & vbCr & _ 
     "Use Update to replace the original data with " & _ 
     "the buffered data in the Recordset?" 
     
     If MsgBox(strMessage, vbYesNo) = vbYes Then 
     .Update 
     Else 
     .CancelUpdate 
     End If 
     
     ' Show the resulting data. 
     MsgBox "Data in recordset = " & !FirstName & " " & _ 
     !LastName 
     
     ' Restore original data because this is a demonstration. 
     If Not (strOldFirst = !FirstName And _ 
     strOldLast = !LastName) Then 
     .Edit 
     !FirstName = strOldFirst 
     !LastName = strOldLast 
     .Update 
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

Dieses Beispiel demonstriert die **Update** -Methode zusammen mit der **AddNew** -Methode.

```vb
    Sub UpdateX2() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strOldFirst As String 
     Dim strOldLast As String 
     Dim strMessage As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     .AddNew 
     !FirstName = "Bill" 
     !LastName = "Sornsin" 
     
     ' Show contents of buffer and get user input. 
     strMessage = "AddNew in progress:" & vbCr & _ 
     " Data in buffer = " & !FirstName & " " & _ 
     !LastName & vbCr & vbCr & _ 
     "Use Update to save buffer to recordset?" 
     
     If MsgBox(strMessage, vbYesNoCancel) = vbYes Then 
     .Update 
     ' Go to the new record and show the resulting data. 
     .Bookmark = .LastModified 
     MsgBox "Data in recordset = " & !FirstName & _ 
     " " & !LastName 
     ' Delete new data because this is a demonstration. 
     .Delete 
     Else 
     .CancelUpdate 
     MsgBox "No new record added." 
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

Dieses Beispiel verwendet die **BatchCollisionCount** -Eigenschaft und die **Update** -Methode, um die Batchaktualisierung zu demonstrieren, wenn Konflikte durch Erzwingen der Batchaktualisierung gelöst werden.

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

<br/>

Dieses Beispiel verwendet die **AddNew** -Methode, um einen neuen Datensatz mit dem angegebenen Namen zu erstellen. Die "AddName"-Funktion ist zum Ausführen dieser Prozedur erforderlich.

```vb
    Sub AddNewX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strFirstName As String 
     Dim strLastName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", dbOpenDynaset) 
     
     ' Get data from the user. 
     strFirstName = Trim(InputBox( _ 
     "Enter first name:")) 
     strLastName = Trim(InputBox( _ 
     "Enter last name:")) 
     
     ' Proceed only if the user actually entered something 
     ' for both the first and last names. 
     If strFirstName <> "" and strLastName <> "" Then 
     
     ' Call the function that adds the record. 
     AddName rstEmployees, strFirstName, strLastName 
     
     ' Show the newly added data. 
     With rstEmployees 
     Debug.Print "New record: " & !FirstName & _ 
     " " & !LastName 
     ' Delete new record because this is a demonstration. 
     .Delete 
     End With 
     
     Else 
     Debug.Print _ 
     "You must input a string for first and last name!" 
     End If 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function AddName(rstTemp As Recordset, _ 
     strFirst As String, strLast As String) 
     
     ' Adds a new record to a Recordset using the data passed 
     ' by the calling procedure. The new record is then made 
     ' the current record. 
     With rstTemp 
     .AddNew 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     .Bookmark = .LastModified 
     End With 
     
    End Function
```
