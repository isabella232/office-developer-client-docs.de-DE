---
title: Recordsetpositionierung
TOCTitle: Recordset positioning
ms:assetid: 1b8b08d5-a11c-ec6e-201c-1405171a1264
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248955(v=office.15)
ms:contentKeyID: 48543546
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5116adbf68e4e98c7fbda8285348e00638465742
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946272"
---
# <a name="recordset-positioning"></a><span data-ttu-id="17f38-102">Recordsetpositionierung</span><span class="sxs-lookup"><span data-stu-id="17f38-102">Recordset positioning</span></span>


<span data-ttu-id="17f38-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="17f38-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="17f38-p101">Verwenden Sie die **AbsolutePosition** -Eigenschaft, um basierend auf der Position im **Recordset** -Objekt zu einem Datensatz zu navigieren, oder um die Position des aktuellen Datensatzes zu bestimmen. Die entsprechende Funktionalität muss vom Anbieter unterstützt werden, damit diese Eigenschaft verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="17f38-p101">Use the **AbsolutePosition** property to move to a record, based on its ordinal position in the **Recordset** object, or to determine the ordinal position of the current record. The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="17f38-p102">**AbsolutePosition** ist 1-basiert und entspricht 1, wenn der aktuelle Datensatz der erste Datensatz im **Recordset** -Objekt ist. Wie bereits weiter oben erwähnt, können Sie die Gesamtanzahl der Datensätze im **Recordset** -Objekt mit der **RecordCount** -Eigenschaft abrufen.</span><span class="sxs-lookup"><span data-stu-id="17f38-p102">**AbsolutePosition** is 1-based and equals 1 when the current record is the first record in the **Recordset**. As mentioned previously, you can obtain the total number of records in the **Recordset** object from the **RecordCount** property.</span></span>

<span data-ttu-id="17f38-p103">Wenn Sie die **AbsolutePosition** -Eigenschaft festlegen, lädt ADO, selbst wenn Sie diese Eigenschaft auf einen Datensatz im aktuellen Cache festlegen, den Cache erneut mit einer neuen Datensatzgruppe, und zwar beginnend mit dem von Ihnen angegebenen Datensatz. Die **CacheSize** -Eigenschaft bestimmt die Größe dieser Gruppe.</span><span class="sxs-lookup"><span data-stu-id="17f38-p103">When you set the **AbsolutePosition** property, even if it is to a record in the current cache, ADO reloads the cache with a new group of records starting with the record you specified. The **CacheSize** property determines the size of this group.</span></span>


> [!NOTE]
> <P><span data-ttu-id="17f38-p104">[!HINWEIS] Sie sollten die <STRONG>AbsolutePosition</STRONG> -Eigenschaft nicht als Ersatz-Datensatznummer verwenden. Die Position eines Datensatzes wird geändert, wenn Sie einen vorausgehenden Datensatz löschen. Außerdem gibt es keine Gewähr, dass ein bestimmter Datensatz den gleichen Wert für <STRONG>AbsolutePosition</STRONG> aufweist, wenn das <STRONG>Recordset</STRONG> -Objekt erneut abgefragt oder geöffnet wird. Lesezeichen sind die empfohlene Methode, um zu einer bestimmten Position zurückzukehren, und sie sind die einzige Methode der Positionierung für alle Typen von <STRONG>Recordset</STRONG> -Objekten.</span><span class="sxs-lookup"><span data-stu-id="17f38-p104">You should not use the <STRONG>AbsolutePosition</STRONG> property as a surrogate record number. The position of a given record changes when you delete a preceding record. There also is no assurance that a given record will have the same <STRONG>AbsolutePosition</STRONG> if the <STRONG>Recordset</STRONG> object is requeried or reopened. Bookmarks are the recommended way of retaining and returning to a given position and are the only way of positioning across all types of <STRONG>Recordset</STRONG> objects.</span></span></P>


