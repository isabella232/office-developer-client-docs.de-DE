---
title: Springen zu einem Datensatz
TOCTitle: Jumping to a Record
ms:assetid: 27177bbe-066c-aeb0-6dfd-45d8c2a87487
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249033(v=office.15)
ms:contentKeyID: 48543829
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c88c7c5643559dabf3304863417c526a9fd15354
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873271"
---
# <a name="jumping-to-a-record"></a><span data-ttu-id="a9d80-102">Springen zu einem Datensatz</span><span class="sxs-lookup"><span data-stu-id="a9d80-102">Jumping to a Record</span></span>


<span data-ttu-id="a9d80-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9d80-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a9d80-104">Mit der [Move](move-method-ado.md)-Methode können Sie im **Recordset** -Objekt mithilfe der folgenden Syntax um eine angegebene Anzahl von Datensätzen vorwärts oder rückwärts navigieren:</span><span class="sxs-lookup"><span data-stu-id="a9d80-104">The [Move](move-method-ado.md) method allows you to move forward or backward in the **Recordset** a specified number of records by using the following syntax:</span></span>

```vb 
 
oRs.Move NumRecords, Start
```

<span data-ttu-id="a9d80-105">Die **Move** -Methode wird für alle **Recordset** -Objekte unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a9d80-105">The **Move** method is supported on all **Recordset** objects.</span></span>

<span data-ttu-id="a9d80-p101">Wenn das Argument *NumRecords* größer als null ist, wird die aktuelle Datensatzposition vorwärts verschoben (zum Ende des **Recordset**-Objekts hin). Wenn *NumRecords* kleiner als null ist, wird die aktuelle Datensatzposition rückwärts verschoben (zum Anfang des **Recordset**-Objekts hin).</span><span class="sxs-lookup"><span data-stu-id="a9d80-p101">If the *NumRecords* argument is greater than zero, the current record position moves forward (toward the end of the **Recordset**). If *NumRecords* is less than zero, the current record position moves backward (toward the beginning of the **Recordset**).</span></span>

<span data-ttu-id="a9d80-p102">Wenn mit dem Aufruf von **Move** die aktuelle Datensatzposition vor den ersten Datensatz verschoben würde, legt ADO den aktuellen Datensatz auf die Position vor dem ersten Datensatz im **Recordset**-Objekt fest (**BOF** ist **True**). Es wird ein Fehler generiert, wenn Sie versuchen rückwärts zu navigieren, obwohl die **BOF**-Eigenschaft bereits **True** ist.</span><span class="sxs-lookup"><span data-stu-id="a9d80-p102">If the **Move** call would move the current record position to a point before the first record, ADO sets the current record to the position before the first record in the **Recordset** (**BOF** is **True**). An attempt to move backward when the **BOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="a9d80-p103">Wenn mit dem Aufruf von **Move** die aktuelle Datensatzposition nach dem letzten Datensatz verschoben würde, legt ADO den aktuellen Datensatz auf die Position nach dem letzten Datensatz im **Recordset**-Objekt fest (**EOF** ist **True**). Es wird ein Fehler generiert, wenn Sie versuchen vorwärts zu navigieren, obwohl die **EOF**-Eigenschaft bereits **True** ist.</span><span class="sxs-lookup"><span data-stu-id="a9d80-p103">If the **Move** call would move the current record position to a point after the last record, ADO sets the current record to the position after the last record in the **Recordset** (**EOF** is **True**). An attempt to move forward when the **EOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="a9d80-112">Beim Aufrufen der **Move** -Methode aus einem leeren **Recordset** -Objekt wird ein Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="a9d80-112">Calling the **Move** method from an empty **Recordset** object generates an error.</span></span>

<span data-ttu-id="a9d80-113">Wenn Sie eine Textmarke in das Argument *Start* übergeben, ist die Verschiebung relativ zum Datensatz mit diesem Lesezeichen, vorausgesetzt, dass das **Recordset** -Objekt Lesezeichen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a9d80-113">If you pass a bookmark in the *Start* argument, the move is relative to the record with this bookmark, assuming the **Recordset** object supports bookmarks.</span></span> <span data-ttu-id="a9d80-114">Ein Lesezeichen erstellen Sie mithilfe der [Bookmark](bookmark-property-ado.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a9d80-114">A bookmark is obtained by using the [Bookmark](bookmark-property-ado.md) property.</span></span> <span data-ttu-id="a9d80-115">Ohne Angabe erfolgt die Navigation relativ zum aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="a9d80-115">If not specified, the move is relative to the current record.</span></span>

<span data-ttu-id="a9d80-116">Bei Verwendung die **CacheSize** -Eigenschaft auf lokal Cache Datensätze aus der Anbieter auf und übergibt ein *NumRecords* -Argument, das die aktuelle Datensatzposition außerhalb der aktuellen Gruppe der zwischengespeicherten Datensätze verschiebt erzwingt, dass ADO Abrufen einer neuen Gruppe von Datensätzen, Starten aus dem Zieldatensatz.</span><span class="sxs-lookup"><span data-stu-id="a9d80-116">If you are using the **CacheSize** property to locally cache records from the provider, passing a *NumRecords* argument that moves the current record position outside the current group of cached records forces ADO to retrieve a new group of records, starting from the destination record.</span></span> <span data-ttu-id="a9d80-117">Die **CacheSize** -Eigenschaft bestimmt die Größe der neu abgerufenen Gruppe, und der Zieldatensatz ist der erste abgerufene Datensatz.</span><span class="sxs-lookup"><span data-stu-id="a9d80-117">The **CacheSize** property determines the size of the newly retrieved group, and the destination record is the first record retrieved.</span></span>

