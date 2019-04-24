---
title: Type-Eigenschaft (ADO Stream)
TOCTitle: Type Property (ADO Stream)
ms:assetid: 43872c74-51bf-47ae-6bdc-55d25b0dc84a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249203(v=office.15)
ms:contentKeyID: 48544505
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bb4cebdb8b4aff1413ec60fe4ebb1e05931f6476
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306251"
---
# <a name="type-property-ado-stream"></a>Type-Eigenschaft (ADO Stream)


**Gilt für**: Access 2013, Office 2013

Gibt die Art der Daten an, die im [Stream](stream-object-ado.md)-Objekt enthalten sind (binär oder Text).

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen [StreamTypeEnum](streamtypeenum.md)-Wert fest, der die Art der Daten im **Stream** -Objekt angibt, oder gibt den Wert zurück. Der Standardwert ist **adTypeText**. Wenn jedoch zuerst binäre Daten in ein neues, leeres **Stream** -Objekt geschrieben werden, wird die **Type** -Eigenschaft in **adTypeBinary** geändert.

## <a name="remarks"></a>Bemerkungen

Die **Type** -Eigenschaft ist nur Lese-/Schreibzugriff, wenn sich die aktuelle Position am Anfang des **Streams** befindet ([Position](position-property-ado.md) ist 0), und an jeder anderen Position schreibgeschützt.

Die **Type**-Eigenschaft bestimmt, welche Methoden zum Lesen und Schreiben des **Stream**-Objekts verwendet werden. Verwenden Sie bei **Stream**-Textobjekten [ReadText](readtext-method-ado.md) und [WriteText](writetext-method-ado.md). Verwenden Sie bei binären **Stream**-Objekten [Read](read-method-ado.md) und [Write](write-method-ado.md).

