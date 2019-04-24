---
title: GRAVITY-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251433
localization_priority: Normal
ms.assetid: db80f147-71a0-0b23-bc7e-fe1915dfdd21
description: Berechnet den korrekten Drehwinkel des Textblocks für die angegebene Form Drehung, um zu verhindern, dass der Text auf den Kopf gestellt wird.
ms.openlocfilehash: 77c944d954292e231f8bacbe3c8a4433aad5d689
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360186"
---
# <a name="gravity-function"></a><span data-ttu-id="4df19-103">GRAVITY Function</span><span class="sxs-lookup"><span data-stu-id="4df19-103">GRAVITY Function</span></span>

<span data-ttu-id="4df19-104">Berechnet den korrekten Drehwinkel des Textblocks für die angegebene Form Drehung, um zu verhindern, dass der Text auf den Kopf gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4df19-104">Calculates a text block's correct angle of rotation for the indicated shape rotation to prevent the text from turning upside down.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="4df19-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4df19-105">Syntax</span></span>

<span data-ttu-id="4df19-106">Gravitation (\* \* *Angle* \* *, [* \* *beschränkung1* \* *], [* \* *limit2* \* \*])</span><span class="sxs-lookup"><span data-stu-id="4df19-106">GRAVITY(\*\* *angle* \*\*,[ \*\* *limit1* \*\* ],[ \*\* *limit2* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4df19-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4df19-107">Parameters</span></span>

|<span data-ttu-id="4df19-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="4df19-108">**Name**</span></span>|<span data-ttu-id="4df19-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="4df19-109">**Required/Optional**</span></span>|<span data-ttu-id="4df19-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="4df19-110">**Data Type**</span></span>|<span data-ttu-id="4df19-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4df19-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4df19-112">_Winkel_</span><span class="sxs-lookup"><span data-stu-id="4df19-112">_angle_</span></span> <br/> |<span data-ttu-id="4df19-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="4df19-113">Required</span></span>  <br/> |<span data-ttu-id="4df19-114">**String**</span><span class="sxs-lookup"><span data-stu-id="4df19-114">**String**</span></span> <br/> | <span data-ttu-id="4df19-115">Der Winkel des Shapes.</span><span class="sxs-lookup"><span data-stu-id="4df19-115">The shape's angle.</span></span>  <br/> |
| <span data-ttu-id="4df19-116">_beschränkung1_</span><span class="sxs-lookup"><span data-stu-id="4df19-116">_limit1_</span></span> <br/> |<span data-ttu-id="4df19-117">Optional</span><span class="sxs-lookup"><span data-stu-id="4df19-117">Optional</span></span>  <br/> |<span data-ttu-id="4df19-118">**String**</span><span class="sxs-lookup"><span data-stu-id="4df19-118">**String**</span></span> <br/> |<span data-ttu-id="4df19-119">Erste Drehbegrenzung.</span><span class="sxs-lookup"><span data-stu-id="4df19-119">First limit of rotation.</span></span> <span data-ttu-id="4df19-120">Der Standardwert beträgt 90 Grad.</span><span class="sxs-lookup"><span data-stu-id="4df19-120">Default is 90 degrees.</span></span>  <br/> |
| <span data-ttu-id="4df19-121">_limit2_</span><span class="sxs-lookup"><span data-stu-id="4df19-121">_limit2_</span></span> <br/> |<span data-ttu-id="4df19-122">Optional</span><span class="sxs-lookup"><span data-stu-id="4df19-122">Optional</span></span>  <br/> |<span data-ttu-id="4df19-123">**String**</span><span class="sxs-lookup"><span data-stu-id="4df19-123">**String**</span></span> <br/> |<span data-ttu-id="4df19-124">Zweite Drehbegrenzung.</span><span class="sxs-lookup"><span data-stu-id="4df19-124">Second limit of rotation.</span></span> <span data-ttu-id="4df19-125">Der Standardwert beträgt 270 Grad.</span><span class="sxs-lookup"><span data-stu-id="4df19-125">Default is 270 degrees.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="4df19-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4df19-126">Return value</span></span>

<span data-ttu-id="4df19-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4df19-127">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4df19-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4df19-128">Remarks</span></span>

<span data-ttu-id="4df19-129">Die GRAVITY-Funktion wird gewöhnlich in der Zelle TxtWinkel verwendet.</span><span class="sxs-lookup"><span data-stu-id="4df19-129">The GRAVITY function is usually used in the TxtAngle cell.</span></span> 
  
<span data-ttu-id="4df19-130">Der zurückgegebene Wert ist __ 180 Grad, wenn Angle zwischen den durch _beschränkung1_ und _limit2_angegebenen Werten liegt. Andernfalls ist der zurückgegebene Wert 0 Grad.</span><span class="sxs-lookup"><span data-stu-id="4df19-130">The value returned is 180 degrees if  _angle_ is between the values specified by  _limit1_ and  _limit2_; otherwise the value returned is 0 degrees.</span></span>
  
<span data-ttu-id="4df19-131">Alle Argumente werden von der Funktion automatisch auf einen Wert zwischen 0 und 360 Grad normalisiert.</span><span class="sxs-lookup"><span data-stu-id="4df19-131">All of the arguments are automatically normalized between 0 and 360 degrees by the function.</span></span> <span data-ttu-id="4df19-132">Wenn bei einem Argument keine Einheiten angegeben sind, wird Bogenmaß (Radiant) unterstellt.</span><span class="sxs-lookup"><span data-stu-id="4df19-132">If an argument does not specify units, radians are assumed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="4df19-133">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4df19-133">Example 1</span></span>

<span data-ttu-id="4df19-134">GRAVITATION (Winkel)</span><span class="sxs-lookup"><span data-stu-id="4df19-134">GRAVITY(Angle)</span></span>
  
<span data-ttu-id="4df19-135">Gibt 180 Grad zurück \*\* , wenn Angle zwischen 90 und 270 Grad liegt; Andernfalls gibt 0 Grad zurück.</span><span class="sxs-lookup"><span data-stu-id="4df19-135">Returns 180 degrees if  *angle*  is between 90 and 270 degrees; otherwise, returns 0 degrees.</span></span> 
  
## <a name="example-2"></a><span data-ttu-id="4df19-136">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4df19-136">Example 2</span></span>

<span data-ttu-id="4df19-137">GRAVITATION (2)</span><span class="sxs-lookup"><span data-stu-id="4df19-137">GRAVITY(2)</span></span>
  
<span data-ttu-id="4df19-138">Gibt 180 Grad zurück, da 2 Bogenmaße (Radiant) zwischen 90 und 270 Grad liegen.</span><span class="sxs-lookup"><span data-stu-id="4df19-138">Returns 180 degrees, because 2 radians is between 90 and 270 degrees.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="4df19-139">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="4df19-139">Example 3</span></span>

<span data-ttu-id="4df19-140">GRAVITY(100 deg, 110 deg, 290 deg)</span><span class="sxs-lookup"><span data-stu-id="4df19-140">GRAVITY(100 deg, 110 deg, 290 deg)</span></span>
  
<span data-ttu-id="4df19-141">Gibt 0 Grad zurück.</span><span class="sxs-lookup"><span data-stu-id="4df19-141">Returns 0 degrees.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="4df19-142">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="4df19-142">Example 4</span></span>

<span data-ttu-id="4df19-143">GRAVITY(100 deg, 290 deg, 110 deg)</span><span class="sxs-lookup"><span data-stu-id="4df19-143">GRAVITY(100 deg, 290 deg, 110 deg)</span></span>
  
<span data-ttu-id="4df19-144">Gibt 0 Grad zurück.</span><span class="sxs-lookup"><span data-stu-id="4df19-144">Returns 0 degrees.</span></span>
  

