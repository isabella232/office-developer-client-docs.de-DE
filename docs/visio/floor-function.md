---
title: FLOOR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251423
localization_priority: Normal
ms.assetid: 6788bc96-cc86-5f21-781f-67274e7f605a
description: Rundet eine Zahl in Richtung 0 (Null), zur nächsten ganzen Zahl oder zur nächsten Instanz von mehreren.
ms.openlocfilehash: 7a16a77a990180f34dd7a5706c24ec3232438467
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439898"
---
# <a name="floor-function"></a><span data-ttu-id="5ae12-103">FLOOR Function</span><span class="sxs-lookup"><span data-stu-id="5ae12-103">FLOOR Function</span></span>

<span data-ttu-id="5ae12-104">Rundet eine Zahl in Richtung 0 (Null), zur nächsten ganzen Zahl oder zur nächsten Instanz von _mehreren ._</span><span class="sxs-lookup"><span data-stu-id="5ae12-104">Rounds a number toward 0 (zero), to the next integer, or to the next instance of  _multiple_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5ae12-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ae12-105">Syntax</span></span>

<span data-ttu-id="5ae12-106">FLOOR(\*\* *number* \*\*, \*\* *multiple* \*\* )</span><span class="sxs-lookup"><span data-stu-id="5ae12-106">FLOOR(\*\* *number* \*\*, \*\* *multiple* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5ae12-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ae12-107">Parameters</span></span>

|<span data-ttu-id="5ae12-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="5ae12-108">**Name**</span></span>|<span data-ttu-id="5ae12-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="5ae12-109">**Required/Optional**</span></span>|<span data-ttu-id="5ae12-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="5ae12-110">**Data Type**</span></span>|<span data-ttu-id="5ae12-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5ae12-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5ae12-112">_Anzahl_</span><span class="sxs-lookup"><span data-stu-id="5ae12-112">_number_</span></span> <br/> |<span data-ttu-id="5ae12-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5ae12-113">Required</span></span>  <br/> |<span data-ttu-id="5ae12-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="5ae12-114">**Number**</span></span> <br/> |<span data-ttu-id="5ae12-115">Die zu rundende Zahl.</span><span class="sxs-lookup"><span data-stu-id="5ae12-115">The number to round.</span></span>  <br/> |
| <span data-ttu-id="5ae12-116">_multiple_</span><span class="sxs-lookup"><span data-stu-id="5ae12-116">_multiple_</span></span> <br/> |<span data-ttu-id="5ae12-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5ae12-117">Required</span></span>  <br/> |<span data-ttu-id="5ae12-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="5ae12-118">**Number**</span></span> <br/> |<span data-ttu-id="5ae12-119">Das Vielfache, auf das gerundet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5ae12-119">The multiple to which to round.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5ae12-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ae12-120">Return value</span></span>

<span data-ttu-id="5ae12-121">Nummer</span><span class="sxs-lookup"><span data-stu-id="5ae12-121">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5ae12-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5ae12-122">Remarks</span></span>

<span data-ttu-id="5ae12-123">Wenn  _nicht multiple_ angegeben ist, wird die Zahl in Richtung 0 zur nächsten ganzen Zahl gerundet.</span><span class="sxs-lookup"><span data-stu-id="5ae12-123">If  _multiple_ is not specified, the number rounds toward 0 to the next integer.</span></span> 
  
 <span data-ttu-id="5ae12-124">_Zahl_ und  _Vielfaches_ müssen die gleichen Zeichen haben, oder ein #NUM!</span><span class="sxs-lookup"><span data-stu-id="5ae12-124">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="5ae12-125">zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5ae12-125">error is returned.</span></span> <span data-ttu-id="5ae12-126">Wenn eine  _Zahl oder_  _ein Vielfaches_ nicht in einen Wert konvertiert werden kann, wird #VALUE!</span><span class="sxs-lookup"><span data-stu-id="5ae12-126">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="5ae12-127">zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5ae12-127">error is returned.</span></span> <span data-ttu-id="5ae12-128">Wenn zahl  _oder_  _mehrfach_ 0 ist, ist das Ergebnis 0.</span><span class="sxs-lookup"><span data-stu-id="5ae12-128">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="5ae12-129">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5ae12-129">Example 1</span></span>

<span data-ttu-id="5ae12-130">FLOOR(3.7)</span><span class="sxs-lookup"><span data-stu-id="5ae12-130">FLOOR(3.7)</span></span>
  
<span data-ttu-id="5ae12-131">Gibt 3 zurück.</span><span class="sxs-lookup"><span data-stu-id="5ae12-131">Returns 3.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="5ae12-132">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5ae12-132">Example 2</span></span>

<span data-ttu-id="5ae12-133">FLOOR(-3.7)</span><span class="sxs-lookup"><span data-stu-id="5ae12-133">FLOOR(-3.7)</span></span>
  
<span data-ttu-id="5ae12-134">Gibt -3 zurück.</span><span class="sxs-lookup"><span data-stu-id="5ae12-134">Returns -3.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="5ae12-135">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5ae12-135">Example 3</span></span>

<span data-ttu-id="5ae12-136">FLOOR(3.7, 0.5)</span><span class="sxs-lookup"><span data-stu-id="5ae12-136">FLOOR(3.7, 0.5)</span></span>
  
<span data-ttu-id="5ae12-137">Gibt 3,5 zurück.</span><span class="sxs-lookup"><span data-stu-id="5ae12-137">Returns 3.5.</span></span>
  

