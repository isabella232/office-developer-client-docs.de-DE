---
title: Count-Eigenschaft (ADO)
TOCTitle: Count Property (ADO)
ms:assetid: b59f9581-ffd1-471d-44fa-3c1bb812e140
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249871(v=office.15)
ms:contentKeyID: 48547253
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ad02d854a560e3fa99bf7454c97083e88638c520
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474254"
---
# <a name="count-property-ado"></a>Count-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013

Gibt die Anzahl von Objekten in einer Auflistung an.

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert vom Datentyp **Long** zurück.

## <a name="remarks"></a>Hinweise

Mit der **Count** -Eigenschaft bestimmen Sie, wie viele Objekte in einer bestimmten Auflistung vorhanden sind.

Die Nummerierung für Auflistungselemente beginnt bei Null, weshalb Sie im Code Schleifen stets mit dem Element Null beginnen und mit dem Wert der **Count** -Eigenschaft minus 1 beenden sollten. Falls Sie Microsoft Visual Basic verwenden und Schleifen durch die Auflistungselemente ausführen möchten, ohne die **Count** -Eigenschaft zu überprüfen, verwenden Sie den Befehl **For** **Each...Next**.

Wenn die **Count** -Eigenschaft gleich null ist, sind in der Auflistung keine Objekte vorhanden.

