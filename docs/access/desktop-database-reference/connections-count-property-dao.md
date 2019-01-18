---
title: Connections.Count-Eigenschaft (DAO)
TOCTitle: Count Property
ms:assetid: 9b2f0aaa-785a-7fe7-15c3-aea37fdacd12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198023(v=office.15)
ms:contentKeyID: 48546563
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a286bf992116dc4ddfa71a9be8231e70b717aaa3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713618"
---
# <a name="connectionscount-property-dao"></a>Connections.Count-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013

Gibt die Anzahl von **[Connection](connection-object-dao.md)** -Objekten in der **[Connections](connections-collection-dao.md)** -Auflistung zurück.

## <a name="syntax"></a>Syntax

*Ausdruck* . Count

*Ausdruck* Eine Variable, die ein **Connections** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Da die Elemente einer Auflistung mit 0 beginnen, müssen Schleifen immer mit dem Element 0 starten und mit dem Wert der **Count**-Eigenschaft minus 1 enden. Wenn eine Schleife die Elemente einer Auflistung durchsucht, ohne die **Count**-Eigenschaft zu überprüfen, können Sie einen **For Each...Next**-Befehl verwenden.

Der Wert der **Count**-Eigenschaft ist nie Null. Wenn ihr Wert 0 ist, sind keine Objekte in der Auflistung enthalten.

