---
title: Speichern von gefilterten und hierarchischen Recordsets
TOCTitle: Persisting filtered and hierarchical Recordsets
ms:assetid: 3648a997-dac7-d8a3-3cca-a6827f26a4f0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249120(v=office.15)
ms:contentKeyID: 48544162
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1332d4348c993f94d8b2ee61280b8b35c02324c4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28725945"
---
# <a name="persisting-filtered-and-hierarchical-recordsets"></a>Speichern von gefilterten und hierarchischen Recordsets


**Betrifft**: Access 2013, Office 2013

Wenn die [Filter](filter-property-ado.md)-Eigenschaft für das **Recordset** -Objekt aktiviert ist, werden nur die Zeilen gespeichert, auf die über den Filter zugegriffen werden kann. Wenn das **Recordset** -Objekt hierarchisch ist, werden das aktuelle untergeordnete **Recordset** -Objekt und dessen untergeordneten Elemente gespeichert, einschließlich des übergeordneten **Recordset** -Objekts. Falls die **Save** -Methode eines untergeordneten **Recordset** -Objekts aufgerufen wird, werden das untergeordnete Element und alle ihm untergeordneten Elemente gespeichert, das übergeordnete Element jedoch nicht. Weitere Informationen zu hierarchischen **Recordset** -Objekten finden Sie in [Kapitel 9: Datenstrukturierung](chapter-9-data-shaping.md).


> [!NOTE]
> [!HINWEIS] Beim Speichern hierarchischer **Recordset** -Objekte (Datenstrukturen) im XML-Format gelten einige Einschränkungen. Weitere Informationen finden Sie unter [Hierarchische Recordset-Objekte in XML](hierarchical-recordsets-in-xml.md).


