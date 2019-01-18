---
title: Source-Eigenschaft (ADO Error)
TOCTitle: Source property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f03dcc8049113df13ff8654aee340d1e2d6e502
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722893"
---
# <a name="source-property-ado-error"></a>Source-Eigenschaft (ADO Error)


**Betrifft**: Access 2013, Office 2013

Gibt den Namen des Objekts oder der Anwendung an, die einen Fehler ursprünglich generierte.

## <a name="return-value"></a>Rückgabewert

Gibt einen **String** -Wert zurück, der den Namen eines Objekts oder einer Anwendung angibt.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **Source** -Eigenschaft für ein [Error](error-object-ado.md)-Objekt, um den Namen des Objekts oder der Anwendung zu ermitteln, die einen Fehler ursprünglich generierte. Dabei kann es sich um den Klassennamen oder die ProgID des Objekts handeln. Bei Fehlern in ADO werden der Eigenschaftswert **ADODB. *** ObjectName*, wobei *ObjectName* der Name des Objekts entspricht, die den Fehler ausgelöst hat. Für ADO MD und ADOX werden der Wert **ADOX. *** ObjectName* und **ADOMD. *** ObjectName,* fest.

Anhand der Fehlerdokumentation der Eigenschaften **Source**, [Number](number-property-ado.md) und [Description](description-property-ado.md) von **Error** -Objekten können Sie Code schreiben, mit dem der Fehler ordnungsgemäß behandelt wird.

Die **Source** -Eigenschaft ist für **Error** -Objekte schreibgeschützt.

