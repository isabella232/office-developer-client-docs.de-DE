---
title: Recordset.Bookmarkable Property (DAO)
TOCTitle: Bookmarkable Property
ms:assetid: 6323f162-75c4-7cfe-c918-0b9454560f97
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194950(v=office.15)
ms:contentKeyID: 48545257
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8eca86433098256128dc78cb1c2cf6fd8b87ec6c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889196"
---
# <a name="recordsetbookmarkable-property-dao"></a><span data-ttu-id="e1d15-102">Recordset.Bookmarkable Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="e1d15-102">Recordset.Bookmarkable Property (DAO)</span></span>


<span data-ttu-id="e1d15-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e1d15-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e1d15-104">Gibt einen Wert zurück, der angibt, ob ein **Recordset**-Objekt Textmarken unterstützt, die Sie mithilfe der **[Bookmark](recordset-bookmark-property-dao.md)** -Eigenschaft festlegen können.</span><span class="sxs-lookup"><span data-stu-id="e1d15-104">Returns a value that indicates whether a **Recordset** object supports bookmarks, which you can set by using the **[Bookmark](recordset-bookmark-property-dao.md)** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1d15-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1d15-105">Syntax</span></span>

<span data-ttu-id="e1d15-106">*Ausdruck* . Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="e1d15-106">*expression* .Bookmarkable</span></span>

<span data-ttu-id="e1d15-107">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="e1d15-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1d15-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1d15-108">Remarks</span></span>

<span data-ttu-id="e1d15-109">Überprüfen Sie die Einstellung der **Bookmarkable**-Eigenschaft eines **Recordset**-Objekts, bevor Sie versuchen, die **Bookmark**-Eigenschaft festzulegen oder zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e1d15-109">Check the **Bookmarkable** property setting of a **Recordset** object before you attempt to set or check the **Bookmark** property.</span></span>

<span data-ttu-id="e1d15-110">**Recordset** -Objekte, die vollständig auf Tabellen des Microsoft Access-Datenbankmoduls basiert der Wert der **Bookmarkable** -Eigenschaft ist True, und Sie Lesezeichen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="e1d15-110">For **Recordset** objects based entirely on Microsoft Access database engine tables, the value of the **Bookmarkable** property is True, and you can use bookmarks.</span></span> <span data-ttu-id="e1d15-111">Andere Datenbank-Produkte unterstützen Textmarken möglicherweise nicht.</span><span class="sxs-lookup"><span data-stu-id="e1d15-111">Other database products may not support bookmarks, however.</span></span> <span data-ttu-id="e1d15-112">Sie können Textmarken nicht in beliebigen **Recordset** -Objekten verwenden, die auf einer verknüpften Paradox-Tabelle basieren, die keinen primären Schlüssel besitzt.</span><span class="sxs-lookup"><span data-stu-id="e1d15-112">For example, you can't use bookmarks in any **Recordset** object based on a linked Paradox table that has no primary key.</span></span>

## <a name="example"></a><span data-ttu-id="e1d15-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e1d15-113">Example</span></span>

<span data-ttu-id="e1d15-114">In diesem Beispiel werden die Eigenschaften **Bookmark** und **Bookmarkable** verwendet, damit der Benutzer einen Datensatz in einem **Recordset**-Objekt kennzeichnen und später zu diesem zurückkehren kann.</span><span class="sxs-lookup"><span data-stu-id="e1d15-114">This example uses the **Bookmark** and **Bookmarkable** properties to let the user flag a record in a **Recordset** and return to it later.</span></span>

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
