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
description: Berechnet den richtigen Drehwinkel eines Textblocks für die angegebene Formdrehung, um zu verhindern, dass der Text auf den Kopf gestellt wird.
ms.openlocfilehash: 77c944d954292e231f8bacbe3c8a4433aad5d689
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429285"
---
# <a name="gravity-function"></a><span data-ttu-id="efead-103">GRAVITY Function</span><span class="sxs-lookup"><span data-stu-id="efead-103">GRAVITY Function</span></span>

<span data-ttu-id="efead-104">Berechnet den richtigen Drehwinkel eines Textblocks für die angegebene Formdrehung, um zu verhindern, dass der Text auf den Kopf gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="efead-104">Calculates a text block's correct angle of rotation for the indicated shape rotation to prevent the text from turning upside down.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="efead-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="efead-105">Syntax</span></span>

<span data-ttu-id="efead-106">GRAVITY(\*\* *angle* **,[ \*\* *limit1* \*\* ],[** *limit2* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="efead-106">GRAVITY(\*\* *angle* \*\*,[ \*\* *limit1* \*\* ],[ \*\* *limit2* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="efead-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="efead-107">Parameters</span></span>

|<span data-ttu-id="efead-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="efead-108">**Name**</span></span>|<span data-ttu-id="efead-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="efead-109">**Required/Optional**</span></span>|<span data-ttu-id="efead-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="efead-110">**Data Type**</span></span>|<span data-ttu-id="efead-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="efead-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="efead-112">_angle_</span><span class="sxs-lookup"><span data-stu-id="efead-112">_angle_</span></span> <br/> |<span data-ttu-id="efead-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="efead-113">Required</span></span>  <br/> |<span data-ttu-id="efead-114">**String**</span><span class="sxs-lookup"><span data-stu-id="efead-114">**String**</span></span> <br/> | <span data-ttu-id="efead-115">Der Winkel des Shapes.</span><span class="sxs-lookup"><span data-stu-id="efead-115">The shape's angle.</span></span>  <br/> |
| <span data-ttu-id="efead-116">_limit1_</span><span class="sxs-lookup"><span data-stu-id="efead-116">_limit1_</span></span> <br/> |<span data-ttu-id="efead-117">Optional</span><span class="sxs-lookup"><span data-stu-id="efead-117">Optional</span></span>  <br/> |<span data-ttu-id="efead-118">**String**</span><span class="sxs-lookup"><span data-stu-id="efead-118">**String**</span></span> <br/> |<span data-ttu-id="efead-p101">Erste Drehbegrenzung. Der Standardwert beträgt 90 Grad.</span><span class="sxs-lookup"><span data-stu-id="efead-p101">First limit of rotation. Default is 90 degrees.</span></span>  <br/> |
| <span data-ttu-id="efead-121">_limit2_</span><span class="sxs-lookup"><span data-stu-id="efead-121">_limit2_</span></span> <br/> |<span data-ttu-id="efead-122">Optional</span><span class="sxs-lookup"><span data-stu-id="efead-122">Optional</span></span>  <br/> |<span data-ttu-id="efead-123">**String**</span><span class="sxs-lookup"><span data-stu-id="efead-123">**String**</span></span> <br/> |<span data-ttu-id="efead-p102">Zweite Drehbegrenzung. Der Standardwert beträgt 270 Grad.</span><span class="sxs-lookup"><span data-stu-id="efead-p102">Second limit of rotation. Default is 270 degrees.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="efead-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="efead-126">Return value</span></span>

<span data-ttu-id="efead-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="efead-127">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="efead-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="efead-128">Remarks</span></span>

<span data-ttu-id="efead-129">Die GRAVITY-Funktion wird gewöhnlich in der Zelle TxtWinkel verwendet.</span><span class="sxs-lookup"><span data-stu-id="efead-129">The GRAVITY function is usually used in the TxtAngle cell.</span></span> 
  
<span data-ttu-id="efead-130">Der zurückgegebene Wert beträgt 180 Grad, wenn der Winkel zwischen den durch _limit1_ und limit2 angegebenen _Werten liegt._  Andernfalls beträgt der zurückgegebene Wert 0 Grad.</span><span class="sxs-lookup"><span data-stu-id="efead-130">The value returned is 180 degrees if  _angle_ is between the values specified by  _limit1_ and  _limit2_; otherwise the value returned is 0 degrees.</span></span>
  
<span data-ttu-id="efead-p103">Alle Argumente werden von der Funktion automatisch auf einen Wert zwischen 0 und 360 Grad normalisiert. Wenn bei einem Argument keine Einheiten angegeben sind, wird Bogenmaß (Radiant) unterstellt.</span><span class="sxs-lookup"><span data-stu-id="efead-p103">All of the arguments are automatically normalized between 0 and 360 degrees by the function. If an argument does not specify units, radians are assumed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="efead-133">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="efead-133">Example 1</span></span>

<span data-ttu-id="efead-134">GRAVITY(Angle)</span><span class="sxs-lookup"><span data-stu-id="efead-134">GRAVITY(Angle)</span></span>
  
<span data-ttu-id="efead-135">Gibt 180 Grad zurück,  *wenn der Winkel*  zwischen 90 und 270 Grad liegt. Andernfalls werden 0 Grad zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="efead-135">Returns 180 degrees if  *angle*  is between 90 and 270 degrees; otherwise, returns 0 degrees.</span></span> 
  
## <a name="example-2"></a><span data-ttu-id="efead-136">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="efead-136">Example 2</span></span>

<span data-ttu-id="efead-137">GRAVITY(2)</span><span class="sxs-lookup"><span data-stu-id="efead-137">GRAVITY(2)</span></span>
  
<span data-ttu-id="efead-138">Gibt 180 Grad zurück, da 2 Bogenmaße (Radiant) zwischen 90 und 270 Grad liegen.</span><span class="sxs-lookup"><span data-stu-id="efead-138">Returns 180 degrees, because 2 radians is between 90 and 270 degrees.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="efead-139">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="efead-139">Example 3</span></span>

<span data-ttu-id="efead-140">GRAVITY(100 deg, 110 deg, 290 deg)</span><span class="sxs-lookup"><span data-stu-id="efead-140">GRAVITY(100 deg, 110 deg, 290 deg)</span></span>
  
<span data-ttu-id="efead-141">Gibt 0 Grad zurück.</span><span class="sxs-lookup"><span data-stu-id="efead-141">Returns 0 degrees.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="efead-142">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="efead-142">Example 4</span></span>

<span data-ttu-id="efead-143">GRAVITY(100 deg, 290 deg, 110 deg)</span><span class="sxs-lookup"><span data-stu-id="efead-143">GRAVITY(100 deg, 290 deg, 110 deg)</span></span>
  
<span data-ttu-id="efead-144">Gibt 0 Grad zurück.</span><span class="sxs-lookup"><span data-stu-id="efead-144">Returns 0 degrees.</span></span>
  

