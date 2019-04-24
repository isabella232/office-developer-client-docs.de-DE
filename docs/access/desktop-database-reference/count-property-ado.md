---
title: Count-Eigenschaft (ADO)
TOCTitle: Count property (ADO)
ms:assetid: b59f9581-ffd1-471d-44fa-3c1bb812e140
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249871(v=office.15)
ms:contentKeyID: 48547253
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e2a341a82e5cdc9ed5a55ca9f4b80ba80c6875bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295471"
---
# <a name="count-property-ado"></a>Count-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt die Anzahl von Objekten in einer Auflistung an.

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert vom Datentyp **Long** zurück.

## <a name="remarks"></a>Bemerkungen

Mit der **Count** -Eigenschaft bestimmen Sie, wie viele Objekte in einer bestimmten Auflistung vorhanden sind.

Die Nummerierung für Auflistungselemente beginnt bei Null, weshalb Sie im Code Schleifen stets mit dem Element Null beginnen und mit dem Wert der **Count** -Eigenschaft minus 1 beenden sollten. Falls Sie Microsoft Visual Basic verwenden und Schleifen durch die Auflistungselemente ausführen möchten, ohne die **Count** -Eigenschaft zu überprüfen, verwenden Sie den Befehl **For** **Each...Next**.

Wenn die **Count** -Eigenschaft gleich null ist, sind in der Auflistung keine Objekte vorhanden.

