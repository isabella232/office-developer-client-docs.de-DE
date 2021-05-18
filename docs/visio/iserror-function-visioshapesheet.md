---
title: ISERROR-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251452
localization_priority: Normal
ms.assetid: 4864ebc2-fee6-2415-7c59-e0af8611f8d6
description: Gibt TRUE zurück, wenn der Wert von cellreference ein Beliebiger Fehlertyp ist. Andernfalls wird FALSE zurückgegeben. Die ISERROR-Funktion wird in Formeln verwendet, die auf eine andere Zelle verweisen.
ms.openlocfilehash: a07b2345858e36dc2e4514d7e4f0f0d653491b50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421543"
---
# <a name="iserror-function-visioshapesheet"></a><span data-ttu-id="5b21b-104">ISERROR-Funktion (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="5b21b-104">ISERROR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="5b21b-105">Gibt TRUE zurück, wenn der Wert von  _cellreference_ ein Beliebiger Fehlertyp ist. Andernfalls wird FALSE zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5b21b-105">Returns TRUE if the value of  _cellreference_ is any error type; otherwise, it returns FALSE.</span></span> <span data-ttu-id="5b21b-106">Die ISERROR-Funktion wird in Formeln verwendet, die auf eine andere Zelle verweisen.</span><span class="sxs-lookup"><span data-stu-id="5b21b-106">The ISERROR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5b21b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b21b-107">Syntax</span></span>

<span data-ttu-id="5b21b-108">ISERROR(\*\* *cellreference* \*\* )</span><span class="sxs-lookup"><span data-stu-id="5b21b-108">ISERROR(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5b21b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b21b-109">Parameters</span></span>

|<span data-ttu-id="5b21b-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="5b21b-110">**Name**</span></span>|<span data-ttu-id="5b21b-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="5b21b-111">**Required/Optional**</span></span>|<span data-ttu-id="5b21b-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="5b21b-112">**Data Type**</span></span>|<span data-ttu-id="5b21b-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5b21b-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5b21b-114">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="5b21b-114">_cellreference_</span></span> <br/> |<span data-ttu-id="5b21b-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5b21b-115">Required</span></span>  <br/> |<span data-ttu-id="5b21b-116">**String**</span><span class="sxs-lookup"><span data-stu-id="5b21b-116">**String**</span></span> <br/> |<span data-ttu-id="5b21b-117">Bezug auf eine Zelle.</span><span class="sxs-lookup"><span data-stu-id="5b21b-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="5b21b-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5b21b-118">Example 1</span></span>

|<span data-ttu-id="5b21b-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="5b21b-119">**Cell**</span></span>|<span data-ttu-id="5b21b-120">**Formula**</span><span class="sxs-lookup"><span data-stu-id="5b21b-120">**Formula**</span></span>|<span data-ttu-id="5b21b-121">**Zurückgegebener Wert**</span><span class="sxs-lookup"><span data-stu-id="5b21b-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5b21b-122">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="5b21b-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="5b21b-123">=NV( )</span><span class="sxs-lookup"><span data-stu-id="5b21b-123">=NA( )</span></span>  <br/> |<span data-ttu-id="5b21b-124">#N/A!</span><span class="sxs-lookup"><span data-stu-id="5b21b-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="5b21b-125">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="5b21b-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="5b21b-126">=ISERROR(Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="5b21b-126">=ISERROR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="5b21b-127">TRUE</span><span class="sxs-lookup"><span data-stu-id="5b21b-127">TRUE</span></span>  <br/> |
   
<span data-ttu-id="5b21b-p103">Gibt TRUE zurück, da die ISERROR-Funktion den Fehler #N/V! erkennt. Mit der ISERROR-Funktion können Sie alle Fehlertypen außer dem Fehlertyp #N/V! verwenden.</span><span class="sxs-lookup"><span data-stu-id="5b21b-p103">Returns TRUE because the #N/A! error is recognized by the ISERROR function. You can use ISERR to find all types but the #N/A! error.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="5b21b-132">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5b21b-132">Example 2</span></span>

|<span data-ttu-id="5b21b-133">**Cell**</span><span class="sxs-lookup"><span data-stu-id="5b21b-133">**Cell**</span></span>|<span data-ttu-id="5b21b-134">**Formula**</span><span class="sxs-lookup"><span data-stu-id="5b21b-134">**Formula**</span></span>|<span data-ttu-id="5b21b-135">**Zurückgegebener Wert**</span><span class="sxs-lookup"><span data-stu-id="5b21b-135">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5b21b-136">Scratch.X1</span><span class="sxs-lookup"><span data-stu-id="5b21b-136">Scratch.X1</span></span>  <br/> |<span data-ttu-id="5b21b-137">="House"</span><span class="sxs-lookup"><span data-stu-id="5b21b-137">="House"</span></span>  <br/> |<span data-ttu-id="5b21b-138">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="5b21b-138">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="5b21b-139">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="5b21b-139">Scratch.B1</span></span>  <br/> |<span data-ttu-id="5b21b-140">=ISERROR(Scratch.X1)</span><span class="sxs-lookup"><span data-stu-id="5b21b-140">=ISERROR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="5b21b-141">TRUE</span><span class="sxs-lookup"><span data-stu-id="5b21b-141">TRUE</span></span>  <br/> |
   
<span data-ttu-id="5b21b-p104">Gibt TRUE zurück, da die ISERROR-Funktion den Fehler #WERT! erkennt. Wenn Sie einen Ausdruck auf Basis des Fehlertyps #WERT! aufbauen möchten, verwenden Sie die Funktion ISERRVALUE.</span><span class="sxs-lookup"><span data-stu-id="5b21b-p104">Returns TRUE because the #VALUE! error is recognized by the ISERROR function. To build an expression based on the #VALUE! error, use the ISERRVALUE function.</span></span>
  

