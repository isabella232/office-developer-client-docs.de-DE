---
title: Name-Eigenschaft (ADO MD)
TOCTitle: Name property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e4e27870a0c1dbb38b7c0be31c439a95f6aae671
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704154"
---
# <a name="name-property-ado-md"></a>Name-Eigenschaft (ADO MD)


**Betrifft**: Access 2013, Office 2013

Gibt den Namen eines Objekts an.

## <a name="return-values"></a>Rückgabewerte

Gibt einen schreibgeschützten **String** -Wert zurück.

## <a name="remarks"></a>Hinweise

Sie können die **Name** -Eigenschaft eines Objekts durch einen Ordinalverweis abrufen. Danach können Sie auf das Objekt direkt durch seinen Namen verweisen. Wenn z. B. "cdf.CubeDefs(0).Name" die Zeichenfolge "Bobs Video Store" zurückgibt, können Sie auf dieses [CubeDef](cubedef-object-ado-md.md)-Objekt durch die Zeichenfolge "cdf.CubeDefs("Bobs Video Store") verweisen.

