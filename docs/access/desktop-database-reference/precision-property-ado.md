---
title: Precision-Eigenschaft (ADO)
TOCTitle: Precision property (ADO)
ms:assetid: c9d54d78-d5a5-caf8-d635-259d1fcc0595
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249983(v=office.15)
ms:contentKeyID: 48547685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f176bb08d757d94b11b9f407177fa27dacf76b70
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622123"
---
# <a name="precision-property-ado"></a>Precision-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt den Genauigkeitsgrad für numerische Werte in einem [Parameter](parameter-object-ado.md)-Objekt oder für numerische [Field](field-object-ado.md)-Objekte an.

## <a name="settings-and-return-values"></a>Einstellungen- und Rückgabewerte

Legt einen **Byte**-Wert fest oder gibt den Wert zurück, der die maximale Anzahl von Stellen angibt, die zum Darstellen eines Werts verwendet werden.

## <a name="remarks"></a>Bemerkungen

Bestimmen Sie mit der **Precision**-Eigenschaft die maximale Anzahl von Stellen, die zum Darstellen von Werten für ein numerisches **Parameter**- oder **Field**-Objekt verwendet werden.

Der Wert ist bei einem **Parameter** -Objekt nicht schreibgeschützt.

Bei einem **Field** -Objekt ist **Precision** in der Regel schreibgeschützt. Bei neuen **Field** -Objekten, die der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts angefügt wurden, ist **Precision** erst schreibgeschützt, nachdem die [Value](value-property-ado.md)-Eigenschaft für das **Field** -Objekt festgelegt wurde und der Datenprovider das neue **Field** -Objekt durch Aufrufen der [Update](update-method-ado.md)-Methode der **Fields** -Auflistung hinzugefügt hat.

