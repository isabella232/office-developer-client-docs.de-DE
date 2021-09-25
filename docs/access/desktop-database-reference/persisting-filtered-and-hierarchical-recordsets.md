---
title: Speichern von gefilterten und hierarchischen Recordsets
TOCTitle: Persisting filtered and hierarchical Recordsets
ms:assetid: 3648a997-dac7-d8a3-3cca-a6827f26a4f0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249120(v=office.15)
ms:contentKeyID: 48544162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9da0cb3e06be240a9782c8fec1e537216290ae2b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581007"
---
# <a name="persisting-filtered-and-hierarchical-recordsets"></a>Speichern von gefilterten und hierarchischen Recordsets


**Gilt für**: Access 2013, Office 2013

Wenn die [Filter](filter-property-ado.md)-Eigenschaft für das **Recordset** -Objekt aktiviert ist, werden nur die Zeilen gespeichert, auf die über den Filter zugegriffen werden kann. Wenn das **Recordset** -Objekt hierarchisch ist, werden das aktuelle untergeordnete **Recordset** -Objekt und dessen untergeordneten Elemente gespeichert, einschließlich des übergeordneten **Recordset** -Objekts. Falls die **Save** -Methode eines untergeordneten **Recordset** -Objekts aufgerufen wird, werden das untergeordnete Element und alle ihm untergeordneten Elemente gespeichert, das übergeordnete Element jedoch nicht. Weitere Informationen zu hierarchischen **Recordset** -Objekten finden Sie in [Kapitel 9: Datenstrukturierung](chapter-9-data-shaping.md).


> [!NOTE]
> [!HINWEIS] Beim Speichern hierarchischer **Recordset** -Objekte (Datenstrukturen) im XML-Format gelten einige Einschränkungen. Weitere Informationen finden Sie unter [Hierarchische Recordset-Objekte in XML](hierarchical-recordsets-in-xml.md).


