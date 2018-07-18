---
title: INTERSECTY-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251445
localization_priority: Normal
ms.assetid: a298eead-044b-6f40-54c7-e0e6088baa19
description: Gibt die y-Koordinate (im lokalen Koordinatensystem) des Punkts, in dem zwei Linien überschneiden.
ms.openlocfilehash: c3c0e9afef317ed4c647f1d236c4c3a29c6cdaa6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797214"
---
# <a name="intersecty-function"></a><span data-ttu-id="9b527-103">INTERSECTY Function</span><span class="sxs-lookup"><span data-stu-id="9b527-103">INTERSECTY Function</span></span>

<span data-ttu-id="9b527-104">Gibt die *y* -Koordinate (im lokalen Koordinatensystem) des Punkts, in dem zwei Linien überschneiden.</span><span class="sxs-lookup"><span data-stu-id="9b527-104">Returns the  *y*  -coordinate (in the local coordinate system) of the point where two lines intersect.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9b527-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b527-105">Syntax</span></span>

<span data-ttu-id="9b527-106">INTERSECTX (** *X1* **, ** *y1* **, ** *Winkel1* **, ** *X2* **, ** *y2* **, ** *Winkel2* **)</span><span class="sxs-lookup"><span data-stu-id="9b527-106">INTERSECTX(** *x1* **, ** *y1* **, ** *angle1* **, ** *x2* **, ** *y2* **, ** *angle2* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9b527-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b527-107">Parameters</span></span>

|<span data-ttu-id="9b527-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="9b527-108">**Name**</span></span>|<span data-ttu-id="9b527-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="9b527-109">**Required/Optional**</span></span>|<span data-ttu-id="9b527-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="9b527-110">**Data Type**</span></span>|<span data-ttu-id="9b527-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9b527-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9b527-112">_x1_</span><span class="sxs-lookup"><span data-stu-id="9b527-112">_x1_</span></span> <br/> |<span data-ttu-id="9b527-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="9b527-113">Required</span></span>  <br/> |<span data-ttu-id="9b527-114">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="9b527-114">**Number**</span></span> <br/> |<span data-ttu-id="9b527-115">Die _X_-Koordinate eines Punkts auf der ersten Linie.</span><span class="sxs-lookup"><span data-stu-id="9b527-115">The  _x_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="9b527-116">_Y1_</span><span class="sxs-lookup"><span data-stu-id="9b527-116">_y1_</span></span> <br/> |<span data-ttu-id="9b527-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="9b527-117">Required</span></span>  <br/> |<span data-ttu-id="9b527-118">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="9b527-118">**Number**</span></span> <br/> |<span data-ttu-id="9b527-119">Die _y_-Koordinate eines Punkts auf der ersten Linie.</span><span class="sxs-lookup"><span data-stu-id="9b527-119">The  _y_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="9b527-120">_Winkel1_</span><span class="sxs-lookup"><span data-stu-id="9b527-120">_angle1_</span></span> <br/> |<span data-ttu-id="9b527-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="9b527-121">Required</span></span>  <br/> |<span data-ttu-id="9b527-122">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="9b527-122">**Number**</span></span> <br/> | <span data-ttu-id="9b527-123">Der Wert der Zelle Winkel für die erste Linie.</span><span class="sxs-lookup"><span data-stu-id="9b527-123">The value of the Angle cell for the first line.</span></span>  <br/> |
| <span data-ttu-id="9b527-124">_x2_</span><span class="sxs-lookup"><span data-stu-id="9b527-124">_x2_</span></span> <br/> |<span data-ttu-id="9b527-125">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="9b527-125">Required</span></span>  <br/> |<span data-ttu-id="9b527-126">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="9b527-126">**Number**</span></span> <br/> |<span data-ttu-id="9b527-127">Die _X_-Koordinate eines Punkts auf der zweiten Linie.</span><span class="sxs-lookup"><span data-stu-id="9b527-127">The  _x_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="9b527-128">_Y2_</span><span class="sxs-lookup"><span data-stu-id="9b527-128">_y2_</span></span> <br/> |<span data-ttu-id="9b527-129">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="9b527-129">Required</span></span>  <br/> |<span data-ttu-id="9b527-130">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="9b527-130">**Number**</span></span> <br/> |<span data-ttu-id="9b527-131">Die _y_-Koordinate eines Punkts auf der zweiten Linie.</span><span class="sxs-lookup"><span data-stu-id="9b527-131">The  _y_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="9b527-132">_Winkel2_</span><span class="sxs-lookup"><span data-stu-id="9b527-132">_angle2_</span></span> <br/> |<span data-ttu-id="9b527-133">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="9b527-133">Required</span></span>  <br/> |<span data-ttu-id="9b527-134">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="9b527-134">**Number**</span></span> <br/> |<span data-ttu-id="9b527-135">Der Wert der Zelle Winkel für die zweite Linie.</span><span class="sxs-lookup"><span data-stu-id="9b527-135">The value of the Angle cell for the second line.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="9b527-136">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="9b527-136">Return value</span></span>

<span data-ttu-id="9b527-137">Zahl</span><span class="sxs-lookup"><span data-stu-id="9b527-137">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9b527-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b527-138">Remarks</span></span>

<span data-ttu-id="9b527-139">Die einzelnen Linien werden als ein Punkt (*x,y*) und ein Winkel definiert.</span><span class="sxs-lookup"><span data-stu-id="9b527-139">Each line is defined as a point (*x,y*) and an angle.</span></span> 
  
<span data-ttu-id="9b527-140">Von Microsoft Visio wird diese Funktion in der Zelle PinY eines Shapes verwendet, das an eine gedrehte Führungslinie geklebt ist.</span><span class="sxs-lookup"><span data-stu-id="9b527-140">Microsoft Visio uses this function in the PinY cell of a shape glued to a rotated guide.</span></span> 
  
<span data-ttu-id="9b527-141">Weisen die Linien keinen Schnittpunkt auf, gibt die Funktion einen Nullteilungsfehler (#DIV/0!) zurück. Visio ignoriert die Fehlermeldung und stellt den letzten bekannten Wert für den Punkt wieder her.</span><span class="sxs-lookup"><span data-stu-id="9b527-141">If the lines don't intersect, the function returns a divide-by-zero error (#DIV/0!), which Visio ignores, restoring the last known value for the point.</span></span> 
  
## <a name="example"></a><span data-ttu-id="9b527-142">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9b527-142">Example</span></span>

<span data-ttu-id="9b527-143">INTERSECTY (VertFL! DrehbezX VertFL! PinY, VertFL! Winkel, HorzFL! DrehbezX HorzFL! PinY, HorzFL! Winkel)</span><span class="sxs-lookup"><span data-stu-id="9b527-143">INTERSECTY(VertGuide!PinX,VertGuide!PinY,VertGuide!Angle, HorzGuide!PinX,HorzGuide!PinY,HorzGuide!Angle)</span></span> 
  
<span data-ttu-id="9b527-144">Gibt die *y* -Koordinate für den Schnittpunkt von VertFL und HorzFL in Seiteneinheiten.</span><span class="sxs-lookup"><span data-stu-id="9b527-144">Returns the  *y*  -coordinate of the intersection point of VertGuide and HorzGuide in page units.</span></span> 
  

