---
title: NumericScale-Eigenschaft (ADO)
TOCTitle: NumericScale property (ADO)
ms:assetid: 51b232d2-5bfd-521c-f4e9-65655ecc7c70
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249263(v=office.15)
ms:contentKeyID: 48544824
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1bcb0c1a38108fbd02551df2a3296abe4d9a3791
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707108"
---
# <a name="numericscale-property-ado"></a>NumericScale-Eigenschaft (ADO)


**Betrifft**: Access 2013, Office 2013

Gibt die Dezimalstellen numerischer Werte in einem [Parameter](parameter-object-ado.md)- oder [Field](field-object-ado.md)-Objekt an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen **Byte** -Wert fest, der die Anzahl von Dezimalstellen angibt, in die numerische Werte aufgelöst werden, oder gibt den Wert zurück.

## <a name="remarks"></a>Hinweise

Bestimmen Sie mit der **NumericScale** -Eigenschaft die Anzahl von Stellen rechts vom Dezimalkomma, die zur Darstellung von Werten für ein numerisches **Parameter** - oder **Field** -Objekt verwendet werden.

Bei **Parameter** -Objekten ist die **NumericScale** -Eigenschaft nicht schreibgeschützt.

Bei einem **Field** -Objekt ist **NumericScale** in der Regel schreibgeschützt. Bei neuen **Field** -Objekten, die der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts angefügt wurden, ist **NumericScale** erst schreibgeschützt, nachdem die [Value](value-property-ado.md)-Eigenschaft für das **Field** -Objekt festgelegt wurde und der Datenprovider das neue **Field** -Objekt durch Aufrufen der [Update](update-method-ado.md)-Methode der **Fields** -Auflistung hinzugefügt hat.

