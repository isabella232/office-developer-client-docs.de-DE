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
# <a name="recordsetupdate-method-dao"></a><span data-ttu-id="a367e-102">Recordset.Update-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="a367e-102">Recordset.Update Method (DAO)</span></span>

<span data-ttu-id="a367e-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a367e-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="a367e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a367e-104">Syntax</span></span>

<span data-ttu-id="a367e-105">*Ausdruck* . Update (***UpdateType***, ***erzwingen***)</span><span class="sxs-lookup"><span data-stu-id="a367e-105">*expression* .Update(***UpdateType***, ***Force***)</span></span>

<span data-ttu-id="a367e-106">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="a367e-106">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="a367e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a367e-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a367e-108">Name</span><span class="sxs-lookup"><span data-stu-id="a367e-108">Name</span></span></p></th>
<th><p><span data-ttu-id="a367e-109">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="a367e-109">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="a367e-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a367e-110">Data Type</span></span></p></th>
<th><p><span data-ttu-id="a367e-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a367e-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a367e-112">UpdateType</span><span class="sxs-lookup"><span data-stu-id="a367e-112">UpdateType</span></span></p></td>
<td><p><span data-ttu-id="a367e-113">Optional</span><span class="sxs-lookup"><span data-stu-id="a367e-113">Optional</span></span></p></td>
<td><p><span data-ttu-id="a367e-114"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="a367e-114"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="a367e-115">Eine <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> -Konstante, die den Aktualisierungstyp so angibt, wie er in den Einstellungen angegeben ist (nur ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="a367e-115">A <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> constant indicating the type of update, as specified in Settings (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a367e-116">Force</span><span class="sxs-lookup"><span data-stu-id="a367e-116">Force</span></span></p></td>
<td><p><span data-ttu-id="a367e-117">Optional</span><span class="sxs-lookup"><span data-stu-id="a367e-117">Optional</span></span></p></td>
<td><p><span data-ttu-id="a367e-118"><strong>Boolean</strong></span><span class="sxs-lookup"><span data-stu-id="a367e-118"><strong>Boolean</strong></span></span></p></td>
<td><p><span data-ttu-id="a367e-p101">Ein <strong>Boolean</strong> -Wert, der angibt, ob die Änderungen in der Datenbank unabhängig davon erzwungen werden sollen, ob die zugrunde liegenden Daten von einem anderen Benutzer seit dem <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong> -, <strong><a href="fields-delete-method-dao.md">Delete</a></strong> - oder <strong><a href="recordset-edit-method-dao.md">Edit</a></strong> -Aufruf geändert wurden. Falls <strong>True</strong>, werden die Änderungen erzwungen und Änderungen anderer Benutzer werden einfach überschrieben. Falls <strong>False</strong> (Standard), verursachen Änderungen eines anderen Benutzers, während die Aktualisierung noch aussteht, das Fehlschlagen der Aktualisierung für die Änderungen, die einen Konflikt verursachen. Es treten keine Fehler auf, aber die <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> - und <strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong> -Eigenschaften geben die Anzahl der Konflikte bzw. die Anzahl der Zeilen an, die von Konflikten betroffen sind (nur ODBCDirect-Arbeitsbereiche).  </span><span class="sxs-lookup"><span data-stu-id="a367e-p101">A <strong>Boolean</strong> value indicating whether or not to force the changes into the database, regardless of whether the underlying data has been changed by another user since the <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong>, or <strong><a href="recordset-edit-method-dao.md">Edit</a></strong> call. If <strong>True</strong>, the changes are forced and changes made by other users are simply overwritten. If <strong>False</strong> (default), changes made by another user while the update is pending will cause the update to fail for those changes that are in conflict. No error occurs, but the <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> and <strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong> properties will indicate the number of conflicts and the rows affected by conflicts, respectively (ODBCDirect workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a367e-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a367e-123">Remarks</span></span>

<span data-ttu-id="a367e-124">Verwenden Sie **Update**, um den aktuellen Datensatz und alle daran vorgenommenen Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a367e-124">Use **Update** to save the current record and any changes you've made to it.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a367e-125">[!WICHTIG] Änderungen an dem aktuellen Datensatz gehen in folgenden Fällen verloren:</span><span class="sxs-lookup"><span data-stu-id="a367e-125">Changes to the current record are lost if:</span></span>
> - <span data-ttu-id="a367e-126">Sie verwenden die **Edit**- oder **AddNew**-Methode und wechseln dann zu einem anderen Datensatz, ohne zuvor **Update** zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a367e-126">You use the **Edit** or **AddNew** method, and then move to another record without first using **Update**.</span></span>
> - <span data-ttu-id="a367e-127">Sie verwenden **Edit** oder **AddNew** und dann erneut **Edit** oder **AddNew**, ohne zuvor **Update** zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a367e-127">You use **Edit** or **AddNew**, and then use **Edit** or **AddNew** again without first using **Update**.</span></span>
> - <span data-ttu-id="a367e-128">Sie legen die **[Bookmark](recordset-bookmark-property-dao.md)** -Eigenschaft auf einen anderen Datensatz fest.</span><span class="sxs-lookup"><span data-stu-id="a367e-128">You set the **[Bookmark](recordset-bookmark-property-dao.md)** property to another record.</span></span>
> - <span data-ttu-id="a367e-129">Sie schließen das **Recordset**, ohne zuvor **Update** zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a367e-129">You close the **Recordset** without first using **Update**.</span></span>
> - <span data-ttu-id="a367e-130">Sie brechen den **Edit**-Vorgang ab, indem Sie **[CancelUpdate](recordset-cancelupdate-method-dao.md)** verwenden.</span><span class="sxs-lookup"><span data-stu-id="a367e-130">You cancel the **Edit** operation by using **[CancelUpdate](recordset-cancelupdate-method-dao.md)**.</span></span>

<span data-ttu-id="a367e-p102">Wenn Sie einen Datensatz bearbeiten möchten, verwenden Sie die **Edit**-Methode, um den Inhalt des aktuellen Datensatzes in den Kopierpuffer zu kopieren. Ohne vorheriges Anwenden von **Edit** tritt ein Fehler auf, sobald Sie **Update** verwenden oder versuchen, den Wert eines Felds zu ändern.</span><span class="sxs-lookup"><span data-stu-id="a367e-p102">To edit a record, use the **Edit** method to copy the contents of the current record to the copy buffer. If you don't use **Edit** first, an error occurs when you use **Update** or attempt to change a field's value.</span></span>

<span data-ttu-id="a367e-133">In einem ODBCDirect-Arbeitsbereich können Sie Batchaktualisierungen vornehmen, wenn die Cursor-Bibliothek dies unterstützt und das **Recordset** mit der Option der optimistischen Batchsperre geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="a367e-133">In an ODBCDirect workspace, you can do batch updates, provided the cursor library supports batch updates, and the **Recordset** was opened with the optimistic batch locking option.</span></span>

<span data-ttu-id="a367e-134">Ist in einem Microsoft Access-Arbeitsbereich die **LockEdits**-Eigenschafteneinstellung eines **Recordset**-Objekts in einer Mehrbenutzerumgebung auf **True** festgelegt (pessimistisch gesperrt), bleibt der Datensatz ab dem Moment gesperrt, in dem **Edit** verwendet wird, bis zu dem Zeitpunkt, zu dem die **Update**-Methode ausgeführt oder die Bearbeitung abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="a367e-134">In a Microsoft Access workspace, when the **Recordset** object's **LockEdits** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the **Update** method is executed or the edit is canceled.</span></span> <span data-ttu-id="a367e-135">Wenn die **LockEdits**-Eigenschafteneinstellung auf **False** festgelegt ist (optimistisch gesperrt), wird der Datensatz gesperrt und mit dem vorab bearbeiteten Datensatz verglichen, bevor er in der Datenbank aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="a367e-135">If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it is updated in the database.</span></span> 

<span data-ttu-id="a367e-136">Wurde der Datensatz nach dem Verwenden der **Edit**-Methode geändert, schlägt der **Update**-Vorgang fehl.</span><span class="sxs-lookup"><span data-stu-id="a367e-136">If the record has changed since you used the **Edit** method, the **Update** operation fails.</span></span> <span data-ttu-id="a367e-137">Die mit einem Microsoft Access-Datenbankmodul verbundenen ODBC- und installierbaren ISAM-Datenbanken verwenden immer optimistische Sperren.</span><span class="sxs-lookup"><span data-stu-id="a367e-137">Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span> <span data-ttu-id="a367e-138">Verwenden Sie erneut die **Update**-Methode, um den **Update**-Vorgang mit Ihren Änderungen fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="a367e-138">To continue the **Update** operation with your changes, use the **Update** method again.</span></span> <span data-ttu-id="a367e-139">Zum Zurücksetzen auf als anderer Benutzer den Datensatz geändert, aktualisieren Sie den aktuellen Datensatz mit Move 0.</span><span class="sxs-lookup"><span data-stu-id="a367e-139">To revert to the record as the other user changed it, refresh the current record by using Move 0.</span></span>


> [!NOTE]
> <span data-ttu-id="a367e-p105">[!HINWEIS] Um einen Datensatz hinzuzufügen, zu bearbeiten oder zu löschen, muss es einen eindeutigen Index im Datensatz in der zugrunde liegenden Datenquelle geben. Andernfalls tritt ein "Berechtigung verweigert"-Fehler im **AddNew** -, **Delete** - oder **Edit** -Methodenaufruf in einem Microsoft Access-Arbeitsbereich auf, oder ein "Ungültiges Argument"-Fehler tritt beim **Update** -Aufruf in einem ODBCDirect-Arbeitsbereich auf.</span><span class="sxs-lookup"><span data-stu-id="a367e-p105">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the **AddNew**, **Delete**, or **Edit** method call in a Microsoft Access workspace, or an "Invalid argument" error will occur on the **Update** call in an ODBCDirect workspace.</span></span>

## <a name="example"></a><span data-ttu-id="a367e-142">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a367e-142">Example</span></span>

<span data-ttu-id="a367e-143">Dieses Beispiel demonstriert die **Update** -Methode zusammen mit der **Edit** -Methode.</span><span class="sxs-lookup"><span data-stu-id="a367e-143">This example demonstrates the **Update** method in conjunction with **Edit** method.</span></span>

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

<span data-ttu-id="a367e-144">Dieses Beispiel demonstriert die **Update** -Methode zusammen mit der **AddNew** -Methode.</span><span class="sxs-lookup"><span data-stu-id="a367e-144">This example demonstrates the **Update** method in conjunction with the **AddNew** method.</span></span>

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

<span data-ttu-id="a367e-145">Dieses Beispiel verwendet die **BatchCollisionCount** -Eigenschaft und die **Update** -Methode, um die Batchaktualisierung zu demonstrieren, wenn Konflikte durch Erzwingen der Batchaktualisierung gelöst werden.</span><span class="sxs-lookup"><span data-stu-id="a367e-145">This example uses the **BatchCollisionCount** property and the **Update** method to demonstrate batch updating where any collisions are resolved by forcing the batch update.</span></span>

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

<span data-ttu-id="a367e-p106">Dieses Beispiel verwendet die **AddNew** -Methode, um einen neuen Datensatz mit dem angegebenen Namen zu erstellen. Die "AddName"-Funktion ist zum Ausführen dieser Prozedur erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a367e-p106">This example uses the **AddNew** method to create a new record with the specified name. The AddName function is required for this procedure to run.</span></span>

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
