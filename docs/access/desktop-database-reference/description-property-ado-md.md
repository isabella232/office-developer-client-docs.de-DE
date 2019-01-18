---
title: Description-Eigenschaft (ADO MD)
TOCTitle: Description property (ADO MD)
ms:assetid: 06d5e1d0-6ed7-fe14-3723-3790e225482a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248816(v=office.15)
ms:contentKeyID: 48543055
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0f74532693f1054dd9d187757af840a3a00b451f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720618"
---
# <a name="description-property-ado-md"></a>Description-Eigenschaft (ADO MD)


**Betrifft**: Access 2013, Office 2013

Gibt eine Texterläuterung des aktuellen Objekts zurück.

## <a name="return-values"></a>Rückgabewerte

Gibt einen schreibgeschützten **String** -Wert zurück.

## <a name="remarks"></a>Hinweise

Bei Member-Objekten wird die Description-Eigenschaft nur für Measure- und Formula-Member verwendet. Description gibt für alle anderen Elementtypen eine leere Zeichenfolge ("") zurück. Weitere Informationen zu verschiedenen Elementtypen finden Sie unter der Type-Eigenschaft.

Diese Eigenschaft wird nur für **Member** -Objekte unterstützt, die zu einem [Level](level-object-ado-md.md)-Objekt gehören. Es Wenn auf diese Eigenschaft durch **Member** -Objekte verwiesen wird, die zu einem [Position](position-object-ado-md.md)-Objekt gehören, tritt ein Fehler auf.

