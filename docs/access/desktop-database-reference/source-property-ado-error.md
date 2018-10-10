---
title: Source-Eigenschaft (ADO Error)
TOCTitle: Source Property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7dcc674a570b3d2adf6108316339a86333a82f9d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474239"
---
# <a name="source-property-ado-error"></a>Source-Eigenschaft (ADO Error)


**Betrifft**: Access 2013 | Office 2013

Gibt den Namen des Objekts oder der Anwendung an, die einen Fehler ursprünglich generierte.

## <a name="return-value"></a>Rückgabewert

Gibt einen **String** -Wert zurück, der den Namen eines Objekts oder einer Anwendung angibt.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **Source** -Eigenschaft für ein [Error](error-object-ado.md)-Objekt, um den Namen des Objekts oder der Anwendung zu ermitteln, die einen Fehler ursprünglich generierte. Dabei kann es sich um den Klassennamen oder die ProgID des Objekts handeln. Bei Fehlern in ADO werden der Eigenschaftswert **ADODB. *** ObjectName*, wobei *ObjectName* der Name des Objekts entspricht, die den Fehler ausgelöst hat. Für ADO MD und ADOX werden der Wert **ADOX. *** ObjectName* und **ADOMD. *** ObjectName,* fest.

Anhand der Fehlerdokumentation der Eigenschaften **Source**, [Number](number-property-ado.md) und [Description](description-property-ado.md) von **Error** -Objekten können Sie Code schreiben, mit dem der Fehler ordnungsgemäß behandelt wird.

Die **Source** -Eigenschaft ist für **Error** -Objekte schreibgeschützt.
