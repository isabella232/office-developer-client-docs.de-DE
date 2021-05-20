---
title: ISERRNA-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251451
localization_priority: Normal
ms.assetid: 6ee7dc3d-efe9-c862-f71d-034b3d9c3ec6
description: 'Gibt TRUE zurück, wenn der Wert von cellreference den Fehlertyp #N/A ist! (nicht verfügbar); Andernfalls wird FALSE zurückgegeben. Die ISERRNA-Funktion wird in Formeln verwendet, die auf eine andere Zelle verweisen.'
ms.openlocfilehash: 8a398eca6da659a6b8f29e4ef8e31b18abf56fde
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432114"
---
# <a name="iserrna-function"></a><span data-ttu-id="fcf59-105">ISERRNA-Funktion</span><span class="sxs-lookup"><span data-stu-id="fcf59-105">ISERRNA Function</span></span>

<span data-ttu-id="fcf59-106">Gibt TRUE zurück, wenn der Wert von  _cellreference_ den Fehlertyp #N/A!</span><span class="sxs-lookup"><span data-stu-id="fcf59-106">Returns TRUE if the value of  _cellreference_ is error type #N/A!</span></span> <span data-ttu-id="fcf59-107">(nicht verfügbar); Andernfalls wird FALSE zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fcf59-107">(not available); otherwise, it returns FALSE.</span></span> <span data-ttu-id="fcf59-108">Die ISERRNA-Funktion wird in Formeln verwendet, die auf eine andere Zelle verweisen.</span><span class="sxs-lookup"><span data-stu-id="fcf59-108">The ISERRNA function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="fcf59-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fcf59-109">Syntax</span></span>

<span data-ttu-id="fcf59-110">ISERRNA(\*\* *cellreference* \*\* )</span><span class="sxs-lookup"><span data-stu-id="fcf59-110">ISERRNA(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fcf59-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="fcf59-111">Parameters</span></span>

|<span data-ttu-id="fcf59-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="fcf59-112">**Name**</span></span>|<span data-ttu-id="fcf59-113">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="fcf59-113">**Required/Optional**</span></span>|<span data-ttu-id="fcf59-114">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="fcf59-114">**Data Type**</span></span>|<span data-ttu-id="fcf59-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fcf59-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fcf59-116">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="fcf59-116">_cellreference_</span></span> <br/> |<span data-ttu-id="fcf59-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fcf59-117">Required</span></span>  <br/> |<span data-ttu-id="fcf59-118">**String**</span><span class="sxs-lookup"><span data-stu-id="fcf59-118">**String**</span></span> <br/> |<span data-ttu-id="fcf59-119">Bezug auf eine Zelle.</span><span class="sxs-lookup"><span data-stu-id="fcf59-119">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="fcf59-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fcf59-120">Example 1</span></span>

|<span data-ttu-id="fcf59-121">**Cell**</span><span class="sxs-lookup"><span data-stu-id="fcf59-121">**Cell**</span></span>|<span data-ttu-id="fcf59-122">**Formula**</span><span class="sxs-lookup"><span data-stu-id="fcf59-122">**Formula**</span></span>|<span data-ttu-id="fcf59-123">**Zurückgegebener Wert**</span><span class="sxs-lookup"><span data-stu-id="fcf59-123">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fcf59-124">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="fcf59-124">Scratch.A1</span></span>  <br/> |<span data-ttu-id="fcf59-125">="5 + 3"</span><span class="sxs-lookup"><span data-stu-id="fcf59-125">="5 + 3"</span></span>  <br/> |<span data-ttu-id="fcf59-126">"8"</span><span class="sxs-lookup"><span data-stu-id="fcf59-126">"8"</span></span>  <br/> |
|<span data-ttu-id="fcf59-127">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="fcf59-127">Scratch.B1</span></span>  <br/> |<span data-ttu-id="fcf59-128">=ISERRNA(Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="fcf59-128">=ISERRNA(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="fcf59-129">FALSE</span><span class="sxs-lookup"><span data-stu-id="fcf59-129">FALSE</span></span>  <br/> |
   
<span data-ttu-id="fcf59-130">Gibt FALSE zurück, da der zurückgegebene Wert verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="fcf59-130">Returns FALSE because the value returned is available.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="fcf59-131">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fcf59-131">Example 2</span></span>

|<span data-ttu-id="fcf59-132">**Cell**</span><span class="sxs-lookup"><span data-stu-id="fcf59-132">**Cell**</span></span>|<span data-ttu-id="fcf59-133">**Formula**</span><span class="sxs-lookup"><span data-stu-id="fcf59-133">**Formula**</span></span>|<span data-ttu-id="fcf59-134">**Zurückgegebener Wert**</span><span class="sxs-lookup"><span data-stu-id="fcf59-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fcf59-135">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="fcf59-135">Scratch.A1</span></span>  <br/> |<span data-ttu-id="fcf59-136">=NV( )</span><span class="sxs-lookup"><span data-stu-id="fcf59-136">=NA( )</span></span>  <br/> |<span data-ttu-id="fcf59-137">#N/A!</span><span class="sxs-lookup"><span data-stu-id="fcf59-137">#N/A!</span></span>  <br/> |
|<span data-ttu-id="fcf59-138">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="fcf59-138">Scratch.B1</span></span>  <br/> |<span data-ttu-id="fcf59-139">=ISERRNA(Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="fcf59-139">=ISERRNA(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="fcf59-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="fcf59-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="fcf59-141">Gibt TRUE zurück, da der Rückgabewert den Fehlertyp #N/V! ergibt.</span><span class="sxs-lookup"><span data-stu-id="fcf59-141">Returns TRUE because the value returned is error type #N/A!</span></span>
  

