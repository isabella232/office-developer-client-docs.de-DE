---
title: AbsolutePage-Eigenschaft (ADO)
TOCTitle: AbsolutePage property (ADO)
ms:assetid: b6e5daac-cc21-0aa6-9119-a973595762bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249881(v=office.15)
ms:contentKeyID: 48547288
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6a0ad4caa6e31b6de39904016cd848e12690f72e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280684"
---
# <a name="absolutepage-property-ado"></a>AbsolutePage-Eigenschaft (ADO)

**Gilt für**: Access 2013, Office 2013

Gibt an, auf welcher Seite sich der aktuelle Datensatz befindet.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen **Long** -Wert zwischen 1 und der Anzahl von Seiten im [Recordset](recordset-object-ado.md) -Objekt ([PageCount](pagecount-property-ado.md)) fest oder gibt einen der [PositionEnum](positionenum.md) -Werte zurück.

## <a name="remarks"></a>Bemerkungen

Mit dieser Eigenschaft kann die Nummer der Seite identifiziert werden, auf der sich der aktuelle Datensatz befindet. Sie verwendet die [PageSize](pagesize-property-ado.md)-Eigenschaft, um die Gesamtzahl von Rowsets des **Recordset** -Objekts logisch in Seitenblöcke aufzuteilen, die jeweils die Anzahl von Datensätzen gemäß **PageSize** enthalten (außer der letzten Seite, die weniger Datensätze haben kann). Die entsprechende Funktionalität muss vom Anbieter unterstützt werden, damit diese Eigenschaft verfügbar ist.

Beim Abrufen oder Festlegen der **AbsolutePage** -Eigenschaft verwendet ADO die [AbsolutePosition](absoluteposition-property-ado.md)- und die [PageSize](pagesize-property-ado.md)-Eigenschaft wie folgt zusammen:

- Zum Abrufen von **AbsolutePage** ruft ADO zuerst die **AbsolutePosition** -Eigenschaft ab und dividiert den Wert dann durch die **PageSize** -Eigenschaft.

- Zum Festlegen von **AbsolutePage** verschiebt ADO die **AbsolutePosition** -Eigenschaft wie folgt: **PageSize** wird mit dem neuen Wert von **AbsolutePage** multipliziert, und dann wird 1 addiert. Daher ist die aktuelle Position im **Recordset** nach dem erfolgreichen Festlegen von **AbsolutePage** der erste Datensatz auf dieser Seite.

**AbsolutePage** ist wie die **AbsolutePosition** -Eigenschaft 1-basiert und entspricht 1, wenn der aktuelle Datensatz der erste Datensatz im **Recordset** -Objekt ist. Legen Sie diese Eigenschaft fest, um zum ersten Datensatz einer bestimmten Seite zu navigieren. Die Gesamtseitenanzahl rufen Sie von der **PageCount** -Eigenschaft ab.

