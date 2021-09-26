---
title: Fields.Count-Eigenschaft (DAO)
TOCTitle: Count Property
ms:assetid: 574de1db-2640-159b-7756-28c37acc9f83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194261(v=office.15)
ms:contentKeyID: 48544969
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9a58f534dc115281c649d2708c2ddf28d749fa3f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626624"
---
# <a name="fieldscount-property-dao"></a>Fields.Count-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Gibt die Anzahl der Objekte in der angegebenen Auflistung zurück. Schreibgeschützter **Integer**-Wert.

## <a name="syntax"></a>Syntax

*Ausdruck* . Count

*Ausdruck* Eine Variable, die ein **Fields**-Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Da die Elemente einer Auflistung mit 0 beginnen, müssen Schleifen immer mit dem Element 0 starten und mit dem Wert der **Count**-Eigenschaft minus 1 enden. Wenn eine Schleife die Elemente einer Auflistung durchsucht, ohne die **Count**-Eigenschaft zu überprüfen, können Sie einen **For Each...Next**-Befehl verwenden.

Der Wert der **Count**-Eigenschaft ist nie Null. Wenn ihr Wert 0 ist, sind keine Objekte in der Auflistung enthalten.

