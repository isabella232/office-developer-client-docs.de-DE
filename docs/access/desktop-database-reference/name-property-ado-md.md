---
title: Name-Eigenschaft (ADO MD)
TOCTitle: Name property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 8bf9420370021b35c86c08746d0257289d156cd0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568796"
---
# <a name="name-property-ado-md"></a>Name-Eigenschaft (ADO MD)


**Gilt für**: Access 2013, Office 2013

Gibt den Namen eines Objekts an.

## <a name="return-values"></a>Rückgabewerte

Gibt einen schreibgeschützten **String**-Wert zurück.

## <a name="remarks"></a>HinwBemerkungeneise

Sie können die **Name**-Eigenschaft eines Objekts durch einen Ordinalverweis abrufen. Danach können Sie auf das Objekt direkt durch seinen Namen verweisen. Wenn z. B. "cdf.CubeDefs(0).Name" die Zeichenfolge "Bobs Video Store" zurückgibt, können Sie auf dieses [CubeDef](cubedef-object-ado-md.md)-Objekt durch die Zeichenfolge "cdf.CubeDefs("Bobs Video Store") verweisen.

