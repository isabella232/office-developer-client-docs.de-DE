---
title: ISERROR Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251452
localization_priority: Normal
ms.assetid: 4864ebc2-fee6-2415-7c59-e0af8611f8d6
description: Gibt TRUE zurück, wenn der Wert von Zellbezug beliebiger Fehlertyp ist. Andernfalls wird FALSE zurückgegeben. ISERROR-Funktion wird in Formeln verwendet, die auf einer anderen Zelle verweisen.
ms.openlocfilehash: c93801f5d61e45be5d178027405ead3aa129654d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797243"
---
# <a name="iserror-function-visioshapesheet"></a><span data-ttu-id="47ec4-104">ISERROR Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="47ec4-104">ISERROR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="47ec4-105">Gibt TRUE zurück, wenn der Wert von _Zellbezug_ beliebiger Fehlertyp ist. Andernfalls wird FALSE zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="47ec4-105">Returns TRUE if the value of  _cellreference_ is any error type; otherwise, it returns FALSE.</span></span> <span data-ttu-id="47ec4-106">ISERROR-Funktion wird in Formeln verwendet, die auf einer anderen Zelle verweisen.</span><span class="sxs-lookup"><span data-stu-id="47ec4-106">The ISERROR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="47ec4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="47ec4-107">Syntax</span></span>

<span data-ttu-id="47ec4-108">ISERROR (** *Zellbezug* **)</span><span class="sxs-lookup"><span data-stu-id="47ec4-108">ISERROR(** *cellreference* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="47ec4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="47ec4-109">Parameters</span></span>

|<span data-ttu-id="47ec4-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="47ec4-110">**Name**</span></span>|<span data-ttu-id="47ec4-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="47ec4-111">**Required/Optional**</span></span>|<span data-ttu-id="47ec4-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="47ec4-112">**Data Type**</span></span>|<span data-ttu-id="47ec4-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="47ec4-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="47ec4-114">_Zellbezug_</span><span class="sxs-lookup"><span data-stu-id="47ec4-114">_cellreference_</span></span> <br/> |<span data-ttu-id="47ec4-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="47ec4-115">Required</span></span>  <br/> |<span data-ttu-id="47ec4-116">**String**</span><span class="sxs-lookup"><span data-stu-id="47ec4-116">**String**</span></span> <br/> |<span data-ttu-id="47ec4-117">Bezug auf eine Zelle.</span><span class="sxs-lookup"><span data-stu-id="47ec4-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="47ec4-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="47ec4-118">Example 1</span></span>

|<span data-ttu-id="47ec4-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="47ec4-119">**Cell**</span></span>|<span data-ttu-id="47ec4-120">**Formula**</span><span class="sxs-lookup"><span data-stu-id="47ec4-120">**Formula**</span></span>|<span data-ttu-id="47ec4-121">**Zurückgegebener Wert**</span><span class="sxs-lookup"><span data-stu-id="47ec4-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="47ec4-122">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="47ec4-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="47ec4-123">=NV( )</span><span class="sxs-lookup"><span data-stu-id="47ec4-123">=NA( )</span></span>  <br/> |<span data-ttu-id="47ec4-124">#N/V!</span><span class="sxs-lookup"><span data-stu-id="47ec4-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="47ec4-125">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="47ec4-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="47ec4-126">=IsError(Scratch.a1)</span><span class="sxs-lookup"><span data-stu-id="47ec4-126">=ISERROR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="47ec4-127">TRUE</span><span class="sxs-lookup"><span data-stu-id="47ec4-127">TRUE</span></span>  <br/> |
   
<span data-ttu-id="47ec4-p103">Gibt TRUE zurück, da die ISERROR-Funktion den Fehler #N/V! erkennt. Mit der ISERROR-Funktion können Sie alle Fehlertypen außer dem Fehlertyp #N/V! verwenden.</span><span class="sxs-lookup"><span data-stu-id="47ec4-p103">Returns TRUE because the #N/A! error is recognized by the ISERROR function. You can use ISERR to find all types but the #N/A! error.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="47ec4-132">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="47ec4-132">Example 2</span></span>

|<span data-ttu-id="47ec4-133">**Cell**</span><span class="sxs-lookup"><span data-stu-id="47ec4-133">**Cell**</span></span>|<span data-ttu-id="47ec4-134">**Formula**</span><span class="sxs-lookup"><span data-stu-id="47ec4-134">**Formula**</span></span>|<span data-ttu-id="47ec4-135">**Zurückgegebener Wert**</span><span class="sxs-lookup"><span data-stu-id="47ec4-135">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="47ec4-136">Scratch.X1</span><span class="sxs-lookup"><span data-stu-id="47ec4-136">Scratch.X1</span></span>  <br/> |<span data-ttu-id="47ec4-137">="Haus"</span><span class="sxs-lookup"><span data-stu-id="47ec4-137">="House"</span></span>  <br/> |<span data-ttu-id="47ec4-138">#WERT!</span><span class="sxs-lookup"><span data-stu-id="47ec4-138">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="47ec4-139">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="47ec4-139">Scratch.B1</span></span>  <br/> |<span data-ttu-id="47ec4-140">=IsError(Scratch.x1)</span><span class="sxs-lookup"><span data-stu-id="47ec4-140">=ISERROR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="47ec4-141">TRUE</span><span class="sxs-lookup"><span data-stu-id="47ec4-141">TRUE</span></span>  <br/> |
   
<span data-ttu-id="47ec4-p104">Gibt TRUE zurück, da die ISERROR-Funktion den Fehler #WERT! erkennt. Wenn Sie einen Ausdruck auf Basis des Fehlertyps #WERT! aufbauen möchten, verwenden Sie die Funktion ISERRVALUE.</span><span class="sxs-lookup"><span data-stu-id="47ec4-p104">Returns TRUE because the #VALUE! error is recognized by the ISERROR function. To build an expression based on the #VALUE! error, use the ISERRVALUE function.</span></span>
  

