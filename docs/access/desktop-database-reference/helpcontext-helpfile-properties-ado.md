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
# <a name="helpcontext-helpfile-properties-ado"></a><span data-ttu-id="9c0c3-102">HelpContext, Hilfen-Eigenschaften (ADO)</span><span class="sxs-lookup"><span data-stu-id="9c0c3-102">HelpContext, HelpFile properties (ADO)</span></span>

<span data-ttu-id="9c0c3-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9c0c3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9c0c3-104">Gibt die Hilfedatei und das Hilfethema an, das einem [Error](error-object-ado.md)-Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9c0c3-104">Indicates the help file and topic associated with an [Error](error-object-ado.md) object.</span></span>

## <a name="return-values"></a><span data-ttu-id="9c0c3-105">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="9c0c3-105">Return values</span></span>

- <span data-ttu-id="9c0c3-106">**HelpContextID** - gibt eine Kontext-ID als **Long** -Wert für ein Thema in einer Hilfedatei zurück.</span><span class="sxs-lookup"><span data-stu-id="9c0c3-106">**HelpContextID** — returns a context ID, as a **Long** value, for a topic in a Help file.</span></span>

- <span data-ttu-id="9c0c3-107">**HelpFile** – gibt einen **String**-Wert zurück, der als vollständig aufgelöster Pfad zu einer Hilfedatei ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="9c0c3-107">**HelpFile** — returns a **String** value that evaluates to a fully resolved path to a Help file.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c0c3-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c0c3-108">Remarks</span></span>

<span data-ttu-id="9c0c3-p101">Wenn in der **HelpFile**-Eigenschaft eine Hilfedatei angegeben ist, wird mit der **HelpContext**-Eigenschaft automatisch das darin identifizierte Hilfethema angezeigt. Ist kein relevantes Hilfethema verfügbar, gibt die **HelpContext**-Eigenschaft Null zurück, und die **HelpFile**-Eigenschaft gibt eine leere Zeichenfolge ("") zurück.</span><span class="sxs-lookup"><span data-stu-id="9c0c3-p101">If a Help file is specified in the **HelpFile** property, the **HelpContext** property is used to automatically display the Help topic it identifies. If there is no relevant help topic available, the **HelpContext** property returns zero and the **HelpFile** property returns a zero-length string ("").</span></span>

