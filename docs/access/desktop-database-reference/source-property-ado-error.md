---
title: Source-Eigenschaft (ADO Error)
TOCTitle: Source property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ebaf5f3a9e0c8ae005c21b0872177e0699c0f9aa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568418"
---
# <a name="source-property-ado-error"></a>Source-Eigenschaft (ADO Error)


**Gilt für**: Access 2013, Office 2013

Gibt den Namen des Objekts oder der Anwendung an, die einen Fehler ursprünglich generierte.

## <a name="return-value"></a>Rückgabewert

Gibt einen **String**-Wert zurück, der den Namen eines Objekts oder einer Anwendung angibt.

## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie die **Source** -Eigenschaft für ein [Error](error-object-ado.md)-Objekt, um den Namen des Objekts oder der Anwendung zu ermitteln, die einen Fehler ursprünglich generierte. Dabei kann es sich um den Klassennamen oder die ProgID des Objekts handeln. Bei Fehlern in ADO lautet der Eigenschaftswert **ADODB.** *ObjectName*, wobei *ObjectName* der Name des Objekts ist, das den Fehler ausgelöst hat. Bei ADOX und ADO MD lautet der Wert jeweils **ADOX.** *ObjectName* und **ADOMD.** *ObjectName*.

Anhand der Fehlerdokumentation der Eigenschaften **Source**, [Number](number-property-ado.md) und [Description](description-property-ado.md) von **Error**-Objekten können Sie Code schreiben, mit dem der Fehler ordnungsgemäß behandelt wird.

Die **Source** -Eigenschaft ist für **Error** -Objekte schreibgeschützt.

