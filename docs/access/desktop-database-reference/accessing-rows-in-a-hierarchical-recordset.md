---
title: Zugreifen auf Zeilen in einem hierarchischen Recordset
TOCTitle: Accessing rows in a hierarchical Recordset
ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15)
ms:contentKeyID: 48548104
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a80b089fa72ef01eb1b4b2f1dae494e002c6a6fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281956"
---
# <a name="accessing-rows-in-a-hierarchical-recordset"></a><span data-ttu-id="a9a6a-102">Zugreifen auf Zeilen in einem hierarchischen Recordset</span><span class="sxs-lookup"><span data-stu-id="a9a6a-102">Accessing rows in a hierarchical Recordset</span></span>

<span data-ttu-id="a9a6a-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9a6a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a9a6a-104">Das folgende Beispiel zeigt die notwendigen Schritte zum Zugreifen auf Zeilen in einem hierarchischen [Recordset](recordset-object-ado.md):</span><span class="sxs-lookup"><span data-stu-id="a9a6a-104">The following example shows the steps necessary to access rows in a hierarchical [Recordset](recordset-object-ado.md):</span></span>

1. <span data-ttu-id="a9a6a-105">**Recordset** objects from the authors and titleauthor tables are related by author ID.</span><span class="sxs-lookup"><span data-stu-id="a9a6a-105">**Recordset** objects from the authors and titleauthor tables are related by author ID.</span></span>

2. <span data-ttu-id="a9a6a-106">In der äußeren Schleife werden der Vor- und Nachname, der Status und die Identifikation jedes Autors angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a9a6a-106">The outer loop displays each author's first and last name, state, and identification.</span></span>

3. <span data-ttu-id="a9a6a-107">Das angefügte **Recordset** für jede Zeile wird aus der **Fields**-Auflistung abgerufen und *rstTitleAuthor* zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="a9a6a-107">The appended **Recordset** for each row is retrieved from the **Fields** collection and assigned to *rstTitleAuthor*.</span></span>

4. <span data-ttu-id="a9a6a-108">In der inneren Schleife werden vier Felder aus jeder Zeile im angefügten **Recordset** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a9a6a-108">The inner loop displays four fields from each row in the appended **Recordset**.</span></span>

> [!NOTE] 
> <span data-ttu-id="a9a6a-109">Die [StayInSync](stayinsync-property-ado.md) -Eigenschaft ist für Zwecke der Illustration auf false festgelegt, sodass Sie die Kapitel Änderung explizit in jeder Iteration der äußeren Schleife sehen können.</span><span class="sxs-lookup"><span data-stu-id="a9a6a-109">The [StayInSync](stayinsync-property-ado.md) property is set to FALSE for purposes of illustration, so you can see the chapter change explicitly in each iteration of the outer loop.</span></span> <span data-ttu-id="a9a6a-110">Das Beispiel ist jedoch effizienter, wenn die Zuweisung in Schritt 3 vor die erste Zeile in Schritt 2 verschoben wird, sodass die Zuweisung nur ein Mal ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9a6a-110">However, the example will be more efficient if the assignment in step 3 is moved before the first line in step 2, so that the assignment is performed only once.</span></span> <span data-ttu-id="a9a6a-111">Legen Sie die **StayInSync** -Eigenschaft auf true fest, sodass *rstTitleAuthor* implizit und automatisch in das entsprechende Kapitel wechselt, wenn *RST* zu einer neuen Zeile wechselt.</span><span class="sxs-lookup"><span data-stu-id="a9a6a-111">Set the **StayInSync** property to TRUE, so that *rstTitleAuthor* will implicitly and automatically change to the corresponding chapter whenever *rst* moves to a new row.</span></span>

<span data-ttu-id="a9a6a-112">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="a9a6a-112">**Example**</span></span>

```vb 
 
Sub datashape() 
 Dim cnn As New ADODB.Connection 
 Dim rst As New ADODB.Recordset 
 Dim rstTitleAuthor As New ADODB.Recordset 
 
 cnn.Provider = "MSDataShape" 
 cnn.Open "Data Provider=MSDASQL;" & _ 
 "Data Source=SRV;" & _ 
 "User Id=MyUserName;Password=MyPassword;Database=Pubs" 
' STEP 1 
 rst.StayInSync = FALSE 
 rst.Open "SHAPE {select * from authors} " & _ 
 "APPEND ({select * from titleauthor} " & _ 
 "RELATE au_id TO au_id) AS chapTitleAuthor", _ 
 cnn 
' STEP 2 
 While Not rst.EOF 
 Debug.Print rst("au_fname"), rst("au_lname"), _ 
 rst("state"), rst("au_id") 
' STEP 3 
 Set rstTitleAuthor = rst("chapTitleAuthor").Value 
' STEP 4 
 While Not rstTitleAuthor.EOF 
 Debug.Print rstTitleAuthor(0), rstTitleAuthor(1), _ 
 rstTitleAuthor(2), rstTitleAuthor(3) 
 rstTitleAuthor.MoveNext 
 Wend 
 rst.MoveNext 
 Wend 
End Sub 
```

