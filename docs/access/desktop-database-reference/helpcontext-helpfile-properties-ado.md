---
title: HelpContext, Hilfen-Eigenschaften (ADO)
TOCTitle: HelpContext, HelpFile properties (ADO)
ms:assetid: 8a79f994-f17c-2983-0593-095801be762e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15)
ms:contentKeyID: 48546194
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c90fee6b8525ab13c8a294f9b39c52c20f580a62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291992"
---
# <a name="helpcontext-helpfile-properties-ado"></a>HelpContext, Hilfen-Eigenschaften (ADO)

**Gilt für**: Access 2013, Office 2013

Gibt die Hilfedatei und das Hilfethema an, das einem [Error](error-object-ado.md)-Objekt zugeordnet ist.

## <a name="return-values"></a>Rückgabewerte

- **HelpContextID** - gibt eine Kontext-ID als **Long** -Wert für ein Thema in einer Hilfedatei zurück.

- **HelpFile** – gibt einen **String**-Wert zurück, der als vollständig aufgelöster Pfad zu einer Hilfedatei ausgewertet wird.

## <a name="remarks"></a>Bemerkungen

Wenn in der **HelpFile**-Eigenschaft eine Hilfedatei angegeben ist, wird mit der **HelpContext**-Eigenschaft automatisch das darin identifizierte Hilfethema angezeigt. Ist kein relevantes Hilfethema verfügbar, gibt die **HelpContext**-Eigenschaft Null zurück, und die **HelpFile**-Eigenschaft gibt eine leere Zeichenfolge ("") zurück.

