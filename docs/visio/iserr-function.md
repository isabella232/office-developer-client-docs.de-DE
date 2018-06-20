---
title: ISERR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251448
localization_priority: Normal
ms.assetid: 87508007-8ad2-3bcf-55dc-f0207c7c6fe3
description: 'Gibt true zurück, wenn der Wert von Zellbezug beliebiger Fehlertyp #n /; Andernfalls wird FALSE zurückgegeben. Die Funktion ISERR wird in Formeln verwendet, die auf einer anderen Zelle verweisen.'
ms.openlocfilehash: 651b095e53b7f2690aa9c8774d87d5afcede75be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797229"
---
# <a name="iserr-function"></a><span data-ttu-id="dd64f-104">ISERR Function</span><span class="sxs-lookup"><span data-stu-id="dd64f-104">ISERR Function</span></span>

<span data-ttu-id="dd64f-105">Gibt True, wenn der Wert von _Zellbezug_ beliebiger Fehlertyp #n /; Andernfalls wird FALSE zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dd64f-105">Returns TRUE if the value of  _cellreference_ is any error type except #N/A; otherwise, it returns FALSE.</span></span> <span data-ttu-id="dd64f-106">Die Funktion ISERR wird in Formeln verwendet, die auf einer anderen Zelle verweisen.</span><span class="sxs-lookup"><span data-stu-id="dd64f-106">The ISERR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="dd64f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd64f-107">Syntax</span></span>

<span data-ttu-id="dd64f-108">ISERR (** *Zellbezug* **)</span><span class="sxs-lookup"><span data-stu-id="dd64f-108">ISERR(** *cellreference* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="dd64f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd64f-109">Parameters</span></span>

|<span data-ttu-id="dd64f-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="dd64f-110">**Name**</span></span>|<span data-ttu-id="dd64f-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="dd64f-111">**Required/Optional**</span></span>|<span data-ttu-id="dd64f-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="dd64f-112">**Data Type**</span></span>|<span data-ttu-id="dd64f-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dd64f-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="dd64f-114">_Zellbezug_</span><span class="sxs-lookup"><span data-stu-id="dd64f-114">_cellreference_</span></span> <br/> |<span data-ttu-id="dd64f-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="dd64f-115">Required</span></span>  <br/> |<span data-ttu-id="dd64f-116">**String**</span><span class="sxs-lookup"><span data-stu-id="dd64f-116">**String**</span></span> <br/> |<span data-ttu-id="dd64f-117">Bezug auf eine Zelle.</span><span class="sxs-lookup"><span data-stu-id="dd64f-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="dd64f-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dd64f-118">Example 1</span></span>

|<span data-ttu-id="dd64f-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="dd64f-119">**Cell**</span></span>|<span data-ttu-id="dd64f-120">**Formula**</span><span class="sxs-lookup"><span data-stu-id="dd64f-120">**Formula**</span></span>|<span data-ttu-id="dd64f-121">**Zurückgegebener Wert**</span><span class="sxs-lookup"><span data-stu-id="dd64f-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dd64f-122">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="dd64f-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="dd64f-123">=NV( )</span><span class="sxs-lookup"><span data-stu-id="dd64f-123">=NA( )</span></span>  <br/> |<span data-ttu-id="dd64f-124">#N/V!</span><span class="sxs-lookup"><span data-stu-id="dd64f-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="dd64f-125">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="dd64f-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="dd64f-126">=ISERR(Scratch.a1)</span><span class="sxs-lookup"><span data-stu-id="dd64f-126">=ISERR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="dd64f-127">FALSCH</span><span class="sxs-lookup"><span data-stu-id="dd64f-127">FALSE</span></span>  <br/> |
   
<span data-ttu-id="dd64f-p103">Gibt FALSE zurück, da die ISERR-Funktion den Fehler #N/V! nicht erkennt. Verwenden Sie ISERROR, um alle Fehlertypen zu finden.</span><span class="sxs-lookup"><span data-stu-id="dd64f-p103">Returns FALSE because the #N/A! error is not recognized by the ISERR function. Use ISERROR to find all error types.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="dd64f-131">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="dd64f-131">Example 2</span></span>

|<span data-ttu-id="dd64f-132">**Cell**</span><span class="sxs-lookup"><span data-stu-id="dd64f-132">**Cell**</span></span>|<span data-ttu-id="dd64f-133">**Formula**</span><span class="sxs-lookup"><span data-stu-id="dd64f-133">**Formula**</span></span>|<span data-ttu-id="dd64f-134">**Zurückgegebener Wert**</span><span class="sxs-lookup"><span data-stu-id="dd64f-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dd64f-135">Scratch.X1</span><span class="sxs-lookup"><span data-stu-id="dd64f-135">Scratch.X1</span></span>  <br/> |<span data-ttu-id="dd64f-136">="Haus"</span><span class="sxs-lookup"><span data-stu-id="dd64f-136">="House"</span></span>  <br/> |<span data-ttu-id="dd64f-137">#WERT!</span><span class="sxs-lookup"><span data-stu-id="dd64f-137">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="dd64f-138">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="dd64f-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="dd64f-139">=ISERR(Scratch.x1)</span><span class="sxs-lookup"><span data-stu-id="dd64f-139">=ISERR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="dd64f-140">WAHR</span><span class="sxs-lookup"><span data-stu-id="dd64f-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="dd64f-p104">Gibt TRUE zurück, da die Funktion ISERR den Fehler #WERT! erkennt.</span><span class="sxs-lookup"><span data-stu-id="dd64f-p104">Returns TRUE because the #VALUE! error is recognized by the ISERR function.</span></span>
  

