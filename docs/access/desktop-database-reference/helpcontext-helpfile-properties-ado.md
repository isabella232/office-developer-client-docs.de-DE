---
title: HelpContext- und HelpFile-Eigenschaft (ADO)
TOCTitle: HelpContext, HelpFile Properties (ADO)
ms:assetid: 8a79f994-f17c-2983-0593-095801be762e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15)
ms:contentKeyID: 48546194
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 23823ec18b4b87306fa852ac5b0b18e89f60d057
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475330"
---
# <a name="helpcontext-helpfile-properties-ado"></a>HelpContext- und HelpFile-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013

Gibt die Hilfedatei und das Hilfethema an, das einem [Error](error-object-ado.md)-Objekt zugeordnet ist.

## <a name="return-values"></a>Rückgabewerte

  - **HelpContextID** - gibt eine Kontext-ID als **Long** -Wert für ein Thema in einer Hilfedatei zurück.

  - **HelpFile** - gibt einen **String** -Wert zurück, der als vollständig aufgelöster Pfad zu einer Hilfedatei ausgewertet wird.

## <a name="remarks"></a>Hinweise

Wenn in der **HelpFile** -Eigenschaft eine Hilfedatei angegeben ist, wird mit der **HelpContext** -Eigenschaft automatisch das darin identifizierte Hilfethema angezeigt. Ist kein relevantes Hilfethema verfügbar, gibt die **HelpContext** -Eigenschaft Null zurück, und die **HelpFile** -Eigenschaft gibt eine leere Zeichenfolge ("") zurück.

