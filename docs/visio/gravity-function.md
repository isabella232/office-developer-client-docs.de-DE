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
description: Berechnet einen Textblock richtigen Winkel der Drehung für die Drehung der angegebenen Form um zu verhindern, dass den Text auf dem Kopf steht.
ms.openlocfilehash: 0d8b0160c7e7d63fb5a272219a2694d35e6e6b61
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19797110"
---
# <a name="gravity-function"></a><span data-ttu-id="16737-103">GRAVITY Function</span><span class="sxs-lookup"><span data-stu-id="16737-103">GRAVITY Function</span></span>

<span data-ttu-id="16737-104">Berechnet einen Textblock richtigen Winkel der Drehung für die Drehung der angegebenen Form um zu verhindern, dass den Text auf dem Kopf steht.</span><span class="sxs-lookup"><span data-stu-id="16737-104">Calculates a text block's correct angle of rotation for the indicated shape rotation to prevent the text from turning upside down.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="16737-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="16737-105">Syntax</span></span>

<span data-ttu-id="16737-106">GRAVITY (** *Winkel* **, [** *Grenze1* **], [** *Grenze2* **])</span><span class="sxs-lookup"><span data-stu-id="16737-106">GRAVITY(** *angle* **,[ ** *limit1* ** ],[ ** *limit2* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="16737-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="16737-107">Parameters</span></span>

|<span data-ttu-id="16737-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="16737-108">**Name**</span></span>|<span data-ttu-id="16737-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="16737-109">**Required/Optional**</span></span>|<span data-ttu-id="16737-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="16737-110">**Data Type**</span></span>|<span data-ttu-id="16737-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="16737-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="16737-112">_Winkel_</span><span class="sxs-lookup"><span data-stu-id="16737-112">_angle_</span></span> <br/> |<span data-ttu-id="16737-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="16737-113">Required</span></span>  <br/> |<span data-ttu-id="16737-114">**String**</span><span class="sxs-lookup"><span data-stu-id="16737-114">**String**</span></span> <br/> | <span data-ttu-id="16737-115">Der Winkel des Shapes.</span><span class="sxs-lookup"><span data-stu-id="16737-115">The shape's angle.</span></span>  <br/> |
| <span data-ttu-id="16737-116">_Grenze1_</span><span class="sxs-lookup"><span data-stu-id="16737-116">_limit1_</span></span> <br/> |<span data-ttu-id="16737-117">Optional</span><span class="sxs-lookup"><span data-stu-id="16737-117">Optional</span></span>  <br/> |<span data-ttu-id="16737-118">**String**</span><span class="sxs-lookup"><span data-stu-id="16737-118">**String**</span></span> <br/> |<span data-ttu-id="16737-p101">Erste Drehbegrenzung. Der Standardwert beträgt 90 Grad.</span><span class="sxs-lookup"><span data-stu-id="16737-p101">First limit of rotation. Default is 90 degrees.</span></span>  <br/> |
| <span data-ttu-id="16737-121">_Grenze2_</span><span class="sxs-lookup"><span data-stu-id="16737-121">_limit2_</span></span> <br/> |<span data-ttu-id="16737-122">Optional</span><span class="sxs-lookup"><span data-stu-id="16737-122">Optional</span></span>  <br/> |<span data-ttu-id="16737-123">**String**</span><span class="sxs-lookup"><span data-stu-id="16737-123">**String**</span></span> <br/> |<span data-ttu-id="16737-p102">Zweite Drehbegrenzung. Der Standardwert beträgt 270 Grad.</span><span class="sxs-lookup"><span data-stu-id="16737-p102">Second limit of rotation. Default is 270 degrees.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="16737-126">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="16737-126">Return value</span></span>

<span data-ttu-id="16737-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="16737-127">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="16737-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16737-128">Remarks</span></span>

<span data-ttu-id="16737-129">Die GRAVITY-Funktion wird gewöhnlich in der Zelle TxtWinkel verwendet.</span><span class="sxs-lookup"><span data-stu-id="16737-129">The GRAVITY function is usually used in the TxtAngle cell.</span></span> 
  
<span data-ttu-id="16737-130">Der zurückgegebene Wert ist 180 Grad, wenn der _Winkel_ zwischen den _Grenze1_ und _Grenze2_angegebenen Werten liegt. Andernfalls ist der zurückgegebene Wert 0 Grad.</span><span class="sxs-lookup"><span data-stu-id="16737-130">The value returned is 180 degrees if  _angle_ is between the values specified by  _limit1_ and  _limit2_; otherwise the value returned is 0 degrees.</span></span>
  
<span data-ttu-id="16737-p103">Alle Argumente werden von der Funktion automatisch auf einen Wert zwischen 0 und 360 Grad normalisiert. Wenn bei einem Argument keine Einheiten angegeben sind, wird Bogenmaß (Radiant) unterstellt.</span><span class="sxs-lookup"><span data-stu-id="16737-p103">All of the arguments are automatically normalized between 0 and 360 degrees by the function. If an argument does not specify units, radians are assumed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="16737-133">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="16737-133">Example 1</span></span>

<span data-ttu-id="16737-134">GRAVITY(Winkel)</span><span class="sxs-lookup"><span data-stu-id="16737-134">GRAVITY(Angle)</span></span>
  
<span data-ttu-id="16737-135">Gibt 180 Grad, wenn der *Winkel* zwischen 90 und 270 Grad liegt; andernfalls gibt 0 Grad zurück.</span><span class="sxs-lookup"><span data-stu-id="16737-135">Returns 180 degrees if  *angle*  is between 90 and 270 degrees; otherwise, returns 0 degrees.</span></span> 
  
## <a name="example-2"></a><span data-ttu-id="16737-136">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="16737-136">Example 2</span></span>

<span data-ttu-id="16737-137">GRAVITY(2)</span><span class="sxs-lookup"><span data-stu-id="16737-137">GRAVITY(2)</span></span>
  
<span data-ttu-id="16737-138">Gibt 180 Grad zurück, da 2 Bogenmaße (Radiant) zwischen 90 und 270 Grad liegen.</span><span class="sxs-lookup"><span data-stu-id="16737-138">Returns 180 degrees, because 2 radians is between 90 and 270 degrees.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="16737-139">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="16737-139">Example 3</span></span>

<span data-ttu-id="16737-140">GRAVITY(100 deg, 110 deg, 290 deg)</span><span class="sxs-lookup"><span data-stu-id="16737-140">GRAVITY(100 deg, 110 deg, 290 deg)</span></span>
  
<span data-ttu-id="16737-141">Gibt 0 Grad zurück.</span><span class="sxs-lookup"><span data-stu-id="16737-141">Returns 0 degrees.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="16737-142">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="16737-142">Example 4</span></span>

<span data-ttu-id="16737-143">GRAVITY(100 deg, 290 deg, 110 deg)</span><span class="sxs-lookup"><span data-stu-id="16737-143">GRAVITY(100 deg, 290 deg, 110 deg)</span></span>
  
<span data-ttu-id="16737-144">Gibt 0 Grad zurück.</span><span class="sxs-lookup"><span data-stu-id="16737-144">Returns 0 degrees.</span></span>
  

