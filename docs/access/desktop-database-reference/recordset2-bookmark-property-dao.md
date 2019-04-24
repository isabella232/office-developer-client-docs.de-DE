---
title: Recordset2. Bookmark-Eigenschaft (DAO)
TOCTitle: Bookmark Property
ms:assetid: 7366d550-2f72-ed10-b230-eb144a6f874b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195857(v=office.15)
ms:contentKeyID: 48545637
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 31791e9fb3c7081989232e36a90b184ed7e31866
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307448"
---
# <a name="recordset2bookmark-property-dao"></a>Recordset2. Bookmark-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Legt ein Lesezeichen fest, das den aktuellen Datensatz in einem **Recordset**-Objekt eindeutig identifiziert, oder gibt das Lesezeichen zurück.

## <a name="syntax"></a>Syntax

*Ausdruck* . Lesezeichen

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Bei einem **Recordset** -Objekt, das vollständig auf Tabellen des Microsoft Access-Daten Bank **** Moduls basiert, ist der Wert der Bookmarkable-Eigenschaft true, und Sie können die **Bookmark** -Eigenschaft für dieses Recordset verwenden. Andere Datenbankprodukte unterstützen möglicherweise keine Lesezeichen. Sie können beispielsweise keine Lesezeichen in einem **Recordset2** -Objekt verwenden, das auf einer verknüpften Paradox-Tabelle basiert, die keinen Primärschlüssel aufweist.

Wenn Sie ein **Recordset**-Objekt öffnen, besitzt jeder Datensatz bereits eine eindeutige Textmarke. Weisen Sie der **Bookmark**-Eigenschaft eine Variable zu, um die Textmarke für den aktuellen Datensatz zu speichern. Um jederzeit schnell zu diesem Datensatz zurückkehren zu können, nachdem Sie zu einem anderen Datensatz gewechselt haben, legen Sie die **Bookmark**-Eigenschaft des **Recordset**-Objekts auf den Wert dieser Variablen fest.

Es gibt keine Begrenzung für die Anzahl der verwendbaren Lesezeichen. Um das Lesezeichen eines anderen Datensatzes als des aktuellen Datensatzes zu speichern, müssen Sie zum gewünschten Datensatz wechseln und den Wert der **Bookmark**-Eigenschaft in einer **String**-Variablen speichern, die diesen Datensatz identifiziert.

Sie können feststellen, ob das **Recordset**-Objekt Lesezeichen unterstützt, indem Sie den Wert seiner **[Bookmarkable](recordset2-bookmarkable-property-dao.md)** -Eigenschaft überprüfen, bevor Sie die **Bookmark**-Eigenschaft verwenden. Wenn die **Bookmarkable** -Eigenschaft false ist, unterstützt das **Recordset** -Objekt keine Lesezeichen, und die Verwendung der **Bookmark** -Eigenschaft führt zu einem abfangbaren Fehler.

Wenn Sie mithilfe der **[Clone](recordset2-clone-method-dao.md)** -Methode eine Kopie eines **Recordset**-Objekts erstellen, sind die Werte der **Bookmark**-Eigenschaft für das Original und die Kopie des **Recordset**-Objekts identisch und austauschbar. Es ist jedoch nicht möglich, Lesezeichen unterschiedlicher **Recordset**-Objekte auszutauschen, selbst wenn sie mithilfe desselben Objekts oder derselben SQL-Anweisung erstellt wurden.

Wenn Sie für die **Bookmark**-Eigenschaft einen Wert festlegen, der einen gelöschten Datensatz darstellt, tritt ein auffangbarer Fehler auf.

Der Wert der **Bookmark**-Eigenschaft ist nicht dasselbe wie eine Datensatznummer.

## <a name="example"></a>Beispiel

In diesem Beispiel werden die Eigenschaften **Bookmark** und **Bookmarkable** verwendet, damit der Benutzer einen Datensatz in einer Datensatzgruppe kennzeichnen und später zu ihm zurückkehren kann.

```vb
    Sub BookmarkX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCategories As Recordset2 
     Dim strMessage As String 
     Dim intCommand As Integer 
     Dim varBookmark As Variant 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstCategories = _ 
     dbsNorthwind.OpenRecordset("Categories", _ 
     dbOpenSnapshot) 
     
     With rstCategories 
     
     If .Bookmarkable = False Then 
     Debug.Print "Recordset is not Bookmarkable!" 
     Else 
     ' Populate Recordset. 
     .MoveLast 
     .MoveFirst 
     
     Do While True 
     ' Show information about current record and get 
     ' user input. 
     strMessage = "Category: " & !CategoryName & _ 
     " (record " & (.AbsolutePosition + 1) & _ 
     " of " & .RecordCount & ")" & vbCr & _ 
     "Enter command:" & vbCr & _ 
     "[1 - next / 2 - previous /" & vbCr & _ 
     "3 - set bookmark / 4 - go to bookmark]" 
     intCommand = Val(InputBox(strMessage)) 
     
     Select Case intCommand 
     ' Move forward or backward, trapping for BOF 
     ' or EOF. 
     Case 1 
     .MoveNext 
     If .EOF Then .MoveLast 
     Case 2 
     .MovePrevious 
     If .BOF Then .MoveFirst 
     
     ' Store the bookmark of the current record. 
     Case 3 
     varBookmark = .Bookmark 
     
     ' Go to the record indicated by the stored 
     ' bookmark. 
     Case 4 
     If IsEmpty(varBookmark) Then 
     MsgBox "No Bookmark set!" 
     Else 
     .Bookmark = varBookmark 
     End If 
     
     Case Else 
     Exit Do 
     End Select 
     
     Loop 
     
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

In diesem Beispiel wird die **LastModified**-Eigenschaft verwendet, um den aktuellen Datensatzzeiger auf einen geänderten Datensatz sowie auf einen neu erstellten Datensatz zu verschieben.

```vb
    Sub LastModifiedX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strFirst As String 
     Dim strLast As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     ' Store current data. 
     strFirst = !FirstName 
     strLast = !LastName 
     ' Change data in current record. 
     .Edit 
     !FirstName = "Julie" 
     !LastName = "Warren" 
     .Update 
     ' Move current record pointer to the most recently 
     ' changed or added record. 
     .Bookmark = .LastModified 
     Debug.Print _ 
     "Data in LastModified record after Edit: " & _ 
     !FirstName & " " & !LastName 
     
     ' Restore original data because this is a demonstration. 
     .Edit 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     
     ' Add new record. 
     .AddNew 
     !FirstName = "Roger" 
     !LastName = "Harui" 
     .Update 
     ' Move current record pointer to the most recently 
     ' changed or added record. 
     .Bookmark = .LastModified 
     Debug.Print _ 
     "Data in LastModified record after AddNew: " & _ 
     !FirstName & " " & !LastName 
     
     ' Delete new record because this is a demonstration. 
     .Delete 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
