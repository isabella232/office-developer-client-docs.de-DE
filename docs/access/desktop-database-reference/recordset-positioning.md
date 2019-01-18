---
title: Positionieren von Recordsets
TOCTitle: Recordset positioning
ms:assetid: 1b8b08d5-a11c-ec6e-201c-1405171a1264
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248955(v=office.15)
ms:contentKeyID: 48543546
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cffb5adce1266bd7fdd08989e9f92110f4829ba0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718536"
---
# <a name="recordset-positioning"></a><span data-ttu-id="98a42-102">Positionieren von Recordsets</span><span class="sxs-lookup"><span data-stu-id="98a42-102">Recordset positioning</span></span>

<span data-ttu-id="98a42-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="98a42-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="98a42-p101">Verwenden Sie die **AbsolutePosition** -Eigenschaft, um basierend auf der Position im **Recordset** -Objekt zu einem Datensatz zu navigieren, oder um die Position des aktuellen Datensatzes zu bestimmen. Die entsprechende Funktionalität muss vom Anbieter unterstützt werden, damit diese Eigenschaft verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="98a42-p101">Use the **AbsolutePosition** property to move to a record, based on its ordinal position in the **Recordset** object, or to determine the ordinal position of the current record. The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="98a42-p102">**AbsolutePosition** ist 1-basiert und entspricht 1, wenn der aktuelle Datensatz der erste Datensatz im **Recordset** -Objekt ist. Wie bereits weiter oben erwähnt, können Sie die Gesamtanzahl der Datensätze im **Recordset** -Objekt mit der **RecordCount** -Eigenschaft abrufen.</span><span class="sxs-lookup"><span data-stu-id="98a42-p102">**AbsolutePosition** is 1-based and equals 1 when the current record is the first record in the **Recordset**. As mentioned previously, you can obtain the total number of records in the **Recordset** object from the **RecordCount** property.</span></span>

<span data-ttu-id="98a42-p103">Wenn Sie die **AbsolutePosition** -Eigenschaft festlegen, lädt ADO, selbst wenn Sie diese Eigenschaft auf einen Datensatz im aktuellen Cache festlegen, den Cache erneut mit einer neuen Datensatzgruppe, und zwar beginnend mit dem von Ihnen angegebenen Datensatz. Die **CacheSize** -Eigenschaft bestimmt die Größe dieser Gruppe.</span><span class="sxs-lookup"><span data-stu-id="98a42-p103">When you set the **AbsolutePosition** property, even if it is to a record in the current cache, ADO reloads the cache with a new group of records starting with the record you specified. The **CacheSize** property determines the size of this group.</span></span>

> [!NOTE]
> <span data-ttu-id="98a42-p104">[!HINWEIS] Sie sollten die **AbsolutePosition** -Eigenschaft nicht als Ersatz-Datensatznummer verwenden. Die Position eines Datensatzes wird geändert, wenn Sie einen vorausgehenden Datensatz löschen. Außerdem gibt es keine Gewähr, dass ein bestimmter Datensatz den gleichen Wert für **AbsolutePosition** aufweist, wenn das **Recordset** -Objekt erneut abgefragt oder geöffnet wird. Lesezeichen sind die empfohlene Methode, um zu einer bestimmten Position zurückzukehren, und sie sind die einzige Methode der Positionierung für alle Typen von **Recordset** -Objekten.</span><span class="sxs-lookup"><span data-stu-id="98a42-p104">You should not use the **AbsolutePosition** property as a surrogate record number. The position of a given record changes when you delete a preceding record. There also is no assurance that a given record will have the same **AbsolutePosition** if the **Recordset** object is requeried or reopened. Bookmarks are the recommended way of retaining and returning to a given position and are the only way of positioning across all types of **Recordset** objects.</span></span>


