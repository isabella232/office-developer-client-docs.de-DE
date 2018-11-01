---
title: Speichern gefilterter und hierarchischer Recordset-Objekte
TOCTitle: Persisting Filtered and Hierarchical Recordsets
ms:assetid: 3648a997-dac7-d8a3-3cca-a6827f26a4f0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249120(v=office.15)
ms:contentKeyID: 48544162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 931345aff0cd3d8c9b10c53073e640b3cfdd5de5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889714"
---
# <a name="persisting-filtered-and-hierarchical-recordsets"></a>Speichern gefilterter und hierarchischer Recordset-Objekte


**Betrifft**: Access 2013, Office 2013

Wenn die [Filter](filter-property-ado.md)-Eigenschaft für das **Recordset** -Objekt aktiviert ist, werden nur die Zeilen gespeichert, auf die über den Filter zugegriffen werden kann. Wenn das **Recordset** -Objekt hierarchisch ist, werden das aktuelle untergeordnete **Recordset** -Objekt und dessen untergeordneten Elemente gespeichert, einschließlich des übergeordneten **Recordset** -Objekts. Falls die **Save** -Methode eines untergeordneten **Recordset** -Objekts aufgerufen wird, werden das untergeordnete Element und alle ihm untergeordneten Elemente gespeichert, das übergeordnete Element jedoch nicht. Weitere Informationen zu hierarchischen **Recordset** -Objekten finden Sie in [Kapitel 9: Datenstrukturierung](chapter-9-data-shaping.md).


> [!NOTE]
> <P>[!HINWEIS] Beim Speichern hierarchischer <STRONG>Recordset</STRONG> -Objekte (Datenstrukturen) im XML-Format gelten einige Einschränkungen. Weitere Informationen finden Sie unter <A href="hierarchical-recordsets-in-xml.md">Hierarchische Recordset-Objekte in XML</A>.</P>


