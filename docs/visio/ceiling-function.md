---
title: CEILING-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251405
localization_priority: Normal
ms.assetid: 1a8d6d48-7ae3-5483-28d2-5b1706088a53
description: Rundet eine Zahl von 0 (Null) in die nächste Instanz des Vielfachen. Wenn multiple nicht angegeben ist, wird die Zahl von 0 zur nächsten ganzen Zahl abgerundet.
ms.openlocfilehash: 449f17d1b68c116cccb2635723a3f6277d0ac2a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404127"
---
# <a name="ceiling-function"></a><span data-ttu-id="48cff-104">CEILING Function</span><span class="sxs-lookup"><span data-stu-id="48cff-104">CEILING Function</span></span>

<span data-ttu-id="48cff-105">Rundet eine Zahl von 0 (Null) zur nächsten Instanz von _mehreren ab._</span><span class="sxs-lookup"><span data-stu-id="48cff-105">Rounds a number away from 0 (zero) to the next instance of  _multiple_.</span></span> <span data-ttu-id="48cff-106">Wenn  _multiple_ nicht angegeben ist, wird die Zahl von 0 zur nächsten ganzen Zahl abgerundet.</span><span class="sxs-lookup"><span data-stu-id="48cff-106">If  _multiple_ is not specified, the number rounds away from 0 to the next integer.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="48cff-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="48cff-107">Syntax</span></span>

<span data-ttu-id="48cff-108">CEILING(\*\* *number* \*\*, \*\* *multiple* \*\* )</span><span class="sxs-lookup"><span data-stu-id="48cff-108">CEILING(\*\* *number* \*\*, \*\* *multiple* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="48cff-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="48cff-109">Parameters</span></span>

|<span data-ttu-id="48cff-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="48cff-110">**Name**</span></span>|<span data-ttu-id="48cff-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="48cff-111">**Required/Optional**</span></span>|<span data-ttu-id="48cff-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="48cff-112">**Data Type**</span></span>|<span data-ttu-id="48cff-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="48cff-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="48cff-114">_Anzahl_</span><span class="sxs-lookup"><span data-stu-id="48cff-114">_number_</span></span> <br/> |<span data-ttu-id="48cff-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="48cff-115">Required</span></span>  <br/> |<span data-ttu-id="48cff-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="48cff-116">**Number**</span></span> <br/> |<span data-ttu-id="48cff-117">Die zu rundende Zahl.</span><span class="sxs-lookup"><span data-stu-id="48cff-117">The number to round.</span></span>  <br/> |
| <span data-ttu-id="48cff-118">_multiple_</span><span class="sxs-lookup"><span data-stu-id="48cff-118">_multiple_</span></span> <br/> |<span data-ttu-id="48cff-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="48cff-119">Required</span></span>  <br/> |<span data-ttu-id="48cff-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="48cff-120">**Number**</span></span> <br/> |<span data-ttu-id="48cff-121">Das Vielfache, mit dem gerundet werden soll.</span><span class="sxs-lookup"><span data-stu-id="48cff-121">The multiple to round to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48cff-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="48cff-122">Remarks</span></span>

 <span data-ttu-id="48cff-123">_Zahl_ und  _Vielfaches_ müssen die gleichen Zeichen haben, oder ein #NUM!</span><span class="sxs-lookup"><span data-stu-id="48cff-123">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="48cff-124">zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="48cff-124">error is returned.</span></span> <span data-ttu-id="48cff-125">Wenn eine  _Zahl oder_  _ein Vielfaches_ nicht in einen Wert konvertiert werden kann, wird #VALUE!</span><span class="sxs-lookup"><span data-stu-id="48cff-125">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="48cff-126">zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="48cff-126">error is returned.</span></span> <span data-ttu-id="48cff-127">Wenn zahl  _oder_  _mehrfach_ 0 ist, ist das Ergebnis 0.</span><span class="sxs-lookup"><span data-stu-id="48cff-127">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="48cff-128">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="48cff-128">Example 1</span></span>

<span data-ttu-id="48cff-129">CEILING(3.7)</span><span class="sxs-lookup"><span data-stu-id="48cff-129">CEILING(3.7)</span></span>
  
<span data-ttu-id="48cff-130">Gibt 4 zurück.</span><span class="sxs-lookup"><span data-stu-id="48cff-130">Returns 4</span></span>
  
## <a name="example-2"></a><span data-ttu-id="48cff-131">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="48cff-131">Example 2</span></span>

<span data-ttu-id="48cff-132">CEILING(-3.7)</span><span class="sxs-lookup"><span data-stu-id="48cff-132">CEILING(-3.7)</span></span>
  
<span data-ttu-id="48cff-133">Gibt -4 zurück.</span><span class="sxs-lookup"><span data-stu-id="48cff-133">Returns -4</span></span>
  
## <a name="example-3"></a><span data-ttu-id="48cff-134">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="48cff-134">Example 3</span></span>

<span data-ttu-id="48cff-135">CEILING(3.7, 0.25)</span><span class="sxs-lookup"><span data-stu-id="48cff-135">CEILING(3.7, 0.25)</span></span>
  
<span data-ttu-id="48cff-136">Gibt 3,75 zurück.</span><span class="sxs-lookup"><span data-stu-id="48cff-136">Returns 3.75</span></span>
  

