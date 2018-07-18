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
# <a name="iserrvalue-function"></a><span data-ttu-id="8d074-104">ISERRVALUE Function</span><span class="sxs-lookup"><span data-stu-id="8d074-104">ISERRVALUE Function</span></span>

<span data-ttu-id="8d074-105">Gibt True, wenn der Wert von _Zellbezug_ Fehler ist geben #VALUE, wobei ein Argument in der Formel den falschen Typ besitzt.</span><span class="sxs-lookup"><span data-stu-id="8d074-105">Returns TRUE if the value of  _cellreference_ is error type #VALUE, where an argument in the formula is the wrong type.</span></span> <span data-ttu-id="8d074-106">ISERRVALUE-Funktion wird in logischen Ausdrücken verwendet, die auf einer anderen Zelle verweisen.</span><span class="sxs-lookup"><span data-stu-id="8d074-106">The ISERRVALUE function is used in logical expressions that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8d074-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d074-107">Syntax</span></span>

<span data-ttu-id="8d074-108">ISERRVALUE (** *Zellbezug* **)</span><span class="sxs-lookup"><span data-stu-id="8d074-108">ISERRVALUE(** *cellreference* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8d074-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d074-109">Parameters</span></span>

|<span data-ttu-id="8d074-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="8d074-110">**Name**</span></span>|<span data-ttu-id="8d074-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="8d074-111">**Required/Optional**</span></span>|<span data-ttu-id="8d074-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="8d074-112">**Data Type**</span></span>|<span data-ttu-id="8d074-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8d074-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8d074-114">_Zellbezug_</span><span class="sxs-lookup"><span data-stu-id="8d074-114">_cellreference_</span></span> <br/> |<span data-ttu-id="8d074-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8d074-115">Required</span></span>  <br/> |<span data-ttu-id="8d074-116">**String**</span><span class="sxs-lookup"><span data-stu-id="8d074-116">**String**</span></span> <br/> |<span data-ttu-id="8d074-117">Bezug auf eine Zelle.</span><span class="sxs-lookup"><span data-stu-id="8d074-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d074-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d074-118">Remarks</span></span>

<span data-ttu-id="8d074-p103">Die Entwurfzellen A bis D geben keinen Fehler vom Typ #WERT! zurück, da ihre Formeln in der gleichen Zeichenfolge Zahlen und Buchstaben enthalten können. Die Zellen X und Y dürfen nur Zahlen enthalten.</span><span class="sxs-lookup"><span data-stu-id="8d074-p103">Scratch cells A through D won't return a #VALUE! error because the formula can contain numbers and letters in the same string. Cells X and Y must contain numbers only.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="8d074-122">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8d074-122">Example 1</span></span>

|<span data-ttu-id="8d074-123">**Cell**</span><span class="sxs-lookup"><span data-stu-id="8d074-123">**Cell**</span></span>|<span data-ttu-id="8d074-124">**Formula**</span><span class="sxs-lookup"><span data-stu-id="8d074-124">**Formula**</span></span>|<span data-ttu-id="8d074-125">**Zurückgegebener Wert**</span><span class="sxs-lookup"><span data-stu-id="8d074-125">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8d074-126">Scratch.X1</span><span class="sxs-lookup"><span data-stu-id="8d074-126">Scratch.X1</span></span>  <br/> |<span data-ttu-id="8d074-127">="Haus"</span><span class="sxs-lookup"><span data-stu-id="8d074-127">= "House"</span></span>  <br/> |<span data-ttu-id="8d074-128">#WERT!</span><span class="sxs-lookup"><span data-stu-id="8d074-128">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="8d074-129">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="8d074-129">Scratch.A1</span></span>  <br/> |<span data-ttu-id="8d074-130">= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)</span><span class="sxs-lookup"><span data-stu-id="8d074-130">= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)</span></span>  <br/> |<span data-ttu-id="8d074-131">2</span><span class="sxs-lookup"><span data-stu-id="8d074-131">2</span></span>  <br/> |
   
<span data-ttu-id="8d074-p104">Gibt 2 zurück, da der zurückgegebene Wert den Fehlertyp #WERT! aufweist und der Ausdruck Microsoft Visio anweist, statt des Fehlers eine 2 zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="8d074-p104">Returns 2 because the value returned is a #VALUE! error, and the expression instructs Microsoft Visio to return a 2 in place of the error.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="8d074-134">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8d074-134">Example 2</span></span>

|<span data-ttu-id="8d074-135">**Cell**</span><span class="sxs-lookup"><span data-stu-id="8d074-135">**Cell**</span></span>|<span data-ttu-id="8d074-136">**Formula**</span><span class="sxs-lookup"><span data-stu-id="8d074-136">**Formula**</span></span>|<span data-ttu-id="8d074-137">**Zurückgegebener Wert**</span><span class="sxs-lookup"><span data-stu-id="8d074-137">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8d074-138">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="8d074-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="8d074-139">="5 + 7"</span><span class="sxs-lookup"><span data-stu-id="8d074-139">="5 + 7"</span></span>  <br/> |<span data-ttu-id="8d074-140">5 + 7</span><span class="sxs-lookup"><span data-stu-id="8d074-140">5 + 7</span></span>  <br/> |
|<span data-ttu-id="8d074-141">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="8d074-141">Scratch.B1</span></span>  <br/> |<span data-ttu-id="8d074-142">= If (ISERRVALUE(Scratch.A1),2,Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="8d074-142">=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)</span></span>  <br/> |<span data-ttu-id="8d074-143">5 + 7</span><span class="sxs-lookup"><span data-stu-id="8d074-143">5 + 7</span></span>  <br/> |
   
<span data-ttu-id="8d074-p105">Gibt 12 zurück, da der zurückgegebene Wert nicht den Fehlertyp #WERT! aufweist und der Ausdruck Visio anweist, den Wert der ursprünglichen Zelle zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="8d074-p105">Returns 12 because the value returned is not a #VALUE! error, and the expression instructs Visio to return the value of the original cell.</span></span>
  

