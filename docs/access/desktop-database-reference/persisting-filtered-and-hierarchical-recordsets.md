---
title: Speichern von gefiltert und hierarchische Recordsets
TOCTitle: Persisting filtered and hierarchical Recordsets
ms:assetid: 3648a997-dac7-d8a3-3cca-a6827f26a4f0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249120(v=office.15)
ms:contentKeyID: 48544162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 13255bcd5cd40745a767b8aff9f49449b0127294
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946118"
---
# <a name="persisting-filtered-and-hierarchical-recordsets"></a><span data-ttu-id="05510-102">Speichern von gefiltert und hierarchische Recordsets</span><span class="sxs-lookup"><span data-stu-id="05510-102">Persisting filtered and hierarchical Recordsets</span></span>


<span data-ttu-id="05510-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="05510-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="05510-p101">Wenn die [Filter](filter-property-ado.md)-Eigenschaft für das **Recordset** -Objekt aktiviert ist, werden nur die Zeilen gespeichert, auf die über den Filter zugegriffen werden kann. Wenn das **Recordset** -Objekt hierarchisch ist, werden das aktuelle untergeordnete **Recordset** -Objekt und dessen untergeordneten Elemente gespeichert, einschließlich des übergeordneten **Recordset** -Objekts. Falls die **Save** -Methode eines untergeordneten **Recordset** -Objekts aufgerufen wird, werden das untergeordnete Element und alle ihm untergeordneten Elemente gespeichert, das übergeordnete Element jedoch nicht. Weitere Informationen zu hierarchischen **Recordset** -Objekten finden Sie in [Kapitel 9: Datenstrukturierung](chapter-9-data-shaping.md).</span><span class="sxs-lookup"><span data-stu-id="05510-p101">If the [Filter](filter-property-ado.md) property is in effect for the **Recordset**, only the rows accessible under the filter are saved. If the **Recordset** is hierarchical, the current child **Recordset** and its children are saved, including the parent **Recordset**. If the **Save** method of a child **Recordset** is called, the child and all its children are saved, but the parent is not. For more information about hierarchical **Recordsets**, see [Chapter 9: Data Shaping](chapter-9-data-shaping.md).</span></span>


> [!NOTE]
> <span data-ttu-id="05510-p102">[!HINWEIS] Beim Speichern hierarchischer **Recordset** -Objekte (Datenstrukturen) im XML-Format gelten einige Einschränkungen. Weitere Informationen finden Sie unter [Hierarchische Recordset-Objekte in XML](hierarchical-recordsets-in-xml.md).</span><span class="sxs-lookup"><span data-stu-id="05510-p102">Some limitations apply when saving hierarchical **Recordsets** (data shapes) in XML format. For more information, see [Hierarchical Recordsets in XML](hierarchical-recordsets-in-xml.md).</span></span>


