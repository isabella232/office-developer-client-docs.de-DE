---
title: AbsolutePage-Eigenschaft (ADO)
TOCTitle: AbsolutePage property (ADO)
ms:assetid: b6e5daac-cc21-0aa6-9119-a973595762bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249881(v=office.15)
ms:contentKeyID: 48547288
ms.date: 10/17/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 15c4fe003acc3fbc76723c8d0dc271a75b5318d3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569664"
---
# <a name="absolutepage-property-ado"></a>AbsolutePage-Eigenschaft (ADO)

**Gilt für**: Access 2013, Office 2013

Gibt an, auf welcher Seite sich der aktuelle Datensatz befindet.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt fest oder gibt einen **Long -Wert** von 1 auf die Anzahl der Seiten im [Recordset](recordset-object-ado.md) -Objekt ([PageCount](pagecount-property-ado.md)), oder gibt einen der [PositionEnum](positionenum.md) -Werte zurück.

## <a name="remarks"></a>HinwBemerkungeneise

Mit dieser Eigenschaft kann die Nummer der Seite identifiziert werden, auf der sich der aktuelle Datensatz befindet. Sie verwendet die [PageSize](pagesize-property-ado.md)-Eigenschaft, um die Gesamtzahl von Rowsets des **Recordset** -Objekts logisch in Seitenblöcke aufzuteilen, die jeweils die Anzahl von Datensätzen gemäß **PageSize** enthalten (außer der letzten Seite, die weniger Datensätze haben kann). Die entsprechende Funktionalität muss vom Anbieter unterstützt werden, damit diese Eigenschaft verfügbar ist.

Beim Abrufen oder Festlegen der **AbsolutePage** -Eigenschaft verwendet ADO die [AbsolutePosition](absoluteposition-property-ado.md)- und die [PageSize](pagesize-property-ado.md)-Eigenschaft wie folgt zusammen:

- Zum Abrufen von **AbsolutePage** ruft ADO zuerst die **AbsolutePosition** -Eigenschaft ab und dividiert den Wert dann durch die **PageSize** -Eigenschaft.

- Zum Festlegen von **AbsolutePage** verschiebt ADO die **AbsolutePosition** -Eigenschaft wie folgt: **PageSize** wird mit dem neuen Wert von **AbsolutePage** multipliziert, und dann wird 1 addiert. Daher ist die aktuelle Position im **Recordset** nach dem erfolgreichen Festlegen von **AbsolutePage** der erste Datensatz auf dieser Seite.

**AbsolutePage** ist wie die **AbsolutePosition** -Eigenschaft 1-basiert und entspricht 1, wenn der aktuelle Datensatz der erste Datensatz im **Recordset** -Objekt ist. Legen Sie diese Eigenschaft fest, um zum ersten Datensatz einer bestimmten Seite zu navigieren. Die Gesamtseitenanzahl rufen Sie von der **PageCount** -Eigenschaft ab.

