---
title: Name-Eigenschaft (ADO)
TOCTitle: Name property (ADO)
ms:assetid: 4b19bd08-ac3c-86f0-471d-06a37a0d4f89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249234(v=office.15)
ms:contentKeyID: 48544683
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 42b543481e023e10dd79cd42302a5f5f8c98bf93
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626274"
---
# <a name="name-property-ado"></a>Name-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt den Namen eines Objekts an.

## <a name="settings-and-return-values"></a>Einstellungen- und Rückgabewerte

Legt einen **String**-Wert fest, der den Namen eines Objekts oder einer Anwendung angibt, oder gibt den Wert zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **Name**-Eigenschaft, um den Namen eines **Command**-, **Property**-, **Field**- oder **Parameter**-Objekts zuzuweisen oder abzurufen.

Der Wert ist bei einem **Command**-Objekt nicht schreibgeschützt. Bei einem **Property**-Objekt ist der Wert schreibgeschützt.

Bei einem **Field** -Objekt ist **Name** in der Regel schreibgeschützt. Bei neuen **Field** -Objekten, die der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts angefügt wurden, ist **Name** erst schreibgeschützt, nachdem die [Value](value-property-ado.md)-Eigenschaft für das **Field** -Objekt festgelegt wurde und der Datenprovider das neue **Field** -Objekt durch Aufrufen der [Update](update-method-ado.md)-Methode der **Fields** -Auflistung hinzugefügt hat.

Bei **Parameter** -Objekten, die der [Parameters](parameters-collection-ado.md)-Auflistung noch nicht angefügt wurden, ist die **Name** -Eigenschaft nicht schreibgeschützt. Bei angefügten **Parameter** -Objekten und allen sonstigen Objekten ist die **Name** -Eigenschaft schreibgeschützt.

Sie können die **Name-Eigenschaft** eines Objekts durch einen Ordinalverweis abrufen, nach dem Sie direkt anhand des Namens auf das Objekt verweisen können. Beispiel: rstMain.Properties(20). Name ergibt Updatability . Anschließend können Sie auf diese Eigenschaft als "Updatability" verweisen. Anschließend können Sie auf diese Eigenschaft als "rstMain.Properties("Updatability") verweisen.

