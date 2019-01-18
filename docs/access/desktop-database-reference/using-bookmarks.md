---
title: Verwenden von Lesezeichen (Access PC-Datenbank-Referenz)
TOCTitle: Using Bookmarks
ms:assetid: fe6333ef-c9d9-1e84-2252-d27edc676e97
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250306(v=office.15)
ms:contentKeyID: 48548935
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 469d8a0cc9b644fe434770d51c21d8210c8038d0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706320"
---
# <a name="using-bookmarks"></a><span data-ttu-id="18d7c-102">Verwenden von Lesezeichen</span><span class="sxs-lookup"><span data-stu-id="18d7c-102">Using bookmarks</span></span>


<span data-ttu-id="18d7c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="18d7c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="18d7c-p101">Beim Navigieren im **Recordset** -Objekt ist es oft hilfreich, wenn Sie direkt zu einem bestimmten Datensatz zurückkehren können, ohne dass Sie einen Bildlauf in allen Datensätzen ausführen und Werte vergleichen müssen. Wenn Sie z. B. mit der **Find** -Methode nach einem Datensatz suchen, die Suche aber keine Datensätze zurückgibt, wird automatisch das Ende des **Recordset** -Objekts angezeigt. Wenn Lesezeichen von Ihrem Anbieter unterstützt werden, können Sie mithilfe von Lesezeichen die Position markieren, bevor Sie die **Find** -Methode verwenden, damit Sie zu dieser Position zurückkehren können. Ein Lesezeichen ist ein Wert vom Datentyp **Variant**, mit dem ein Datensatz in einem **Recordset** -Objekt eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="18d7c-p101">It is often useful to return directly to a specific record after having moved around in the **Recordset** without having to scroll through every record and compare values. For example, if you attempt to search for a record using the **Find** method but the search returns no records, you are automatically placed at either end of the **Recordset**. If your provider supports them, bookmarks can be used to mark your place before using the **Find** method so you can return to your location. A bookmark is a **Variant** type value that uniquely identifies a record in a **Recordset** object.</span></span>

<span data-ttu-id="18d7c-108">Sie können auch ein variant-Array von Lesezeichen mit der **Filter** -Methode des **Recordset-Objekts** verwenden, um eine ausgewählte Reihe von Datensätze zu filtern.</span><span class="sxs-lookup"><span data-stu-id="18d7c-108">You can also use a variant array of bookmarks with the **Recordset** **Filter** method to filter on a selected set of records.</span></span> <span data-ttu-id="18d7c-109">Ausführliche Informationen zu diesem Verfahren finden Sie unter Filtern der Ergebnisse im Thema, [Arbeiten mit Recordsets](working-with-recordsets.md), weiter unten in diesem Kapitel.</span><span class="sxs-lookup"><span data-stu-id="18d7c-109">For details about this technique, see Filtering the Results in the topic, [Working with Recordsets](working-with-recordsets.md), later in this chapter.</span></span>

<span data-ttu-id="18d7c-p103">Mit der **Bookmark** -Eigenschaft können Sie ein Lesezeichen für einen Datensatz abrufen oder den aktuellen Datensatz in einem **Recordset** -Objekt auf den durch ein gültiges Lesezeichen identifizierten Datensatz festlegen. Im folgenden Code wird mithilfe der **Bookmark** -Eigenschaft ein Lesezeichen festgelegt und anschließend nach dem Navigieren in anderen Datensätzen zu dem Datensatz mit dem Lesezeichen zurückgekehrt. Verwenden Sie die **Supports** -Methode, um zu ermitteln, ob das **Recordset** -Objekt Lesezeichen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="18d7c-p103">You can use the **Bookmark** property to get a bookmark for a record, or set the current record in a **Recordset** object to the record identified by a valid bookmark. The following code uses the **Bookmark** property to set a bookmark and then return to the bookmarked record after moving on to other records. To determine if your **Recordset** supports bookmarks, use the **Supports** method.</span></span>

```vb 
 
'BeginBookmarkEg 
 Dim varBookmark As Variant 
 Dim blnCanBkmrk As Boolean 
 
 objRs.Open strSQL, strConnStr, adOpenStatic, adLockOptimistic, adCmdText 
 
 If objRs.RecordCount > 4 Then 
 objRs.Move 4 ' move to the fifth record 
 blnCanBkmrk = objRs.Supports(adBookmark) 
 If blnCanBkmrk = True Then 
 varBookmark = objRs.Bookmark ' record the bookmark 
 objRs.MoveLast ' move to a different record 
 objRs.Bookmark = varBookmark ' return to the bookmarked (sixth) record 
 End If 
 End If 
'EndBookmarkEg 
```

<span data-ttu-id="18d7c-113">Die [Supports](supports-method-ado.md)-Methode wird weiter unten ausführlicher behandelt.</span><span class="sxs-lookup"><span data-stu-id="18d7c-113">The [Supports](supports-method-ado.md) method is covered in more detail later.</span></span>

<span data-ttu-id="18d7c-p104">Mit Ausnahme geklonter **Recordset** -Objekte sind Lesezeichen für das **Recordset** -Objekt, in dem sie erstellt wurden, eindeutig, selbst wenn derselbe Befehl verwendet wird. Das heißt, Sie können mit einer bestimmten **Bookmark** -Eigenschaft eines **Recordset** -Objekts nicht zum gleichen Datensatz in einem zweiten **Recordset** -Objekt navigieren, das mit dem gleichen Befehl geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="18d7c-p104">Except for the case of cloned **Recordsets**, bookmarks are unique to the **Recordset** in which they were created, even if the same command is used. This means that you cannot use a **Bookmark** obtained from one **Recordset** to move to the same record in a second **Recordset** opened with the same command.</span></span>

