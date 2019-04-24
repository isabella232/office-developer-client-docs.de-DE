---
title: Größer oder gleich (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: cceb8dcb-5ce1-4c32-b057-6201b62a646f
description: Vergleicht zwei Ausdrücke im Hinblick auf größer als oder gleich.
localization_priority: Priority
ms.openlocfilehash: 76472544be950c68f3b5d42fe13b3040e9268f48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302499"
---
# <a name="greater-than-or-equal-to-access-custom-web-app"></a><span data-ttu-id="b3460-103">Größer oder gleich (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="b3460-103">Greater Than or Equal To (Access custom web app)</span></span>

<span data-ttu-id="b3460-104">Vergleicht zwei Ausdrücke im Hinblick auf größer als oder gleich.</span><span class="sxs-lookup"><span data-stu-id="b3460-104">Compares two expressions for greater than or equal.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="b3460-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="b3460-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b3460-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3460-107">Syntax</span></span>

`>= (Greater Than or Equal To)`

<span data-ttu-id="b3460-108">*expression*  \>=  *expression*</span><span class="sxs-lookup"><span data-stu-id="b3460-108">*expression*  \>=  *expression*</span></span> 
  
<span data-ttu-id="b3460-109">*expression*  Ein beliebiger gültiger Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="b3460-109">*expression*  Is any valid expression.</span></span> <span data-ttu-id="b3460-110">Beide Ausdrücke müssen implizit konvertierbare Datentypen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b3460-110">Both expressions must have implicitly convertible data types.</span></span> <span data-ttu-id="b3460-111">Die Konvertierung ist von den Regeln der Rangfolge der Datentypen abhängig.</span><span class="sxs-lookup"><span data-stu-id="b3460-111">The conversion depends on the rules of data type precedence.</span></span> 
  
## <a name="return-type"></a><span data-ttu-id="b3460-112">Rückgabetyp</span><span class="sxs-lookup"><span data-stu-id="b3460-112">Return Type</span></span>

<span data-ttu-id="b3460-113">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="b3460-113">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b3460-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b3460-114">Remarks</span></span>

<span data-ttu-id="b3460-115">Wenn Sie Ausdrücke vergleichen, die nicht null sind, so lautet das Ergebnis „TRUE“, wenn der linke Operand einen Wert aufweist, der größer oder gleich dem rechten Operanden ist, andernfalls ist das Ergebnis „FALSE“.</span><span class="sxs-lookup"><span data-stu-id="b3460-115">When you compare non-null expressions, the result is TRUE if the left operand has a greater or equal value than the right operand; otherwise, the result is FALSE.</span></span>
  

