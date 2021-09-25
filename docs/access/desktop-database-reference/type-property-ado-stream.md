---
title: Type-Eigenschaft (ADO Stream)
TOCTitle: Type Property (ADO Stream)
ms:assetid: 43872c74-51bf-47ae-6bdc-55d25b0dc84a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249203(v=office.15)
ms:contentKeyID: 48544505
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: e075a1380ee2716107d74cea81569e510214ab35
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593418"
---
# <a name="type-property-ado-stream"></a>Type-Eigenschaft (ADO Stream)


**Gilt für**: Access 2013, Office 2013

Gibt die Art der Daten an, die im [Stream](stream-object-ado.md)-Objekt enthalten sind (binär oder Text).

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen [StreamTypeEnum](streamtypeenum.md)-Wert fest, der die Art der Daten im **Stream** -Objekt angibt, oder gibt den Wert zurück. Der Standardwert ist **adTypeText**. Wenn jedoch zuerst binäre Daten in ein neues, leeres **Stream** -Objekt geschrieben werden, wird die **Type** -Eigenschaft in **adTypeBinary** geändert.

## <a name="remarks"></a>HinwBemerkungeneise

The **Type** property is read/write only when the current position is at the beginning of the **Stream** ([Position](position-property-ado.md) is 0), and read-only at any other position.

Die **Type**-Eigenschaft bestimmt, welche Methoden zum Lesen und Schreiben des **Stream**-Objekts verwendet werden. Verwenden Sie bei **Stream**-Textobjekten [ReadText](readtext-method-ado.md) und [WriteText](writetext-method-ado.md). Verwenden Sie bei binären **Stream**-Objekten [Read](read-method-ado.md) und [Write](write-method-ado.md).

