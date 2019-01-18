---
title: Type-Eigenschaft (ADO)
TOCTitle: Type property (ADO)
ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15)
ms:contentKeyID: 48543397
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 34a5d1cb1750dc9803c62202a06feccc2d464f9b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698253"
---
# <a name="type-property-ado"></a>Type-Eigenschaft (ADO)


**Betrifft**: Access 2013, Office 2013

Gibt den Funktions- oder Datentyp eines [Parameter](parameter-object-ado.md)-, [Field](field-object-ado.md)- oder [Property](property-object-ado.md)-Objekts an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen [DataTypeEnum](datatypeenum.md)-Wert fest oder gibt den Wert zurück.

## <a name="remarks"></a>Hinweise

Bei **Parameter** -Objekten ist die **Type** -Eigenschaft nicht schreibgeschützt. Bei neuen **Field** -Objekten, die der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts angefügt wurden, ist **Type** erst schreibgeschützt, nachdem die [Value](value-property-ado.md)-Eigenschaft für das **Field** -Objekt festgelegt wurde und der Datenprovider das neue **Field** -Objekt durch Aufrufen der [Update](update-method-ado.md)-Methode der **Fields** -Auflistung hinzugefügt hat.

Bei allen anderen Objekten ist die **Type** -Eigenschaft schreibgeschützt.

