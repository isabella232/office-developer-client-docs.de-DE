---
title: Description-Eigenschaft (ADO)
TOCTitle: Description property (ADO)
ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15)
ms:contentKeyID: 48544064
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ea9408d7858817e8ffd347528588b1cea9b2a8df
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562720"
---
# <a name="description-property-ado"></a>Description-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Beschreibt ein [Error](error-object-ado.md)-Objekt.

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert vom Datentyp **String** zurück, der eine Beschreibung des Fehlers enthält.

## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie die **Description** -Eigenschaft, um eine kurze Beschreibung des Fehlers zu erhalten. Zeigen Sie diese Eigenschaft an, um den Benutzer auf einen Fehler hinzuweisen, den Sie nicht behandeln können oder möchten. Die Zeichenfolge stammt aus ADO oder von einem Anbieter.

Die Anbieter sind für das Übergeben eines bestimmten Fehlertexts an ADO verantwortlich. ADO fügt für jeden Anbieterfehler oder jede erhaltene Warnung der [Errors](error-object-ado.md) -Auflistung ein **Error**-Objekt hinzu. Zeigen Sie die **Errors** -Auflistung an, um die vom Anbieter gemeldeten Fehler zu überprüfen.

