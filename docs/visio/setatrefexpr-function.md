---
title: SETATREFEXPR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027317
localization_priority: Normal
ms.assetid: c1bd7819-b53b-bff1-69c1-6d78e8fb278b
description: Speichert einen Wert, der durch eine Aktion in der Benutzeroberfläche (UI) oder Automatisierung festgelegt ist.
ms.openlocfilehash: c664717afcc2b81e55495fd1957a86ef1b021d0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798011"
---
# <a name="setatrefexpr-function"></a><span data-ttu-id="c210d-103">SETATREFEXPR Function</span><span class="sxs-lookup"><span data-stu-id="c210d-103">SETATREFEXPR Function</span></span>

<span data-ttu-id="c210d-104">Speichert einen Wert, der durch eine Aktion in der Benutzeroberfläche (UI) oder Automatisierung festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c210d-104">Stores a value that is set through an action in the user interface (UI) or Automation.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c210d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c210d-105">Syntax</span></span>

<span data-ttu-id="c210d-106">SETATREFEXPR ([** *Expr_opt* **])</span><span class="sxs-lookup"><span data-stu-id="c210d-106">SETATREFEXPR ([ ** *expr_opt* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c210d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c210d-107">Parameters</span></span>

|<span data-ttu-id="c210d-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c210d-108">**Name**</span></span>|<span data-ttu-id="c210d-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="c210d-109">**Required/Optional**</span></span>|<span data-ttu-id="c210d-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="c210d-110">**Data Type**</span></span>|<span data-ttu-id="c210d-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c210d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c210d-112">_expr_opt_</span><span class="sxs-lookup"><span data-stu-id="c210d-112">_expr_opt_</span></span> <br/> |<span data-ttu-id="c210d-113">Optional</span><span class="sxs-lookup"><span data-stu-id="c210d-113">Optional</span></span>  <br/> |<span data-ttu-id="c210d-114">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="c210d-114">**Varies**</span></span> <br/> |<span data-ttu-id="c210d-115">Ein Ausdruck, der durch den Wert oder ein Ausdruck, der in der SETATREF-Funktion referenzierten Zelle zugewiesen wird ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="c210d-115">An expression that is replaced by the value or expression being assigned to the referenced cell in the SETATREF function.</span></span> <span data-ttu-id="c210d-116">Wenn nicht angegeben haben, ist der Anfangswert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="c210d-116">If not indicated, its initial value is 0 (zero).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c210d-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c210d-117">Remarks</span></span>

<span data-ttu-id="c210d-118">Der Wert eines SETATREFEXPR-Ausdrucks kann auch über eine SETATREF-Funktion einer anderen Zelle, die auf die Zelle mit dem SETATREFEXPR-Ausdruck verweist, festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c210d-118">The value of a SETATREFEXPR expression can also be set from a SETATREF function in another cell that references the cell containing the SETATREFEXPR expression.</span></span> 
  
<span data-ttu-id="c210d-119">Sie sind nicht auf die Verwendung der SETATREFEXPR-Funktion als Parameter der SETATREF-Funktion beschränkt.</span><span class="sxs-lookup"><span data-stu-id="c210d-119">You are not limited to using the SETATREFEXPR function as a parameter to the SETATREF function.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="c210d-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c210d-120">Example 1</span></span>

<span data-ttu-id="c210d-121">Im folgenden Beispiel wird die SETATREFEXPR-Funktion verwendet, um sicherzustellen, dass ein Shape so breit wie der enthaltene Text ist.</span><span class="sxs-lookup"><span data-stu-id="c210d-121">The following example uses the SETATREFEXPR function to ensure that a shape is as wide as its text.</span></span>
  
<span data-ttu-id="c210d-122">Width =MAX(TEXTWIDTH(TheText),SETATREFEXPR())</span><span class="sxs-lookup"><span data-stu-id="c210d-122">Width =MAX(TEXTWIDTH(TheText),SETATREFEXPR())</span></span>
  
## <a name="example-2"></a><span data-ttu-id="c210d-123">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c210d-123">Example 2</span></span>

<span data-ttu-id="c210d-p102">Im folgenden Beispiel wird gezeigt, wie die SETATREFEXPR-Funktion verwendet werden kann, damit Shapes in einem benutzerdefinierten Gitter einrasten. Die SETATREFEXPR-Formeln werden in den Zellen PinX und PinY platziert, sodass der Drehbezugspunkt in dem in User.GridX und User.GridY definierten Gitter einrastet.</span><span class="sxs-lookup"><span data-stu-id="c210d-p102">The following example shows how you can use the SETATREFEXPR function to cause your shapes to snap to a custom grid. The SETATREFEXPR formulas are placed in the PinX and PinY cells, causing the shape's pin to snap to the grid defined in User.GridX and User.GridY.</span></span> 
  
<span data-ttu-id="c210d-126">User.GridX =2 in</span><span class="sxs-lookup"><span data-stu-id="c210d-126">User.GridX =2 in</span></span>
  
<span data-ttu-id="c210d-127">User.GridY =2 in</span><span class="sxs-lookup"><span data-stu-id="c210d-127">User.GridY =2 in</span></span>
  
<span data-ttu-id="c210d-128">PinX = INT (SETATREFEXPR /User.GridX () +.5)\*User.GridX</span><span class="sxs-lookup"><span data-stu-id="c210d-128">PinX =INT(SETATREFEXPR()/User.GridX + .5)\*User.GridX</span></span>
  
<span data-ttu-id="c210d-129">PinY = INT (SETATREFEXPR /User.GridY () +.5)\*User.GridY</span><span class="sxs-lookup"><span data-stu-id="c210d-129">PinY =INT(SETATREFEXPR()/User.GridY + .5)\*User.GridY</span></span>
  
## <a name="example-3"></a><span data-ttu-id="c210d-130">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c210d-130">Example 3</span></span>

<span data-ttu-id="c210d-131">Ein Beispiel zur Verwendung der SETATREFEXPR-Funktion zusammen mit der SETATREF-Funktion finden Sie unter der [SETATREF ](setatref-function.md)-Funktion.</span><span class="sxs-lookup"><span data-stu-id="c210d-131">For an example using the SETATREFEXPR function with the SETATREF function, see the [SETATREF](setatref-function.md) function.</span></span> 
  

