---
title: Recordset.Bookmark-Eigenschaft (DAO)
TOCTitle: Bookmark Property
ms:assetid: c4b1c2d9-668e-e365-544c-efb4ae4efcc9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823084(v=office.15)
ms:contentKeyID: 48547597
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052887
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: 08c68c7ff58fb0dc0397ea7895f5efc58b99ccc9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617668"
---
# <a name="recordsetbookmark-property-dao"></a>Recordset.Bookmark-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Legt eine Textmarke fest oder gibt sie zurück. Sie identifiziert den aktuellen Datensatz eindeutig in einem **[Recordset](recordset-object-dao.md)**-Objekt.

## <a name="syntax"></a>Syntax

*Ausdruck* .Bookmark

*Ausdruck* Eine Variable, die ein **Recordset**-Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Bei einem **Recordset** -Objekt, das vollständig auf Tabellen der Microsoft Access-Datenbank-Engine basiert, lautet der Wert der **Bookmarkable** -Eigenschaft „True“, und Sie können die **Bookmark** -Eigenschaft mit diesem **Recordset-** verwenden. Andere Datenbankprodukte unterstützen jedoch möglicherweise keine Lesezeichen. Beispielsweise können Sie Lesezeichen in keinem **Recordset-** -Objekt verwenden, das auf einer verknüpften Paradox-Tabelle basiert, die keinen Primärschlüssel aufweist.

Beim Erstellen oder Öffnen eines **Recordset**-Objekts besitzt jeder Datensatz bereits eine eindeutige Textmarke. Sie können die Textmarke für den aktuellen Datensatz speichern, indem Sie der Variable den Wert der **Bookmark**-Eigenschaft zuweisen. Um jederzeit schnell zu dem Datensatz zurückkehren zu können, nachdem Sie einen anderen Datensatz verschoben haben, setzen Sie die **Bookmark**-Eigenschaft des **Recordset**-Objekts auf den Wert der Variable.

Bei der Anzahl der Textmarken gibt es keine Begrenzung. Um eine Textmarke für einen anderen als den aktuellen Datensatz zu erstellen, verschieben Sie den gewünschten Datensatz und weisen Sie einer **String**-Variable den Wert der **Bookmark**-Eigenschaft zu, der den Datensatz identifiziert.

Um sicherzustellen, dass das **Recordset**-Objekt Lesezeichen unterstützt, überprüfen Sie den Wert seiner **[Bookmarkable](recordset-bookmarkable-property-dao.md)**-Eigenschaft, bevor Sie die **Bookmark**-Eigenschaft verwenden. Wenn die **Bookmarkable**-Eigenschaft „false“ ist, unterstützt das **Recordset-**-Objekt keine Lesezeichen, und die Verwendung der **Bookmark**-Eigenschaft führt zu einem abfangbaren Fehler.

Wenn Sie die **[Clone](recordset-clone-method-dao.md)**-Methode verwenden, um eine Kopie eines **Recordset**-Objekts zu erstellen, sind die **Bookmark**-Eigenschaftseinstellungen für die ursorünglichen und die duplizierten **Recordset**-Objekte identisch und austauschbar. Textmarken aus unterschiedlichen **Recordset**-Objekten sind jedoch nicht austauschbar, selbst wenn sie mit dem gleichen Objekt oder der gleichen SQL-Anweisung erstellt wurden.

Wenn Sie die **Bookmark**-Eigenschaft auf einen Wert festlegen, der einen gelöschten Datensatz darstellt, tritt ein abfangbarer Fehler auf.

Der Wert der **Bookmark**-Eigenschaft entspricht nicht einer Datensatzanzahl.

## <a name="example"></a>Beispiel

In diesem Beispiel werden die **Bookmark**- und **Bookmarkable**-Eigenschaften verwendet, damit Benutzer einen Eintrag in einem **Recordset** kennzeichnen und später zu ihm zurückkehren können.

```vb
    Sub BookmarkX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCategories As Recordset 
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

In diesem Beispiel wird die **LastModified**-Eigenschaft verwenden, um den aktuellen Datensatzzeiger zu einem geänderten und neu erstellten Datensatz zu verschieben.

```vb
    Sub LastModifiedX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
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
