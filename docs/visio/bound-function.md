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
ms.openlocfilehash: 2f6228828fee8fa1831bb0d3a714fca068808652
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796572"
---
# <a name="bound-function"></a><span data-ttu-id="fde56-103">BOUND Function</span><span class="sxs-lookup"><span data-stu-id="fde56-103">BOUND Function</span></span>

<span data-ttu-id="fde56-104">Schränkt den Wert einer Zelle auf einen oder mehrere Bereiche ein.</span><span class="sxs-lookup"><span data-stu-id="fde56-104">Constrains the value of a cell to a range or set of ranges.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="fde56-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fde56-105">Syntax</span></span>

<span data-ttu-id="fde56-106">GEBUNDEN (** *Wert* **, ** *Typ* **, ** *ignorieren* **, ** *Wert1* **, ** *value2* ** ** * [, ignore(n), value1(n), value2(n),...] * **)</span><span class="sxs-lookup"><span data-stu-id="fde56-106">BOUND (** *value* **, ** *type* **, ** *ignore* **, ** *value1* **, ** *value2* ** ** * [,ignore(n), value1(n), value2(n),...] * ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fde56-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fde56-107">Parameters</span></span>

|<span data-ttu-id="fde56-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="fde56-108">**Name**</span></span>|<span data-ttu-id="fde56-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="fde56-109">**Required/Optional**</span></span>|<span data-ttu-id="fde56-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="fde56-110">**Data Type**</span></span>|<span data-ttu-id="fde56-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fde56-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fde56-112">_Value_</span><span class="sxs-lookup"><span data-stu-id="fde56-112">_value_</span></span> <br/> |<span data-ttu-id="fde56-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fde56-113">Required</span></span>  <br/> |<span data-ttu-id="fde56-114">**Numerische**</span><span class="sxs-lookup"><span data-stu-id="fde56-114">**Numeric**</span></span> <br/> |<span data-ttu-id="fde56-115">Der aktuelle einzuschränkende Wert.</span><span class="sxs-lookup"><span data-stu-id="fde56-115">The current value being constrained.</span></span>  <br/> |
| <span data-ttu-id="fde56-116">_Typ_</span><span class="sxs-lookup"><span data-stu-id="fde56-116">_type_</span></span> <br/> |<span data-ttu-id="fde56-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fde56-117">Required</span></span>  <br/> |<span data-ttu-id="fde56-118">**Numerische**</span><span class="sxs-lookup"><span data-stu-id="fde56-118">**Numeric**</span></span> <br/> |<span data-ttu-id="fde56-119">Gibt an, ob die Einschränkung einschließend (0) ist ausschließend (1) oder deaktiviert (2).</span><span class="sxs-lookup"><span data-stu-id="fde56-119">Whether the constraint is inclusive (0), exclusive (1), or disabled (2).</span></span>  <br/> |
| <span data-ttu-id="fde56-120">_ignorieren_</span><span class="sxs-lookup"><span data-stu-id="fde56-120">_ignore_</span></span> <br/> |<span data-ttu-id="fde56-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fde56-121">Required</span></span>  <br/> |<span data-ttu-id="fde56-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="fde56-122">**Boolean**</span></span> <br/> | <span data-ttu-id="fde56-123">True, um den Bereich zu ignorieren. Legen Sie false fest, um den Wert der Zelle auf den Bereich einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="fde56-123">TRUE to ignore the range; FALSE to constrain the value of the cell to the range.</span></span>  <br/> |
| <span data-ttu-id="fde56-124">_Wert1_</span><span class="sxs-lookup"><span data-stu-id="fde56-124">_value1_</span></span> <br/> |<span data-ttu-id="fde56-125">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fde56-125">Required</span></span>  <br/> |<span data-ttu-id="fde56-126">**Numerische**</span><span class="sxs-lookup"><span data-stu-id="fde56-126">**Numeric**</span></span> <br/> |<span data-ttu-id="fde56-127">Erster Wert in einem Bereich.</span><span class="sxs-lookup"><span data-stu-id="fde56-127">First value in a range.</span></span>  <br/> |
| <span data-ttu-id="fde56-128">_Wert2_</span><span class="sxs-lookup"><span data-stu-id="fde56-128">_value2_</span></span> <br/> |<span data-ttu-id="fde56-129">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fde56-129">Required</span></span>  <br/> |<span data-ttu-id="fde56-130">**Numerische**</span><span class="sxs-lookup"><span data-stu-id="fde56-130">**Numeric**</span></span> <br/> |<span data-ttu-id="fde56-131">Zweiter Wert in einem Bereich.</span><span class="sxs-lookup"><span data-stu-id="fde56-131">Second value in a range.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fde56-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fde56-132">Remarks</span></span>

<span data-ttu-id="fde56-133">Verwenden der BOUND-Funktion zum Einschränken der Wert auf eine obere und die untere Grenze, beispielsweise einer Zelle, um Objekte zu steuern, die nicht über oder unter eine minimale oder maximale Höhe gedehnt werden sollten.</span><span class="sxs-lookup"><span data-stu-id="fde56-133">Use the BOUND function to restrict a cell's value to an upper and lower bound, for example, to control objects that should not be stretched above or below a minimum or maximum height.</span></span> <span data-ttu-id="fde56-134">Die Einschränkung kann inklusive oder exklusive in Bezug auf den Bereich oder die Bereiche.</span><span class="sxs-lookup"><span data-stu-id="fde56-134">The constraint can be inclusive or exclusive with respect to the range or ranges.</span></span> <span data-ttu-id="fde56-135">Wenn der aktuelle Wert nicht eingeschränkt werden soll, legen Sie den Parameter _Type_ auf 2 (deaktiviert).</span><span class="sxs-lookup"><span data-stu-id="fde56-135">If the current value should not be constrained, set the  _type_ parameter to 2 (disabled).</span></span> 
  
<span data-ttu-id="fde56-136">Sie können mehrere Bereiche definieren, indem der Parameter _ignore_, _value1_und _value2_ mehrere Vorkommen.</span><span class="sxs-lookup"><span data-stu-id="fde56-136">You can define multiple ranges by supplying multiple occurrences of the  _ignore_,  _value1_, and  _value2_ parameters.</span></span> <span data-ttu-id="fde56-137">Verwenden Sie den Parameter _ignorieren_ , um Einschränkungen durch einen bestimmten Bereich deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="fde56-137">Use the  _ignore_ parameter to disable constraints by a particular range.</span></span> 
  
<span data-ttu-id="fde56-138">Die Formel, die mit der BOUND-Funktion ist nicht überschrieben, wenn der Wert geändert wird; stattdessen die Formel wird beibehalten, und der neue Wert wird in der _Value_ -Parameter eingefügt.</span><span class="sxs-lookup"><span data-stu-id="fde56-138">The formula containing the BOUND function does not get overwritten when its value changes; instead, the formula is preserved and the new value is placed into the  _value_ parameter.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="fde56-139">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fde56-139">Example 1</span></span>

<span data-ttu-id="fde56-140">In diesem Beispiel wird mit der BOUND-Funktion erzwungen, dass ein Steuerpunkt nicht die Grenzen eines Shape-Felds verlässt.</span><span class="sxs-lookup"><span data-stu-id="fde56-140">This example uses the BOUND function to force a control handle to stay within the bounding box of a shape.</span></span> 
  
<span data-ttu-id="fde56-141">Controls.X1 = Grenze (Breite\*0,5, 0, FALSE, Breite\*0, Breite\*1)</span><span class="sxs-lookup"><span data-stu-id="fde56-141">Controls.X1 = BOUND(Width\*0.5, 0, FALSE, Width\*0, Width\*1)</span></span>
  
<span data-ttu-id="fde56-142">Controls.Y1 = Grenze (Höhe\*0,5, 0, FALSE, Height\*0, Höhe\*1)</span><span class="sxs-lookup"><span data-stu-id="fde56-142">Controls.Y1 = BOUND(Height\*0.5, 0, FALSE, Height\*0, Height\*1)</span></span>
  
## <a name="example-2"></a><span data-ttu-id="fde56-143">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fde56-143">Example 2</span></span>

<span data-ttu-id="fde56-144">In diesem Beispiel wird mit der BOUND-Funktion die Breite eines Shapes auf 2 Zoll (inches), 4 Zoll oder 6 Zoll beschränkt.</span><span class="sxs-lookup"><span data-stu-id="fde56-144">This example uses the BOUND function to constrain a shape's width to 2 inches, 4 inches, or 6 inches.</span></span> 
  
<span data-ttu-id="fde56-145">Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)</span><span class="sxs-lookup"><span data-stu-id="fde56-145">Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)</span></span>
  

