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
description: Rundet eine Zahl von 0 (null) zur nächsten Instanz von Multiple ab. Wenn mehrere nicht angegeben ist, wird die Zahl von 0 auf die nächste ganze Zahl gerundet.
ms.openlocfilehash: 449f17d1b68c116cccb2635723a3f6277d0ac2a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337226"
---
# <a name="ceiling-function"></a><span data-ttu-id="8ca53-104">CEILING Function</span><span class="sxs-lookup"><span data-stu-id="8ca53-104">CEILING Function</span></span>

<span data-ttu-id="8ca53-105">Rundet eine Zahl von 0 (null) zur nächsten Instanz von _Multiple_ab.</span><span class="sxs-lookup"><span data-stu-id="8ca53-105">Rounds a number away from 0 (zero) to the next instance of  _multiple_.</span></span> <span data-ttu-id="8ca53-106">Wenn _mehrere_ nicht angegeben ist, wird die Zahl von 0 auf die nächste ganze Zahl gerundet.</span><span class="sxs-lookup"><span data-stu-id="8ca53-106">If  _multiple_ is not specified, the number rounds away from 0 to the next integer.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8ca53-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ca53-107">Syntax</span></span>

<span data-ttu-id="8ca53-108">Obergrenze (\* \* *Number* \* \*, \* \* *Multiple* \* \*)</span><span class="sxs-lookup"><span data-stu-id="8ca53-108">CEILING(\*\* *number* \*\*, \*\* *multiple* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8ca53-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ca53-109">Parameters</span></span>

|<span data-ttu-id="8ca53-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="8ca53-110">**Name**</span></span>|<span data-ttu-id="8ca53-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="8ca53-111">**Required/Optional**</span></span>|<span data-ttu-id="8ca53-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="8ca53-112">**Data Type**</span></span>|<span data-ttu-id="8ca53-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8ca53-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8ca53-114">_Anzahl_</span><span class="sxs-lookup"><span data-stu-id="8ca53-114">_number_</span></span> <br/> |<span data-ttu-id="8ca53-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8ca53-115">Required</span></span>  <br/> |<span data-ttu-id="8ca53-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="8ca53-116">**Number**</span></span> <br/> |<span data-ttu-id="8ca53-117">Die zu rundende Zahl.</span><span class="sxs-lookup"><span data-stu-id="8ca53-117">The number to round.</span></span>  <br/> |
| <span data-ttu-id="8ca53-118">_mehrere_</span><span class="sxs-lookup"><span data-stu-id="8ca53-118">_multiple_</span></span> <br/> |<span data-ttu-id="8ca53-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8ca53-119">Required</span></span>  <br/> |<span data-ttu-id="8ca53-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="8ca53-120">**Number**</span></span> <br/> |<span data-ttu-id="8ca53-121">Das Vielfache, auf das gerundet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ca53-121">The multiple to round to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ca53-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ca53-122">Remarks</span></span>

 <span data-ttu-id="8ca53-123">_Zahl_ und _mehrere_ müssen die gleichen Zeichen oder ein #NUM!</span><span class="sxs-lookup"><span data-stu-id="8ca53-123">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="8ca53-124">zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8ca53-124">error is returned.</span></span> <span data-ttu-id="8ca53-125">Wenn eine oder _mehrere_ _Zahlen_ nicht in einen Wert konvertiert werden können, wird ein #VALUE!</span><span class="sxs-lookup"><span data-stu-id="8ca53-125">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="8ca53-126">zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8ca53-126">error is returned.</span></span> <span data-ttu-id="8ca53-127">Wenn eine _Zahl_ oder __ ein Vielfaches 0 ist, ist das Ergebnis 0.</span><span class="sxs-lookup"><span data-stu-id="8ca53-127">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="8ca53-128">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8ca53-128">Example 1</span></span>

<span data-ttu-id="8ca53-129">OBERGRENZE (3.7)</span><span class="sxs-lookup"><span data-stu-id="8ca53-129">CEILING(3.7)</span></span>
  
<span data-ttu-id="8ca53-130">Gibt 4 zurück.</span><span class="sxs-lookup"><span data-stu-id="8ca53-130">Returns 4</span></span>
  
## <a name="example-2"></a><span data-ttu-id="8ca53-131">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8ca53-131">Example 2</span></span>

<span data-ttu-id="8ca53-132">DECKE (-3,7)</span><span class="sxs-lookup"><span data-stu-id="8ca53-132">CEILING(-3.7)</span></span>
  
<span data-ttu-id="8ca53-133">Gibt -4 zurück.</span><span class="sxs-lookup"><span data-stu-id="8ca53-133">Returns -4</span></span>
  
## <a name="example-3"></a><span data-ttu-id="8ca53-134">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="8ca53-134">Example 3</span></span>

<span data-ttu-id="8ca53-135">OBERGRENZE (3.7, 0,25)</span><span class="sxs-lookup"><span data-stu-id="8ca53-135">CEILING(3.7, 0.25)</span></span>
  
<span data-ttu-id="8ca53-136">Gibt 3,75 zurück.</span><span class="sxs-lookup"><span data-stu-id="8ca53-136">Returns 3.75</span></span>
  

