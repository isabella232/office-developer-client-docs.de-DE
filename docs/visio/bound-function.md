---
title: BOUND-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60099
localization_priority: Normal
ms.assetid: 36374d78-1028-bd7f-6282-66555ee31306
description: Schränkt den Wert einer Zelle auf einen oder mehrere Bereiche ein.
ms.openlocfilehash: 85fbe66d4e458ac4e42c9eb3c65b9a3a1d8211df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425960"
---
# <a name="bound-function"></a><span data-ttu-id="0cc11-103">BOUND Function</span><span class="sxs-lookup"><span data-stu-id="0cc11-103">BOUND Function</span></span>

<span data-ttu-id="0cc11-104">Schränkt den Wert einer Zelle auf einen oder mehrere Bereiche ein.</span><span class="sxs-lookup"><span data-stu-id="0cc11-104">Constrains the value of a cell to a range or set of ranges.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="0cc11-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0cc11-105">Syntax</span></span>

<span data-ttu-id="0cc11-106">BOUND (\* \* *Wert* \* \*, \* \* *Typ* \* \*, \* \* *Ignore* \* \*, \* \* *Wert1* \* \*, \* \* *value2* \* \* \* \* \* [, ignore (n), Wert1 (n), Value2 (n),...] \* \* \*)</span><span class="sxs-lookup"><span data-stu-id="0cc11-106">BOUND (\*\* *value* \*\*, \*\* *type* \*\*, \*\* *ignore* \*\*, \*\* *value1* \*\*, \*\* *value2* \*\* \*\* \* [,ignore(n), value1(n), value2(n),...] \* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0cc11-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="0cc11-107">Parameters</span></span>

|<span data-ttu-id="0cc11-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="0cc11-108">**Name**</span></span>|<span data-ttu-id="0cc11-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="0cc11-109">**Required/Optional**</span></span>|<span data-ttu-id="0cc11-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="0cc11-110">**Data Type**</span></span>|<span data-ttu-id="0cc11-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0cc11-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0cc11-112">_value_</span><span class="sxs-lookup"><span data-stu-id="0cc11-112">_value_</span></span> <br/> |<span data-ttu-id="0cc11-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0cc11-113">Required</span></span>  <br/> |<span data-ttu-id="0cc11-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="0cc11-114">**Numeric**</span></span> <br/> |<span data-ttu-id="0cc11-115">Der aktuelle einzuschränkende Wert.</span><span class="sxs-lookup"><span data-stu-id="0cc11-115">The current value being constrained.</span></span>  <br/> |
| <span data-ttu-id="0cc11-116">_Typ_</span><span class="sxs-lookup"><span data-stu-id="0cc11-116">_type_</span></span> <br/> |<span data-ttu-id="0cc11-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0cc11-117">Required</span></span>  <br/> |<span data-ttu-id="0cc11-118">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="0cc11-118">**Numeric**</span></span> <br/> |<span data-ttu-id="0cc11-119">Gibt an, ob die Einschränkung einschließend (0), ausschließend (1) oder deaktiviert (2) ist.</span><span class="sxs-lookup"><span data-stu-id="0cc11-119">Whether the constraint is inclusive (0), exclusive (1), or disabled (2).</span></span>  <br/> |
| <span data-ttu-id="0cc11-120">_ignorieren_</span><span class="sxs-lookup"><span data-stu-id="0cc11-120">_ignore_</span></span> <br/> |<span data-ttu-id="0cc11-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0cc11-121">Required</span></span>  <br/> |<span data-ttu-id="0cc11-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="0cc11-122">**Boolean**</span></span> <br/> | <span data-ttu-id="0cc11-123">TRUE, um den Range zu ignorieren; FALSE, wenn der Wert der Zelle auf den Range beschränkt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0cc11-123">TRUE to ignore the range; FALSE to constrain the value of the cell to the range.</span></span>  <br/> |
| <span data-ttu-id="0cc11-124">_Wert1_</span><span class="sxs-lookup"><span data-stu-id="0cc11-124">_value1_</span></span> <br/> |<span data-ttu-id="0cc11-125">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0cc11-125">Required</span></span>  <br/> |<span data-ttu-id="0cc11-126">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="0cc11-126">**Numeric**</span></span> <br/> |<span data-ttu-id="0cc11-127">Erster Wert in einem Bereich.</span><span class="sxs-lookup"><span data-stu-id="0cc11-127">First value in a range.</span></span>  <br/> |
| <span data-ttu-id="0cc11-128">_Wert2_</span><span class="sxs-lookup"><span data-stu-id="0cc11-128">_value2_</span></span> <br/> |<span data-ttu-id="0cc11-129">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0cc11-129">Required</span></span>  <br/> |<span data-ttu-id="0cc11-130">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="0cc11-130">**Numeric**</span></span> <br/> |<span data-ttu-id="0cc11-131">Zweiter Wert in einem Bereich.</span><span class="sxs-lookup"><span data-stu-id="0cc11-131">Second value in a range.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0cc11-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0cc11-132">Remarks</span></span>

<span data-ttu-id="0cc11-133">Verwenden Sie die BOUND-Funktion, um den Wert einer Zelle auf eine Ober-und Untergrenze zu beschränken, um beispielsweise Objekte zu steuern, die nicht oberhalb oder unterhalb einer minimalen oder maximalen Höhe gedehnt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0cc11-133">Use the BOUND function to restrict a cell's value to an upper and lower bound, for example, to control objects that should not be stretched above or below a minimum or maximum height.</span></span> <span data-ttu-id="0cc11-134">Die Einschränkung kann im Hinblick auf den Bereich oder die Bereiche inklusive oder exklusiv sein.</span><span class="sxs-lookup"><span data-stu-id="0cc11-134">The constraint can be inclusive or exclusive with respect to the range or ranges.</span></span> <span data-ttu-id="0cc11-135">Wenn der aktuelle Wert nicht eingeschränkt werden soll, legen Sie den _Type_ -Parameter auf 2 (deaktiviert) fest.</span><span class="sxs-lookup"><span data-stu-id="0cc11-135">If the current value should not be constrained, set the  _type_ parameter to 2 (disabled).</span></span> 
  
<span data-ttu-id="0cc11-136">Sie können mehrere Bereiche definieren, indem Sie mehrere Vorkommen der Parameter _Ignore_, _Wert1_und _value2_ angeben.</span><span class="sxs-lookup"><span data-stu-id="0cc11-136">You can define multiple ranges by supplying multiple occurrences of the  _ignore_,  _value1_, and  _value2_ parameters.</span></span> <span data-ttu-id="0cc11-137">Verwenden Sie den _Ignore_ -Parameter, um Einschränkungen für einen bestimmten Zeitraum zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="0cc11-137">Use the  _ignore_ parameter to disable constraints by a particular range.</span></span> 
  
<span data-ttu-id="0cc11-138">Die Formel, die die gebundene Funktion enthält, wird nicht überschrieben, wenn sich ihr Wert ändert; Stattdessen wird die Formel beibehalten, und der neue Wert wird in den _value_ -Parameter eingefügt.</span><span class="sxs-lookup"><span data-stu-id="0cc11-138">The formula containing the BOUND function does not get overwritten when its value changes; instead, the formula is preserved and the new value is placed into the  _value_ parameter.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="0cc11-139">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0cc11-139">Example 1</span></span>

<span data-ttu-id="0cc11-140">In diesem Beispiel wird mit der BOUND-Funktion erzwungen, dass ein Steuerpunkt nicht die Grenzen eines Shape-Felds verlässt.</span><span class="sxs-lookup"><span data-stu-id="0cc11-140">This example uses the BOUND function to force a control handle to stay within the bounding box of a shape.</span></span> 
  
<span data-ttu-id="0cc11-141">Controls. x1 = BOUND (Breite\*0,5, 0, false, Breite\*0, Breite\*1)</span><span class="sxs-lookup"><span data-stu-id="0cc11-141">Controls.X1 = BOUND(Width\*0.5, 0, FALSE, Width\*0, Width\*1)</span></span>
  
<span data-ttu-id="0cc11-142">Controls. Y1 = BOUND (Höhe\*0,5, 0, false, Höhe\*0, Höhe\*1)</span><span class="sxs-lookup"><span data-stu-id="0cc11-142">Controls.Y1 = BOUND(Height\*0.5, 0, FALSE, Height\*0, Height\*1)</span></span>
  
## <a name="example-2"></a><span data-ttu-id="0cc11-143">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0cc11-143">Example 2</span></span>

<span data-ttu-id="0cc11-144">In diesem Beispiel wird mit der BOUND-Funktion die Breite eines Shapes auf 2 Zoll (inches), 4 Zoll oder 6 Zoll beschränkt.</span><span class="sxs-lookup"><span data-stu-id="0cc11-144">This example uses the BOUND function to constrain a shape's width to 2 inches, 4 inches, or 6 inches.</span></span> 
  
<span data-ttu-id="0cc11-145">Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)</span><span class="sxs-lookup"><span data-stu-id="0cc11-145">Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)</span></span>
  

