---
title: PageCount-Eigenschaft (ADO)
TOCTitle: PageCount property (ADO)
ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15)
ms:contentKeyID: 48546609
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b37ccc0c9a61e00b3c2e8f5eb3367831e5ddea43
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704553"
---
# <a name="pagecount-property-ado"></a>PageCount-Eigenschaft (ADO)


**Betrifft**: Access 2013, Office 2013

Gibt an, wie viele Seiten mit Daten das [Recordset](recordset-object-ado.md)-Objekt enthält.

## <a name="return-value"></a>Rückgabewert

Gibt einen **Long** -Wert zurück, der die Anzahl von Seiten im **Recordset** -Objekt angibt.

## <a name="remarks"></a>Hinweise

Bestimmen Sie mit der PageCount-Eigenschaft, wie viele Seiten mit Daten in einem Recordset-Objekt enthalten sind. Seiten sind Datensatzgruppen, deren Größe der Einstellung der PageSize-Eigenschaft entspricht. Die letzte Seite wird auch dann als weitere Seite im PageCount-Wert gezählt, wenn sie nicht vollständig ist, weil sie weniger Datensätze enthält als der PageSize-Wert angibt. Wird diese Eigenschaft vom Recordset-Objekt nicht unterstützt, gibt der Wert -1 an, dass PageCount nicht bestimmt werden kann.

Weitere Informationen zur Seitenfunktionalität finden Sie unter den Eigenschaften **PageSize** und [AbsolutePage](absolutepage-property-ado.md).

