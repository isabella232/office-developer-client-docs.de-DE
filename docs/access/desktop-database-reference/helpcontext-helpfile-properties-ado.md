---
title: HelpContext- und HelpFile-Eigenschaft (ADO)
TOCTitle: HelpContext, HelpFile properties (ADO)
ms:assetid: 8a79f994-f17c-2983-0593-095801be762e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15)
ms:contentKeyID: 48546194
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c90fee6b8525ab13c8a294f9b39c52c20f580a62
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722515"
---
# <a name="helpcontext-helpfile-properties-ado"></a>HelpContext- und HelpFile-Eigenschaft (ADO)

**Betrifft**: Access 2013, Office 2013

Gibt die Hilfedatei und das Hilfethema an, das einem [Error](error-object-ado.md)-Objekt zugeordnet ist.

## <a name="return-values"></a>Rückgabewerte

- **HelpContextID** - gibt eine Kontext-ID als **Long** -Wert für ein Thema in einer Hilfedatei zurück.

- **HelpFile** - gibt einen **String** -Wert zurück, der als vollständig aufgelöster Pfad zu einer Hilfedatei ausgewertet wird.

## <a name="remarks"></a>Hinweise

Wenn in der **HelpFile** -Eigenschaft eine Hilfedatei angegeben ist, wird mit der **HelpContext** -Eigenschaft automatisch das darin identifizierte Hilfethema angezeigt. Ist kein relevantes Hilfethema verfügbar, gibt die **HelpContext** -Eigenschaft Null zurück, und die **HelpFile** -Eigenschaft gibt eine leere Zeichenfolge ("") zurück.

