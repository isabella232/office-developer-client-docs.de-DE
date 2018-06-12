---
title: ISERRVALUE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251453
localization_priority: Normal
ms.assetid: c7feec6f-f47a-60ee-b056-7b2dc51ed9a9
description: 'Gibt True, wenn der Wert von Zellbezug Fehler ist geben #VALUE, wobei ein Argument in der Formel den falschen Typ besitzt. ISERRVALUE-Funktion wird in logischen Ausdrücken verwendet, die auf einer anderen Zelle verweisen.'
ms.openlocfilehash: 50c501cc404d9c5f80e0bd1261b3d3bcd7087de2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797246"
---
# <a name="iserrvalue-function"></a><span data-ttu-id="50442-104">ISERRVALUE-Funktion</span><span class="sxs-lookup"><span data-stu-id="50442-104">ISERRVALUE Function</span></span>

<span data-ttu-id="50442-105">Gibt True, wenn der Wert von _Zellbezug_ Fehler ist geben #VALUE, wobei ein Argument in der Formel den falschen Typ besitzt.</span><span class="sxs-lookup"><span data-stu-id="50442-105">Returns TRUE if the value of  _cellreference_ is error type #VALUE, where an argument in the formula is the wrong type.</span></span> <span data-ttu-id="50442-106">ISERRVALUE-Funktion wird in logischen Ausdrücken verwendet, die auf einer anderen Zelle verweisen.</span><span class="sxs-lookup"><span data-stu-id="50442-106">The ISERRVALUE function is used in logical expressions that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="50442-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="50442-107">Syntax</span></span>

<span data-ttu-id="50442-108">ISERRVALUE (** *Zellbezug* **)</span><span class="sxs-lookup"><span data-stu-id="50442-108">ISERRVALUE(** *cellreference* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="50442-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="50442-109">Parameters</span></span>

|<span data-ttu-id="50442-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="50442-110">**Name**</span></span>|<span data-ttu-id="50442-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="50442-111">**Required/Optional**</span></span>|<span data-ttu-id="50442-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="50442-112">**Data Type**</span></span>|<span data-ttu-id="50442-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="50442-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="50442-114">_Zellbezug_</span><span class="sxs-lookup"><span data-stu-id="50442-114">_cellreference_</span></span> <br/> |<span data-ttu-id="50442-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="50442-115">Required</span></span>  <br/> |<span data-ttu-id="50442-116">**String**</span><span class="sxs-lookup"><span data-stu-id="50442-116">**String**</span></span> <br/> |<span data-ttu-id="50442-117">Bezug auf eine Zelle.</span><span class="sxs-lookup"><span data-stu-id="50442-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50442-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50442-118">Remarks</span></span>

<span data-ttu-id="50442-p103">Die Entwurfzellen A bis D geben keinen Fehler vom Typ #WERT! zurück, da ihre Formeln in der gleichen Zeichenfolge Zahlen und Buchstaben enthalten können. Die Zellen X und Y dürfen nur Zahlen enthalten.</span><span class="sxs-lookup"><span data-stu-id="50442-p103">Scratch cells A through D won't return a #VALUE! error because the formula can contain numbers and letters in the same string. Cells X and Y must contain numbers only.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="50442-122">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="50442-122">Example 1</span></span>

|<span data-ttu-id="50442-123">**Cell**</span><span class="sxs-lookup"><span data-stu-id="50442-123">**Cell**</span></span>|<span data-ttu-id="50442-124">**Formula**</span><span class="sxs-lookup"><span data-stu-id="50442-124">**Formula**</span></span>|<span data-ttu-id="50442-125">**Zurückgegebener Wert**</span><span class="sxs-lookup"><span data-stu-id="50442-125">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="50442-126">Scratch.X1</span><span class="sxs-lookup"><span data-stu-id="50442-126">Scratch.X1</span></span>  <br/> |<span data-ttu-id="50442-127">="Haus"</span><span class="sxs-lookup"><span data-stu-id="50442-127">= "House"</span></span>  <br/> |<span data-ttu-id="50442-128">#WERT!</span><span class="sxs-lookup"><span data-stu-id="50442-128">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="50442-129">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="50442-129">Scratch.A1</span></span>  <br/> |<span data-ttu-id="50442-130">= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)</span><span class="sxs-lookup"><span data-stu-id="50442-130">= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)</span></span>  <br/> |<span data-ttu-id="50442-131">2</span><span class="sxs-lookup"><span data-stu-id="50442-131">2</span></span>  <br/> |
   
<span data-ttu-id="50442-p104">Gibt 2 zurück, da der zurückgegebene Wert den Fehlertyp #WERT! aufweist und der Ausdruck Microsoft Visio anweist, statt des Fehlers eine 2 zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="50442-p104">Returns 2 because the value returned is a #VALUE! error, and the expression instructs Microsoft Visio to return a 2 in place of the error.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="50442-134">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="50442-134">Example 2</span></span>

|<span data-ttu-id="50442-135">**Cell**</span><span class="sxs-lookup"><span data-stu-id="50442-135">**Cell**</span></span>|<span data-ttu-id="50442-136">**Formula**</span><span class="sxs-lookup"><span data-stu-id="50442-136">**Formula**</span></span>|<span data-ttu-id="50442-137">**Zurückgegebener Wert**</span><span class="sxs-lookup"><span data-stu-id="50442-137">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="50442-138">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="50442-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="50442-139">="5 + 7"</span><span class="sxs-lookup"><span data-stu-id="50442-139">="5 + 7"</span></span>  <br/> |<span data-ttu-id="50442-140">5 + 7</span><span class="sxs-lookup"><span data-stu-id="50442-140">5 + 7</span></span>  <br/> |
|<span data-ttu-id="50442-141">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="50442-141">Scratch.B1</span></span>  <br/> |<span data-ttu-id="50442-142">= If (ISERRVALUE(Scratch.A1),2,Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="50442-142">=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)</span></span>  <br/> |<span data-ttu-id="50442-143">5 + 7</span><span class="sxs-lookup"><span data-stu-id="50442-143">5 + 7</span></span>  <br/> |
   
<span data-ttu-id="50442-p105">Gibt 12 zurück, da der zurückgegebene Wert nicht den Fehlertyp #WERT! aufweist und der Ausdruck Visio anweist, den Wert der ursprünglichen Zelle zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="50442-p105">Returns 12 because the value returned is not a #VALUE! error, and the expression instructs Visio to return the value of the original cell.</span></span>
  

