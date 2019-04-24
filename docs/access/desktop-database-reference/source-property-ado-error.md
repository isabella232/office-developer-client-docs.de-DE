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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308596"
---
# <a name="source-property-ado-error"></a>Source-Eigenschaft (ADO Error)


**Gilt für**: Access 2013, Office 2013

Gibt den Namen des Objekts oder der Anwendung an, die einen Fehler ursprünglich generierte.

## <a name="return-value"></a>Rückgabewert

Gibt einen **String**-Wert zurück, der den Namen eines Objekts oder einer Anwendung angibt.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **Source** -Eigenschaft für ein [Error](error-object-ado.md)-Objekt, um den Namen des Objekts oder der Anwendung zu ermitteln, die einen Fehler ursprünglich generierte. Dabei kann es sich um den Klassennamen oder die ProgID des Objekts handeln. Bei Fehlern in ADO ist der Eigenschaftswert **ADODB. * * * ObjectName*, wobei ** ObjectName der Namen des Objekts ist, das den Fehler ausgelöst hat. Für ADOX und ADO MD lautet der Wert **ADOX. * ** * ObjectName und **ADOMD. * * * ObjectName* .

Anhand der Fehlerdokumentation der Eigenschaften **Source**, [Number](number-property-ado.md) und [Description](description-property-ado.md) von **Error** -Objekten können Sie Code schreiben, mit dem der Fehler ordnungsgemäß behandelt wird.

Die **Source** -Eigenschaft ist für **Error** -Objekte schreibgeschützt.

