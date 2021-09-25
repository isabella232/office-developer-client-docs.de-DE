---
title: Type-Eigenschaft (ADO)
TOCTitle: Type property (ADO)
ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15)
ms:contentKeyID: 48543397
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f8bcdfe1c5f3ea1890603ef3c5b69258d3140ca6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585116"
---
# <a name="type-property-ado"></a>Type-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt den Funktions- oder Datentyp eines [Parameter](parameter-object-ado.md)-, [Field](field-object-ado.md)- oder [Property](property-object-ado.md)-Objekts an.

## <a name="settings-and-return-values"></a>Einstellungen- und Rückgabewerte

Legt einen [DataTypeEnum](datatypeenum.md)-Wert fest oder gibt den Wert zurück.

## <a name="remarks"></a>HinwBemerkungeneise

Bei **Parameter** -Objekten ist die **Type** -Eigenschaft nicht schreibgeschützt. Bei neuen **Field** -Objekten, die der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts angefügt wurden, ist **Type** erst schreibgeschützt, nachdem die [Value](value-property-ado.md)-Eigenschaft für das **Field** -Objekt festgelegt wurde und der Datenprovider das neue **Field** -Objekt durch Aufrufen der [Update](update-method-ado.md)-Methode der **Fields** -Auflistung hinzugefügt hat.

Bei allen anderen Objekten ist die **Type** -Eigenschaft schreibgeschützt.

