---
title: HelpContext-, HelpFile-Eigenschaft (ADO)
TOCTitle: HelpContext, HelpFile properties (ADO)
ms:assetid: 8a79f994-f17c-2983-0593-095801be762e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15)
ms:contentKeyID: 48546194
ms.date: 10/17/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 860d300d0be62e2db17776c03289b0ef8a3d4029
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615431"
---
# <a name="helpcontext-helpfile-properties-ado"></a>HelpContext-, HelpFile-Eigenschaft (ADO)

**Gilt für**: Access 2013, Office 2013

Gibt die Hilfedatei und das Hilfethema an, das einem [Error](error-object-ado.md)-Objekt zugeordnet ist.

## <a name="return-values"></a>Rückgabewerte

- **HelpContextID** - gibt eine Kontext-ID als **Long** -Wert für ein Thema in einer Hilfedatei zurück.

- **HelpFile** – gibt einen **String**-Wert zurück, der als vollständig aufgelöster Pfad zu einer Hilfedatei ausgewertet wird.

## <a name="remarks"></a>Bemerkungen

Wenn in der **HelpFile**-Eigenschaft eine Hilfedatei angegeben ist, wird mit der **HelpContext**-Eigenschaft automatisch das darin identifizierte Hilfethema angezeigt. Ist kein relevantes Hilfethema verfügbar, gibt die **HelpContext**-Eigenschaft Null zurück, und die **HelpFile**-Eigenschaft gibt eine leere Zeichenfolge ("") zurück.

