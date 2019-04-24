---
title: Springen zu einem Datensatz
TOCTitle: Jumping to a record
ms:assetid: 27177bbe-066c-aeb0-6dfd-45d8c2a87487
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249033(v=office.15)
ms:contentKeyID: 48543829
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 08d8a3d7b3d6012867a91aa306f45872bfebb2e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290786"
---
# <a name="jumping-to-a-record"></a><span data-ttu-id="fff88-102">Springen zu einem Datensatz</span><span class="sxs-lookup"><span data-stu-id="fff88-102">Jumping to a record</span></span>


<span data-ttu-id="fff88-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fff88-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fff88-104">Mit der [Move](move-method-ado.md)-Methode können Sie im **Recordset** -Objekt mithilfe der folgenden Syntax um eine angegebene Anzahl von Datensätzen vorwärts oder rückwärts navigieren:</span><span class="sxs-lookup"><span data-stu-id="fff88-104">The [Move](move-method-ado.md) method allows you to move forward or backward in the **Recordset** a specified number of records by using the following syntax:</span></span>

```vb 
 
oRs.Move NumRecords, Start
```

<span data-ttu-id="fff88-105">Die **Move**-Methode wird für alle **Recordset**-Objekte unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fff88-105">The **Move** method is supported on all **Recordset** objects.</span></span>

<span data-ttu-id="fff88-p101">Wenn das Argument *NumRecords* größer als null ist, wird die aktuelle Datensatzposition vorwärts verschoben (zum Ende des **Recordset**-Objekts hin). Wenn *NumRecords* kleiner als null ist, wird die aktuelle Datensatzposition rückwärts verschoben (zum Anfang des **Recordset**-Objekts hin).</span><span class="sxs-lookup"><span data-stu-id="fff88-p101">If the *NumRecords* argument is greater than zero, the current record position moves forward (toward the end of the **Recordset**). If *NumRecords* is less than zero, the current record position moves backward (toward the beginning of the **Recordset**).</span></span>

<span data-ttu-id="fff88-p102">Wenn mit dem Aufruf von **Move** die aktuelle Datensatzposition vor den ersten Datensatz verschoben würde, legt ADO den aktuellen Datensatz auf die Position vor dem ersten Datensatz im **Recordset**-Objekt fest (**BOF** ist **True**). Es wird ein Fehler generiert, wenn Sie versuchen rückwärts zu navigieren, obwohl die **BOF**-Eigenschaft bereits **True** ist.</span><span class="sxs-lookup"><span data-stu-id="fff88-p102">If the **Move** call would move the current record position to a point before the first record, ADO sets the current record to the position before the first record in the **Recordset** (**BOF** is **True**). An attempt to move backward when the **BOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="fff88-p103">Wenn mit dem Aufruf von **Move** die aktuelle Datensatzposition nach dem letzten Datensatz verschoben würde, legt ADO den aktuellen Datensatz auf die Position nach dem letzten Datensatz im **Recordset**-Objekt fest (**EOF** ist **True**). Es wird ein Fehler generiert, wenn Sie versuchen vorwärts zu navigieren, obwohl die **EOF**-Eigenschaft bereits **True** ist.</span><span class="sxs-lookup"><span data-stu-id="fff88-p103">If the **Move** call would move the current record position to a point after the last record, ADO sets the current record to the position after the last record in the **Recordset** (**EOF** is **True**). An attempt to move forward when the **EOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="fff88-112">Es wird ein Fehler generiert, wenn Sie die **Move**-Methode in einem leeren **Recordset**-Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fff88-112">Calling the **Move** method from an empty **Recordset** object generates an error.</span></span>

<span data-ttu-id="fff88-p104">Wenn Sie im Argument *Start* ein Lesezeichen übergeben, erfolgt die Navigation relativ zum Datensatz mit diesem Lesezeichen, vorausgesetzt Lesezeichen werden vom **Recordset**-Objekt unterstützt. Ein Lesezeichen erstellen Sie mithilfe der [Bookmark](bookmark-property-ado.md)-Eigenschaft. Ohne Angabe erfolgt die Navigation relativ zum aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="fff88-p104">If you pass a bookmark in the *Start* argument, the move is relative to the record with this bookmark, assuming the **Recordset** object supports bookmarks. A bookmark is obtained by using the [Bookmark](bookmark-property-ado.md) property. If not specified, the move is relative to the current record.</span></span>

<span data-ttu-id="fff88-p105">Falls Sie mithilfe der **CacheSize**-Eigenschaft Datensätze vom Anbieter lokal zwischenspeichern, wird durch das Übergeben eines Arguments *NumRecords*, mit dem die aktuelle Datensatzposition außerhalb der aktuellen Gruppe zwischengespeicherter Datensätze verschoben wird, ADO gezwungen, eine neue Datensatzgruppe ausgehend vom Zieldatensatz abzurufen. Die **CacheSize**-Eigenschaft bestimmt die Größe der neu abgerufenen Gruppe, und der Zieldatensatz ist der erste abgerufene Datensatz.</span><span class="sxs-lookup"><span data-stu-id="fff88-p105">If you are using the **CacheSize** property to locally cache records from the provider, passing a *NumRecords* argument that moves the current record position outside the current group of cached records forces ADO to retrieve a new group of records, starting from the destination record. The **CacheSize** property determines the size of the newly retrieved group, and the destination record is the first record retrieved.</span></span>

