---
title: MODULUS-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251465
localization_priority: Normal
ms.assetid: cb6326a5-1bf8-b6a3-5c0d-d38c071353a5
description: Gibt den Rest (Modulo) zurück, der ergibt, wenn eine Zahl durch einen Divisor geteilt wird.
ms.openlocfilehash: f6b713b1b3a9d2afa85f49de9d451642a00d8dad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356994"
---
# <a name="modulus-function"></a><span data-ttu-id="35793-103">MODULUS Function</span><span class="sxs-lookup"><span data-stu-id="35793-103">MODULUS Function</span></span>

<span data-ttu-id="35793-104">Gibt den Rest (Modulo) zurück, der ergibt, wenn eine Zahl durch einen Divisor geteilt wird.</span><span class="sxs-lookup"><span data-stu-id="35793-104">Returns the remainder (modulus) that results when a number is divided by a divisor.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="35793-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="35793-105">Syntax</span></span>

<span data-ttu-id="35793-106">MODULo (\* \* *Number* \* \*, \* \* *Divisor* \* \*)</span><span class="sxs-lookup"><span data-stu-id="35793-106">MODULUS(\*\* *number* \*\*, \*\* *divisor* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="35793-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="35793-107">Parameters</span></span>

|<span data-ttu-id="35793-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="35793-108">**Name**</span></span>|<span data-ttu-id="35793-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="35793-109">**Required/Optional**</span></span>|<span data-ttu-id="35793-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="35793-110">**Data Type**</span></span>|<span data-ttu-id="35793-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="35793-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="35793-112">_Anzahl_</span><span class="sxs-lookup"><span data-stu-id="35793-112">_number_</span></span> <br/> |<span data-ttu-id="35793-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="35793-113">Required</span></span>  <br/> |<span data-ttu-id="35793-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="35793-114">**Number**</span></span> <br/> |<span data-ttu-id="35793-115">Der Dividend.</span><span class="sxs-lookup"><span data-stu-id="35793-115">The dividend.</span></span>  <br/> |
| <span data-ttu-id="35793-116">_Divisor_</span><span class="sxs-lookup"><span data-stu-id="35793-116">_divisor_</span></span> <br/> |<span data-ttu-id="35793-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="35793-117">Required</span></span>  <br/> |<span data-ttu-id="35793-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="35793-118">**Number**</span></span> <br/> |<span data-ttu-id="35793-119">Der Divisor.</span><span class="sxs-lookup"><span data-stu-id="35793-119">The divisor.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="35793-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35793-120">Return value</span></span>

<span data-ttu-id="35793-121">Zahl</span><span class="sxs-lookup"><span data-stu-id="35793-121">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="35793-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35793-122">Remarks</span></span>

<span data-ttu-id="35793-p101">Das Ergebnis hat das gleiche Vorzeichen wie der Divisor. Wenn der Divisor 0 ist, wird der Fehler #DIV/0! zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="35793-p101">The result has the same sign as the divisor. A #DIV/0! error is returned if the divisor is 0.</span></span> 
  
<span data-ttu-id="35793-126">In fast allen Situationen sollte die MODULUS-Funktion gegenüber der MOD-Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="35793-126">In almost all situations, the MODULUS function should be used rather than the MOD function.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="35793-127">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="35793-127">Example 1</span></span>

<span data-ttu-id="35793-128">MODULUS(5, 1,4)</span><span class="sxs-lookup"><span data-stu-id="35793-128">MODULUS(5, 1.4)</span></span>
  
<span data-ttu-id="35793-129">Gibt 0,8 zurück.</span><span class="sxs-lookup"><span data-stu-id="35793-129">Returns 0.8.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="35793-130">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="35793-130">Example 2</span></span>

<span data-ttu-id="35793-131">MODULUS(5, -1,4)</span><span class="sxs-lookup"><span data-stu-id="35793-131">MODULUS(5, -1.4)</span></span>
  
<span data-ttu-id="35793-132">Gibt -0,6 zurück.</span><span class="sxs-lookup"><span data-stu-id="35793-132">Returns -0.6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="35793-133">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="35793-133">Example 3</span></span>

<span data-ttu-id="35793-134">MODULUS(-5, 1,4)</span><span class="sxs-lookup"><span data-stu-id="35793-134">MODULUS(-5, 1.4)</span></span>
  
<span data-ttu-id="35793-135">Gibt 0,6 zurück.</span><span class="sxs-lookup"><span data-stu-id="35793-135">Returns 0.6.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="35793-136">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="35793-136">Example 4</span></span>

<span data-ttu-id="35793-137">MODULUS(-5, -1,4)</span><span class="sxs-lookup"><span data-stu-id="35793-137">MODULUS(-5, -1.4)</span></span>
  
<span data-ttu-id="35793-138">Gibt -0,8 zurück.</span><span class="sxs-lookup"><span data-stu-id="35793-138">Returns -0.8.</span></span>
  

