---
title: Recordset2.Bookmark-Eigenschaft (DAO)
TOCTitle: Bookmark Property
ms:assetid: 7366d550-2f72-ed10-b230-eb144a6f874b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195857(v=office.15)
ms:contentKeyID: 48545637
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 306962eda3430a1797cf79dc04a34d2e55e9daf8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930973"
---
# <a name="recordset2bookmark-property-dao"></a><span data-ttu-id="409fb-102">Recordset2.Bookmark-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="409fb-102">Recordset2.Bookmark property (DAO)</span></span>


<span data-ttu-id="409fb-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="409fb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="409fb-104">Legt ein Lesezeichen fest, das den aktuellen Datensatz in einem **Recordset**-Objekt eindeutig identifiziert, oder gibt das Lesezeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="409fb-104">Sets or returns a bookmark that uniquely identifies the current record in a **Recordset** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="409fb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="409fb-105">Syntax</span></span>

<span data-ttu-id="409fb-106">*Ausdruck* . Lesezeichen</span><span class="sxs-lookup"><span data-stu-id="409fb-106">*expression* .Bookmark</span></span>

<span data-ttu-id="409fb-107">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="409fb-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="409fb-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="409fb-108">Remarks</span></span>

<span data-ttu-id="409fb-109">Für ein **Recordset** -Objekt vollständig auf Tabellen des Microsoft Access-Datenbankmoduls basiert der Wert der **Bookmarkable** -Eigenschaft True ist, und können Sie die **Bookmark** -Eigenschaft Recordset verwenden.</span><span class="sxs-lookup"><span data-stu-id="409fb-109">For a **Recordset** object based entirely on Microsoft Access database engine tables, the value of the **Bookmarkable** property is True, and you can use the **Bookmark** property with that recordset.</span></span> <span data-ttu-id="409fb-110">Andere Datenbank-Produkte unterstützen Textmarken möglicherweise nicht.</span><span class="sxs-lookup"><span data-stu-id="409fb-110">Other database products may not support bookmarks, however.</span></span> <span data-ttu-id="409fb-111">Beispielsweise können nicht verwenden Sie Textmarken in eine beliebige **Recordset2** -Objekt basierend auf einer verknüpften Paradox-Tabelle, die ohne Primärschlüssel.</span><span class="sxs-lookup"><span data-stu-id="409fb-111">For example, you can't use bookmarks in any **Recordset2** object based on a linked Paradox table that has no primary key.</span></span>

<span data-ttu-id="409fb-p102">Beim Erstellen oder Öffnen eines **Recordset** -Objekts besitzt jeder Datensatz bereits eine eindeutige Textmarke. Sie können die Textmarke für den aktuellen Datensatz speichern, indem Sie der Variable den Wert der **Bookmark** -Eigenschaft zuweisen. Um jederzeit schnell zu dem Datensatz zurückkehren zu können, nachdem Sie einen anderen Datensatz verschoben haben, setzen Sie die **Bookmark** -Eigenschaft des **Recordset** -Objekts auf den Wert der Variable.</span><span class="sxs-lookup"><span data-stu-id="409fb-p102">When you create or open a **Recordset** object, each of its records already has a unique bookmark. You can save the bookmark for the current record by assigning the value of the **Bookmark** property to a variable. To quickly return to that record at any time after moving to a different record, set the **Recordset** object's **Bookmark** property to the value of that variable.</span></span>

<span data-ttu-id="409fb-p103">Bei der Anzahl der Textmarken gibt es keine Begrenzung. Um eine Textmarke für einen anderen als den aktuellen Datensatz zu erstellen, verschieben Sie den gewünschten Datensatz und weisen Sie einer **String** -Variable den Wert der **Bookmark** -Eigenschaft zu, der den Datensatz identifiziert.</span><span class="sxs-lookup"><span data-stu-id="409fb-p103">There is no limit to the number of bookmarks you can establish. To create a bookmark for a record other than the current record, move to the desired record and assign the value of the **Bookmark** property to a **String** variable that identifies the record.</span></span>

<span data-ttu-id="409fb-117">Um sicherzustellen, dass das **Recordset** -Objekt Textmarken unterstützt, überprüfen Sie den Wert der **[Bookmarkable](recordset2-bookmarkable-property-dao.md)** -Eigenschaft, bevor Sie die **Bookmark** -Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="409fb-117">To make sure the **Recordset** object supports bookmarks, check the value of its **[Bookmarkable](recordset2-bookmarkable-property-dao.md)** property before you use the **Bookmark** property.</span></span> <span data-ttu-id="409fb-118">Wenn die **Bookmarkable** -Eigenschaft auf false festgelegt ist, das **Recordset** -Objekt Lesezeichen unterstützt keine und ein auffangbarer Fehler mithilfe der **Bookmark** -Eigenschaft erzeugt.</span><span class="sxs-lookup"><span data-stu-id="409fb-118">If the **Bookmarkable** property is False, the **Recordset** object doesn't support bookmarks, and using the **Bookmark** property results in a trappable error.</span></span>

<span data-ttu-id="409fb-p105">Wenn Sie die **[Clone](recordset2-clone-method-dao.md)** -Methode verwenden, um eine Kopie eines **Recordset** -Objekts zu erstellen, sind die **Bookmark** -Eigenschaftseinstellungen für die ursorünglichen und die duplizierten **Recordset** -Objekte identisch und austauschbar. Textmarken aus unterschiedlichen **Recordset** -Objekten sind jedoch nicht austauschbar, selbst wenn sie mit dem gleichen Objekt oder der gleichen SQL-Anweisung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="409fb-p105">If you use the **[Clone](recordset2-clone-method-dao.md)** method to create a copy of a **Recordset** object, the **Bookmark** property settings for the original and the duplicate **Recordset** objects are identical and can be used interchangeably. However, you can't use bookmarks from different **Recordset** objects interchangeably, even if they were created by using the same object or the same SQL statement.</span></span>

<span data-ttu-id="409fb-121">Wenn Sie die **Bookmark** -Eigenschaft auf einen Wert festlegen, der einen gelöschten Datensatz darstellt, tritt ein abfangbarer Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="409fb-121">If you set the **Bookmark** property to a value that represents a deleted record, a trappable error occurs.</span></span>

<span data-ttu-id="409fb-122">Der Wert der **Bookmark** -Eigenschaft entspricht nicht einer Datensatzanzahl.</span><span class="sxs-lookup"><span data-stu-id="409fb-122">The value of the **Bookmark** property isn't the same as a record number.</span></span>

## <a name="example"></a><span data-ttu-id="409fb-123">Beispiel</span><span class="sxs-lookup"><span data-stu-id="409fb-123">Example</span></span>

<span data-ttu-id="409fb-124">In diesem Beispiel werden die Eigenschaften **Bookmark** und **Bookmarkable** verwendet, damit der Benutzer einen Datensatz in einer Datensatzgruppe kennzeichnen und später zu ihm zurückkehren kann.</span><span class="sxs-lookup"><span data-stu-id="409fb-124">This example uses the **Bookmark** and **Bookmarkable** properties to let the user flag a record in a recordset and return to it later.</span></span>

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

<span data-ttu-id="409fb-125">In diesem Beispiel wird die **LastModified**-Eigenschaft verwendet, um den aktuellen Datensatzzeiger auf einen geänderten Datensatz sowie auf einen neu erstellten Datensatz zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="409fb-125">This example uses the **LastModified** property to move the current record pointer to both a record that has been modified and a newly created record.</span></span>

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
