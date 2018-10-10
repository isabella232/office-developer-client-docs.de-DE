---
title: Type-Eigenschaft (ADO)
TOCTitle: Type Property (ADO)
ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15)
ms:contentKeyID: 48543397
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2ac119b9582634e619455870c8a2e115f5e8dafa
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473554"
---
# <a name="type-property-ado"></a>Type-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013

Gibt den Funktions- oder Datentyp eines [Parameter](parameter-object-ado.md)-, [Field](field-object-ado.md)- oder [Property](property-object-ado.md)-Objekts an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen [DataTypeEnum](datatypeenum.md)-Wert fest oder gibt den Wert zurück.

## <a name="remarks"></a>Hinweise

Bei **Parameter** -Objekten ist die **Type** -Eigenschaft nicht schreibgeschützt. Bei neuen **Field** -Objekten, die der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts angefügt wurden, ist **Type** erst schreibgeschützt, nachdem die [Value](value-property-ado.md)-Eigenschaft für das **Field** -Objekt festgelegt wurde und der Datenprovider das neue **Field** -Objekt durch Aufrufen der [Update](update-method-ado.md)-Methode der **Fields** -Auflistung hinzugefügt hat.

Bei allen anderen Objekten ist die **Type** -Eigenschaft schreibgeschützt.

