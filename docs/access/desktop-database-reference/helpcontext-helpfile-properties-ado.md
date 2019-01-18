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
# <a name="helpcontext-helpfile-properties-ado"></a><span data-ttu-id="3e6a1-102">HelpContext- und HelpFile-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="3e6a1-102">HelpContext, HelpFile properties (ADO)</span></span>

<span data-ttu-id="3e6a1-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3e6a1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3e6a1-104">Gibt die Hilfedatei und das Hilfethema an, das einem [Error](error-object-ado.md)-Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3e6a1-104">Indicates the help file and topic associated with an [Error](error-object-ado.md) object.</span></span>

## <a name="return-values"></a><span data-ttu-id="3e6a1-105">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="3e6a1-105">Return values</span></span>

- <span data-ttu-id="3e6a1-106">**HelpContextID** - gibt eine Kontext-ID als **Long** -Wert für ein Thema in einer Hilfedatei zurück.</span><span class="sxs-lookup"><span data-stu-id="3e6a1-106">**HelpContextID** — returns a context ID, as a **Long** value, for a topic in a Help file.</span></span>

- <span data-ttu-id="3e6a1-107">**HelpFile** - gibt einen **String** -Wert zurück, der als vollständig aufgelöster Pfad zu einer Hilfedatei ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="3e6a1-107">**HelpFile** — returns a **String** value that evaluates to a fully resolved path to a Help file.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e6a1-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3e6a1-108">Remarks</span></span>

<span data-ttu-id="3e6a1-p101">Wenn in der **HelpFile** -Eigenschaft eine Hilfedatei angegeben ist, wird mit der **HelpContext** -Eigenschaft automatisch das darin identifizierte Hilfethema angezeigt. Ist kein relevantes Hilfethema verfügbar, gibt die **HelpContext** -Eigenschaft Null zurück, und die **HelpFile** -Eigenschaft gibt eine leere Zeichenfolge ("") zurück.</span><span class="sxs-lookup"><span data-stu-id="3e6a1-p101">If a Help file is specified in the **HelpFile** property, the **HelpContext** property is used to automatically display the Help topic it identifies. If there is no relevant help topic available, the **HelpContext** property returns zero and the **HelpFile** property returns a zero-length string ("").</span></span>

