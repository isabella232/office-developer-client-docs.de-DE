---
title: Verwenden von Lesezeichen (Access-Desktopdatenbankreferenz)
TOCTitle: Using Bookmarks
ms:assetid: fe6333ef-c9d9-1e84-2252-d27edc676e97
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250306(v=office.15)
ms:contentKeyID: 48548935
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b7291c1fd3fa63e20b5ac3a098884e0c4fd0ec6e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588931"
---
# <a name="using-bookmarks"></a>Verwenden von Lesezeichen


**Gilt für**: Access 2013, Office 2013

Beim Navigieren im **Recordset** -Objekt ist es oft hilfreich, wenn Sie direkt zu einem bestimmten Datensatz zurückkehren können, ohne dass Sie einen Bildlauf in allen Datensätzen ausführen und Werte vergleichen müssen. Wenn Sie z. B. mit der **Find** -Methode nach einem Datensatz suchen, die Suche aber keine Datensätze zurückgibt, wird automatisch das Ende des **Recordset** -Objekts angezeigt. Wenn Lesezeichen von Ihrem Anbieter unterstützt werden, können Sie mithilfe von Lesezeichen die Position markieren, bevor Sie die **Find** -Methode verwenden, damit Sie zu dieser Position zurückkehren können. Ein Lesezeichen ist ein Wert vom Datentyp **Variant**, mit dem ein Datensatz in einem **Recordset** -Objekt eindeutig identifiziert wird.

You can also use a variant array of bookmarks with the **Recordset** **Filter** method to filter on a selected set of records. For details about this technique, see Filtering the Results in the topic, [Working with Recordsets](working-with-recordsets.md), later in this chapter.

Mit der **Bookmark** -Eigenschaft können Sie ein Lesezeichen für einen Datensatz abrufen oder den aktuellen Datensatz in einem **Recordset** -Objekt auf den durch ein gültiges Lesezeichen identifizierten Datensatz festlegen. Im folgenden Code wird mithilfe der **Bookmark** -Eigenschaft ein Lesezeichen festgelegt und anschließend nach dem Navigieren in anderen Datensätzen zu dem Datensatz mit dem Lesezeichen zurückgekehrt. Verwenden Sie die **Supports** -Methode, um zu ermitteln, ob das **Recordset** -Objekt Lesezeichen unterstützt.

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

Die [Supports](supports-method-ado.md)-Methode wird weiter unten ausführlicher behandelt.

Mit Ausnahme geklonter **Recordset** -Objekte sind Lesezeichen für das **Recordset** -Objekt, in dem sie erstellt wurden, eindeutig, selbst wenn derselbe Befehl verwendet wird. Das heißt, Sie können mit einer bestimmten **Bookmark** -Eigenschaft eines **Recordset** -Objekts nicht zum gleichen Datensatz in einem zweiten **Recordset** -Objekt navigieren, das mit dem gleichen Befehl geöffnet wurde.

