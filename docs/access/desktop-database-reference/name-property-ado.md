---
title: Name-Eigenschaft (ADO)
TOCTitle: Name Property (ADO)
ms:assetid: 4b19bd08-ac3c-86f0-471d-06a37a0d4f89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249234(v=office.15)
ms:contentKeyID: 48544683
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 132d00af1aecf7ec1ae8fbdb7855a10dd99c7f4f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475466"
---
# <a name="name-property-ado"></a>Name-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013

Gibt den Namen eines Objekts an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen **String** -Wert fest, der den Namen eines Objekts oder einer Anwendung angibt, oder gibt den Wert zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **Name** -Eigenschaft, um den Namen eines **Command** -, **Property** -, **Field** - oder **Parameter** -Objekts zuzuweisen oder abzurufen.

Der Wert ist bei einem **Command** -Objekt nicht schreibgeschützt. Bei einem **Property** -Objekt ist der Wert schreibgeschützt.

Bei einem **Field** -Objekt ist **Name** in der Regel schreibgeschützt. Bei neuen **Field** -Objekten, die der [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts angefügt wurden, ist **Name** erst schreibgeschützt, nachdem die [Value](value-property-ado.md)-Eigenschaft für das **Field** -Objekt festgelegt wurde und der Datenprovider das neue **Field** -Objekt durch Aufrufen der [Update](update-method-ado.md)-Methode der **Fields** -Auflistung hinzugefügt hat.

Bei **Parameter** -Objekten, die der [Parameters](parameters-collection-ado.md)-Auflistung noch nicht angefügt wurden, ist die **Name** -Eigenschaft nicht schreibgeschützt. Bei angefügten **Parameter** -Objekten und allen sonstigen Objekten ist die **Name** -Eigenschaft schreibgeschützt.

Sie können die **Name** -Eigenschaft eines Objekts ordinal Bezugnahme abrufen, nach denen Sie auf das Objekt direkt nach Namen verweisen können. Beispielsweise wenn rstMain.Properties(20). Name ergibt Updatability, Sie können später auf diese Eigenschaft, wenn Updatability liefert verweisen, Sie können später auf diese Eigenschaft als rstMain.Properties("Updatability") verweisen.
