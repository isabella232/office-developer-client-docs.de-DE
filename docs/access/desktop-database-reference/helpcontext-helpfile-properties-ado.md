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
# <a name="helpcontext-helpfile-properties-ado"></a><span data-ttu-id="6298d-102">HelpContext- und HelpFile-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="6298d-102">HelpContext, HelpFile Properties (ADO)</span></span>


<span data-ttu-id="6298d-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6298d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6298d-104">Gibt die Hilfedatei und das Hilfethema an, das einem [Error](error-object-ado.md)-Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6298d-104">Indicates the help file and topic associated with an [Error](error-object-ado.md) object.</span></span>

## <a name="return-values"></a><span data-ttu-id="6298d-105">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="6298d-105">Return Values</span></span>

  - <span data-ttu-id="6298d-106">**HelpContextID** - gibt eine Kontext-ID als **Long** -Wert für ein Thema in einer Hilfedatei zurück.</span><span class="sxs-lookup"><span data-stu-id="6298d-106">**HelpContextID** — returns a context ID, as a **Long** value, for a topic in a Help file.</span></span>

  - <span data-ttu-id="6298d-107">**HelpFile** - gibt einen **String** -Wert zurück, der als vollständig aufgelöster Pfad zu einer Hilfedatei ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="6298d-107">**HelpFile** — returns a **String** value that evaluates to a fully resolved path to a Help file.</span></span>

## <a name="remarks"></a><span data-ttu-id="6298d-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6298d-108">Remarks</span></span>

<span data-ttu-id="6298d-p101">Wenn in der **HelpFile** -Eigenschaft eine Hilfedatei angegeben ist, wird mit der **HelpContext** -Eigenschaft automatisch das darin identifizierte Hilfethema angezeigt. Ist kein relevantes Hilfethema verfügbar, gibt die **HelpContext** -Eigenschaft Null zurück, und die **HelpFile** -Eigenschaft gibt eine leere Zeichenfolge ("") zurück.</span><span class="sxs-lookup"><span data-stu-id="6298d-p101">If a Help file is specified in the **HelpFile** property, the **HelpContext** property is used to automatically display the Help topic it identifies. If there is no relevant help topic available, the **HelpContext** property returns zero and the **HelpFile** property returns a zero-length string ("").</span></span>

