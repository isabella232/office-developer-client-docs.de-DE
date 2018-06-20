---
title: INTERSECTX-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251444
localization_priority: Normal
ms.assetid: d8dc1915-f055-e858-1323-9e8c1cb7f2f1
description: Gibt das X-Koordinate (im lokalen Koordinatensystem) des Punkts, in dem zwei Linien überschneiden.
ms.openlocfilehash: ea5a08f25f3e45dab3fe3fd83b74cf9a7541b6e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797211"
---
# <a name="intersectx-function"></a><span data-ttu-id="597b3-103">INTERSECTX-Funktion</span><span class="sxs-lookup"><span data-stu-id="597b3-103">INTERSECTX Function</span></span>

<span data-ttu-id="597b3-104">Gibt die *X* -Koordinate (im lokalen Koordinatensystem) des Punkts, in dem zwei Linien überschneiden.</span><span class="sxs-lookup"><span data-stu-id="597b3-104">Returns the  *x*  -coordinate (in the local coordinate system) of the point where two lines intersect.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="597b3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="597b3-105">Syntax</span></span>

<span data-ttu-id="597b3-106">INTERSECTX (** *X1* **, ** *y1* **, ** *Winkel1* **, ** *X2* **, ** *y2* **, ** *Winkel2* **)</span><span class="sxs-lookup"><span data-stu-id="597b3-106">INTERSECTX(** *x1* **, ** *y1* **, ** *angle1* **, ** *x2* **, ** *y2* **, ** *angle2* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="597b3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="597b3-107">Parameters</span></span>

|<span data-ttu-id="597b3-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="597b3-108">**Name**</span></span>|<span data-ttu-id="597b3-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="597b3-109">**Required/Optional**</span></span>|<span data-ttu-id="597b3-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="597b3-110">**Data Type**</span></span>|<span data-ttu-id="597b3-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="597b3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="597b3-112">_x1_</span><span class="sxs-lookup"><span data-stu-id="597b3-112">_x1_</span></span> <br/> |<span data-ttu-id="597b3-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="597b3-113">Required</span></span>  <br/> |<span data-ttu-id="597b3-114">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="597b3-114">**Number**</span></span> <br/> |<span data-ttu-id="597b3-115">Die _X_-Koordinate eines Punkts auf der ersten Linie.</span><span class="sxs-lookup"><span data-stu-id="597b3-115">The  _x_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="597b3-116">_Y1_</span><span class="sxs-lookup"><span data-stu-id="597b3-116">_y1_</span></span> <br/> |<span data-ttu-id="597b3-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="597b3-117">Required</span></span>  <br/> |<span data-ttu-id="597b3-118">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="597b3-118">**Number**</span></span> <br/> |<span data-ttu-id="597b3-119">Die _y_-Koordinate eines Punkts auf der ersten Linie.</span><span class="sxs-lookup"><span data-stu-id="597b3-119">The  _y_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="597b3-120">_Winkel1_</span><span class="sxs-lookup"><span data-stu-id="597b3-120">_angle1_</span></span> <br/> |<span data-ttu-id="597b3-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="597b3-121">Required</span></span>  <br/> |<span data-ttu-id="597b3-122">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="597b3-122">**Number**</span></span> <br/> | <span data-ttu-id="597b3-123">Der Wert der Zelle Winkel für die erste Linie.</span><span class="sxs-lookup"><span data-stu-id="597b3-123">The value of the Angle cell for the first line.</span></span>  <br/> |
| <span data-ttu-id="597b3-124">_x2_</span><span class="sxs-lookup"><span data-stu-id="597b3-124">_x2_</span></span> <br/> |<span data-ttu-id="597b3-125">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="597b3-125">Required</span></span>  <br/> |<span data-ttu-id="597b3-126">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="597b3-126">**Number**</span></span> <br/> |<span data-ttu-id="597b3-127">Die _X_-Koordinate eines Punkts auf der zweiten Linie.</span><span class="sxs-lookup"><span data-stu-id="597b3-127">The  _x_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="597b3-128">_Y2_</span><span class="sxs-lookup"><span data-stu-id="597b3-128">_y2_</span></span> <br/> |<span data-ttu-id="597b3-129">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="597b3-129">Required</span></span>  <br/> |<span data-ttu-id="597b3-130">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="597b3-130">**Number**</span></span> <br/> |<span data-ttu-id="597b3-131">Die _y_-Koordinate eines Punkts auf der zweiten Linie.</span><span class="sxs-lookup"><span data-stu-id="597b3-131">The  _y_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="597b3-132">_Winkel2_</span><span class="sxs-lookup"><span data-stu-id="597b3-132">_angle2_</span></span> <br/> |<span data-ttu-id="597b3-133">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="597b3-133">Required</span></span>  <br/> |<span data-ttu-id="597b3-134">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="597b3-134">**Number**</span></span> <br/> |<span data-ttu-id="597b3-135">Der Wert der Zelle Winkel für die zweite Linie.</span><span class="sxs-lookup"><span data-stu-id="597b3-135">The value of the Angle cell for the second line.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="597b3-136">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="597b3-136">Return value</span></span>

<span data-ttu-id="597b3-137">Zahl</span><span class="sxs-lookup"><span data-stu-id="597b3-137">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="597b3-138">Hinweise</span><span class="sxs-lookup"><span data-stu-id="597b3-138">Remarks</span></span>

<span data-ttu-id="597b3-139">Jede Zeile wird als ein Punkt (*X, y*) und ein Winkel definiert.</span><span class="sxs-lookup"><span data-stu-id="597b3-139">Each line is defined as a point (*x,y*) and an angle.</span></span> 
  
<span data-ttu-id="597b3-140">Von Microsoft Visio wird diese Funktion in der Zelle PinX eines Shapes verwendet, das an eine gedrehte Führungslinie geklebt ist.</span><span class="sxs-lookup"><span data-stu-id="597b3-140">Microsoft Visio uses this function in the PinX cell of a shape glued to a rotated guide.</span></span> 
  
<span data-ttu-id="597b3-141">Weisen die Linien keinen Schnittpunkt auf, gibt die Funktion einen Nullteilungsfehler (#DIV/0!) zurück. Visio ignoriert die Fehlermeldung und stellt den letzten bekannten Wert für den Punkt wieder her.</span><span class="sxs-lookup"><span data-stu-id="597b3-141">If the lines don't intersect, the function returns a divide-by-zero error (#DIV/0!), which Visio ignores, restoring the last known value for the point.</span></span> 
  
## <a name="example"></a><span data-ttu-id="597b3-142">Beispiel</span><span class="sxs-lookup"><span data-stu-id="597b3-142">Example</span></span>

<span data-ttu-id="597b3-143">INTERSECTX (VertFL! DrehbezX VertFL! PinY, VertFL! Winkel, HorzFL! DrehbezX HorzFL! PinY, HorzFL! Winkel)</span><span class="sxs-lookup"><span data-stu-id="597b3-143">INTERSECTX(VertGuide!PinX,VertGuide!PinY,VertGuide!Angle, HorzGuide!PinX,HorzGuide!PinY,HorzGuide!Angle)</span></span> 
  
<span data-ttu-id="597b3-144">Gibt die *X* -Koordinate für den Schnittpunkt von VertFL und HorzFL in Seiteneinheiten.</span><span class="sxs-lookup"><span data-stu-id="597b3-144">Returns the  *x*  -coordinate of the intersection point of VertGuide and HorzGuide in page units.</span></span> 
  

