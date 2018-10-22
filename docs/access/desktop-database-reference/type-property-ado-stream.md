---
title: Type-Eigenschaft (ADO Stream)
TOCTitle: Type Property (ADO Stream)
ms:assetid: 43872c74-51bf-47ae-6bdc-55d25b0dc84a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249203(v=office.15)
ms:contentKeyID: 48544505
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2fdf3f40565f41a3d34b2202c4e079839af1f1ff
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602741"
---
# <a name="type-property-ado-stream"></a>Type-Eigenschaft (ADO Stream)


**Betrifft**: Access 2013 | Office 2013

Gibt die Art der Daten an, die im [Stream](stream-object-ado.md)-Objekt enthalten sind (binär oder Text).

<<<<<<< Kopf
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
=======
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
>>>>>>> master

Legt einen [StreamTypeEnum](streamtypeenum.md)-Wert fest, der die Art der Daten im **Stream** -Objekt angibt, oder gibt den Wert zurück. Der Standardwert ist **adTypeText**. Wenn jedoch zuerst binäre Daten in ein neues, leeres **Stream** -Objekt geschrieben werden, wird die **Type** -Eigenschaft in **adTypeBinary** geändert.

## <a name="remarks"></a>Hinweise

Die Type-Eigenschaft ist nur dann nicht schreibgeschützt, wenn sich die aktuelle Position am Anfang des Stream-Objekts befindet (Position ist 0). Bei jeder anderen Position ist sie schreibgeschützt.

Die **Type** -Eigenschaft bestimmt, welche Methoden zum Lesen und Schreiben des **Stream** -Objekts verwendet werden. Verwenden Sie bei **Stream** -Textobjekten [ReadText](readtext-method-ado.md) und [WriteText](writetext-method-ado.md). Verwenden Sie bei binären **Stream** -Objekten [Read](read-method-ado.md) und [Write](write-method-ado.md).
