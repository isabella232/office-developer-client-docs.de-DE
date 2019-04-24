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
description: Rundet eine Zahl in Richtung 0 (null), auf die nächste ganze Zahl oder auf die nächste Instanz von Multiple.
ms.openlocfilehash: 7a16a77a990180f34dd7a5706c24ec3232438467
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346179"
---
# <a name="floor-function"></a><span data-ttu-id="15db4-103">FLOOR Function</span><span class="sxs-lookup"><span data-stu-id="15db4-103">FLOOR Function</span></span>

<span data-ttu-id="15db4-104">Rundet eine Zahl in Richtung 0 (null), auf die nächste ganze Zahl oder auf die nächste Instanz von _Multiple_.</span><span class="sxs-lookup"><span data-stu-id="15db4-104">Rounds a number toward 0 (zero), to the next integer, or to the next instance of  _multiple_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="15db4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="15db4-105">Syntax</span></span>

<span data-ttu-id="15db4-106">FLOOR (\* \* *Number* \* \*, \* \* *Multiple* \* \*)</span><span class="sxs-lookup"><span data-stu-id="15db4-106">FLOOR(\*\* *number* \*\*, \*\* *multiple* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="15db4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="15db4-107">Parameters</span></span>

|<span data-ttu-id="15db4-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="15db4-108">**Name**</span></span>|<span data-ttu-id="15db4-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="15db4-109">**Required/Optional**</span></span>|<span data-ttu-id="15db4-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="15db4-110">**Data Type**</span></span>|<span data-ttu-id="15db4-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="15db4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="15db4-112">_Anzahl_</span><span class="sxs-lookup"><span data-stu-id="15db4-112">_number_</span></span> <br/> |<span data-ttu-id="15db4-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="15db4-113">Required</span></span>  <br/> |<span data-ttu-id="15db4-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="15db4-114">**Number**</span></span> <br/> |<span data-ttu-id="15db4-115">Die zu rundende Zahl.</span><span class="sxs-lookup"><span data-stu-id="15db4-115">The number to round.</span></span>  <br/> |
| <span data-ttu-id="15db4-116">_mehrere_</span><span class="sxs-lookup"><span data-stu-id="15db4-116">_multiple_</span></span> <br/> |<span data-ttu-id="15db4-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="15db4-117">Required</span></span>  <br/> |<span data-ttu-id="15db4-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="15db4-118">**Number**</span></span> <br/> |<span data-ttu-id="15db4-119">Das Vielfache, auf das gerundet werden soll.</span><span class="sxs-lookup"><span data-stu-id="15db4-119">The multiple to which to round.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="15db4-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15db4-120">Return value</span></span>

<span data-ttu-id="15db4-121">Zahl</span><span class="sxs-lookup"><span data-stu-id="15db4-121">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="15db4-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15db4-122">Remarks</span></span>

<span data-ttu-id="15db4-123">Wenn _Multiple_ nicht angegeben wird, wird die Zahl in Richtung 0 in die nächste ganze Zahl gerundet.</span><span class="sxs-lookup"><span data-stu-id="15db4-123">If  _multiple_ is not specified, the number rounds toward 0 to the next integer.</span></span> 
  
 <span data-ttu-id="15db4-124">_Zahl_ und _mehrere_ müssen die gleichen Zeichen oder ein #NUM!</span><span class="sxs-lookup"><span data-stu-id="15db4-124">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="15db4-125">zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="15db4-125">error is returned.</span></span> <span data-ttu-id="15db4-126">Wenn eine oder _mehrere_ _Zahlen_ nicht in einen Wert konvertiert werden können, wird ein #VALUE!</span><span class="sxs-lookup"><span data-stu-id="15db4-126">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="15db4-127">zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="15db4-127">error is returned.</span></span> <span data-ttu-id="15db4-128">Wenn eine _Zahl_ oder __ ein Vielfaches 0 ist, ist das Ergebnis 0.</span><span class="sxs-lookup"><span data-stu-id="15db4-128">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="15db4-129">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="15db4-129">Example 1</span></span>

<span data-ttu-id="15db4-130">BODEN (3.7)</span><span class="sxs-lookup"><span data-stu-id="15db4-130">FLOOR(3.7)</span></span>
  
<span data-ttu-id="15db4-131">Gibt 3 zurück.</span><span class="sxs-lookup"><span data-stu-id="15db4-131">Returns 3.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="15db4-132">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="15db4-132">Example 2</span></span>

<span data-ttu-id="15db4-133">FLOOR (-3,7)</span><span class="sxs-lookup"><span data-stu-id="15db4-133">FLOOR(-3.7)</span></span>
  
<span data-ttu-id="15db4-134">Gibt -3 zurück.</span><span class="sxs-lookup"><span data-stu-id="15db4-134">Returns -3.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="15db4-135">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="15db4-135">Example 3</span></span>

<span data-ttu-id="15db4-136">BODEN (3.7, 0,5)</span><span class="sxs-lookup"><span data-stu-id="15db4-136">FLOOR(3.7, 0.5)</span></span>
  
<span data-ttu-id="15db4-137">Gibt 3,5 zurück.</span><span class="sxs-lookup"><span data-stu-id="15db4-137">Returns 3.5.</span></span>
  

