---
title: Name-Eigenschaft (ADO)
TOCTitle: Name property (ADO)
ms:assetid: 4b19bd08-ac3c-86f0-471d-06a37a0d4f89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249234(v=office.15)
ms:contentKeyID: 48544683
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f6fbfbd7008919cc4d784a4d0468d8471d102708
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288665"
---
# <a name="name-property-ado"></a>Name-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt den Namen eines Objekts an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen **String**-Wert fest, der den Namen eines Objekts oder einer Anwendung angibt, oder gibt den Wert zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **Name**-Eigenschaft, um den Namen eines **Command**-, **Property**-, **Field**- oder **Parameter**-Objekts zuzuweisen oder abzurufen.

Der Wert ist bei einem **Command**-Objekt nicht schreibgeschützt. Bei einem **Property**-Objekt ist der Wert schreibgeschützt.

Bei einem **Field** -Objekt ist **Name** in der Regel schreibgeschützt. Bei neuen **Field** -Objekten, die der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts angefügt wurden, ist **Name** erst schreibgeschützt, nachdem die [Value](value-property-ado.md)-Eigenschaft für das **Field** -Objekt festgelegt wurde und der Datenprovider das neue **Field** -Objekt durch Aufrufen der [Update](update-method-ado.md)-Methode der **Fields** -Auflistung hinzugefügt hat.

Bei **Parameter** -Objekten, die der [Parameters](parameters-collection-ado.md)-Auflistung noch nicht angefügt wurden, ist die **Name** -Eigenschaft nicht schreibgeschützt. Bei angefügten **Parameter** -Objekten und allen sonstigen Objekten ist die **Name** -Eigenschaft schreibgeschützt.

Sie können die **Name** -Eigenschaft eines Objekts anhand einer Ordnungszahl abrufen, nach der Sie direkt auf das Objekt über den Namen verweisen können. Beispiel: If rstMain. Properties (20). Name ergibt Veränderbarkeit, können Sie anschließend auf diese Eigenschaft als yields Veränderbarkeit verweisen, können Sie anschließend als rstMain. Properties ("Veränderbarkeit") auf diese Eigenschaft verweisen.

