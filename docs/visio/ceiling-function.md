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
description: Rundet eine Zahl von 0 (null) auf die nächste Instanz von Vielfaches. Wenn Multiple nicht angegeben wurde, wird die Zahl von 0 auf die nächste ganze Zahl gerundet.
ms.openlocfilehash: fa982b44ea4a73e7da614c49a52cd50efd612f20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796578"
---
# <a name="ceiling-function"></a><span data-ttu-id="61e7b-104">CEILING Function</span><span class="sxs-lookup"><span data-stu-id="61e7b-104">CEILING Function</span></span>

<span data-ttu-id="61e7b-105">Rundet eine Zahl von 0 (null) auf die nächste Instanz von _Vielfaches_.</span><span class="sxs-lookup"><span data-stu-id="61e7b-105">Rounds a number away from 0 (zero) to the next instance of  _multiple_.</span></span> <span data-ttu-id="61e7b-106">Wenn _mehrere_ nicht angegeben ist, wird die Anzahl von 0 auf die nächste ganze Zahl gerundet.</span><span class="sxs-lookup"><span data-stu-id="61e7b-106">If  _multiple_ is not specified, the number rounds away from 0 to the next integer.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="61e7b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="61e7b-107">Syntax</span></span>

<span data-ttu-id="61e7b-108">CEILING (** *Anzahl* **, ** *mehrere* **)</span><span class="sxs-lookup"><span data-stu-id="61e7b-108">CEILING(** *number* **, ** *multiple* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="61e7b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="61e7b-109">Parameters</span></span>

|<span data-ttu-id="61e7b-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="61e7b-110">**Name**</span></span>|<span data-ttu-id="61e7b-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="61e7b-111">**Required/Optional**</span></span>|<span data-ttu-id="61e7b-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="61e7b-112">**Data Type**</span></span>|<span data-ttu-id="61e7b-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="61e7b-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="61e7b-114">_Anzahl_</span><span class="sxs-lookup"><span data-stu-id="61e7b-114">_number_</span></span> <br/> |<span data-ttu-id="61e7b-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="61e7b-115">Required</span></span>  <br/> |<span data-ttu-id="61e7b-116">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="61e7b-116">**Number**</span></span> <br/> |<span data-ttu-id="61e7b-117">Die zu rundende Zahl.</span><span class="sxs-lookup"><span data-stu-id="61e7b-117">The number to round.</span></span>  <br/> |
| <span data-ttu-id="61e7b-118">_mehrere_</span><span class="sxs-lookup"><span data-stu-id="61e7b-118">_multiple_</span></span> <br/> |<span data-ttu-id="61e7b-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="61e7b-119">Required</span></span>  <br/> |<span data-ttu-id="61e7b-120">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="61e7b-120">**Number**</span></span> <br/> |<span data-ttu-id="61e7b-121">Das Vielfache, auf die gerundet werden soll.</span><span class="sxs-lookup"><span data-stu-id="61e7b-121">The multiple to round to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61e7b-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61e7b-122">Remarks</span></span>

 <span data-ttu-id="61e7b-123">_Anzahl_ und _Vielfaches_ müssen die gleichen Vorzeichen oder ein #NUM haben.</span><span class="sxs-lookup"><span data-stu-id="61e7b-123">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="61e7b-124">Fehler wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="61e7b-124">error is returned.</span></span> <span data-ttu-id="61e7b-125">Wenn _Zahl_ oder _mehrere_ auf einen Wert, der ein #VALUE konvertiert werden kann!</span><span class="sxs-lookup"><span data-stu-id="61e7b-125">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="61e7b-126">Fehler wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="61e7b-126">error is returned.</span></span> <span data-ttu-id="61e7b-127">Wenn _Zahl_ oder _mehrere_ 0 ist, ist das Ergebnis 0.</span><span class="sxs-lookup"><span data-stu-id="61e7b-127">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="61e7b-128">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="61e7b-128">Example 1</span></span>

<span data-ttu-id="61e7b-129">CEILING(3.7)</span><span class="sxs-lookup"><span data-stu-id="61e7b-129">CEILING(3.7)</span></span>
  
<span data-ttu-id="61e7b-130">Gibt 4 zurück.</span><span class="sxs-lookup"><span data-stu-id="61e7b-130">Returns 4</span></span>
  
## <a name="example-2"></a><span data-ttu-id="61e7b-131">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="61e7b-131">Example 2</span></span>

<span data-ttu-id="61e7b-132">CEILING(-3.7)</span><span class="sxs-lookup"><span data-stu-id="61e7b-132">CEILING(-3.7)</span></span>
  
<span data-ttu-id="61e7b-133">Gibt -4 zurück.</span><span class="sxs-lookup"><span data-stu-id="61e7b-133">Returns -4</span></span>
  
## <a name="example-3"></a><span data-ttu-id="61e7b-134">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="61e7b-134">Example 3</span></span>

<span data-ttu-id="61e7b-135">CEILING (3.7, 0,25)</span><span class="sxs-lookup"><span data-stu-id="61e7b-135">CEILING(3.7, 0.25)</span></span>
  
<span data-ttu-id="61e7b-136">Gibt 3,75 zurück.</span><span class="sxs-lookup"><span data-stu-id="61e7b-136">Returns 3.75</span></span>
  

