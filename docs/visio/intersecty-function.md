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
description: Gibt die y-Koordinate (im lokalen Koordinatensystem) des Punkts zurück, an dem sich zwei Linien überschneiden.
ms.openlocfilehash: 6fcd06e7086d52b9c45f1deb9d4c191f1a7b1fd2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426100"
---
# <a name="intersecty-function"></a><span data-ttu-id="a510b-103">INTERSECTY Function</span><span class="sxs-lookup"><span data-stu-id="a510b-103">INTERSECTY Function</span></span>

<span data-ttu-id="a510b-104">Gibt die *y* -Koordinate (im lokalen Koordinatensystem) des Punkts zurück, an dem sich zwei Linien überschneiden.</span><span class="sxs-lookup"><span data-stu-id="a510b-104">Returns the  *y*  -coordinate (in the local coordinate system) of the point where two lines intersect.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a510b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a510b-105">Syntax</span></span>

<span data-ttu-id="a510b-106">INTERSECTX-(\* \* *x1* \* \*, \* \* *Y1* \* \*, \* \* *angle1* \* \*, \* \* *x2* \* \*, \* \* *Y2* \* \*, \* \* *angle2* \* \*)</span><span class="sxs-lookup"><span data-stu-id="a510b-106">INTERSECTX(\*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *angle1* \*\*, \*\* *x2* \*\*, \*\* *y2* \*\*, \*\* *angle2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a510b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a510b-107">Parameters</span></span>

|<span data-ttu-id="a510b-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="a510b-108">**Name**</span></span>|<span data-ttu-id="a510b-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="a510b-109">**Required/Optional**</span></span>|<span data-ttu-id="a510b-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a510b-110">**Data Type**</span></span>|<span data-ttu-id="a510b-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a510b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a510b-112">_x1_</span><span class="sxs-lookup"><span data-stu-id="a510b-112">_x1_</span></span> <br/> |<span data-ttu-id="a510b-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a510b-113">Required</span></span>  <br/> |<span data-ttu-id="a510b-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="a510b-114">**Number**</span></span> <br/> |<span data-ttu-id="a510b-115">Die _x_-Koordinate eines Punkts in der ersten Leitung.</span><span class="sxs-lookup"><span data-stu-id="a510b-115">The  _x_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="a510b-116">_Y1_</span><span class="sxs-lookup"><span data-stu-id="a510b-116">_y1_</span></span> <br/> |<span data-ttu-id="a510b-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a510b-117">Required</span></span>  <br/> |<span data-ttu-id="a510b-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="a510b-118">**Number**</span></span> <br/> |<span data-ttu-id="a510b-119">Die _y_-Koordinate eines Punkts in der ersten Leitung.</span><span class="sxs-lookup"><span data-stu-id="a510b-119">The  _y_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="a510b-120">_angle1_</span><span class="sxs-lookup"><span data-stu-id="a510b-120">_angle1_</span></span> <br/> |<span data-ttu-id="a510b-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a510b-121">Required</span></span>  <br/> |<span data-ttu-id="a510b-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="a510b-122">**Number**</span></span> <br/> | <span data-ttu-id="a510b-123">Der Wert der Zelle Winkel für die erste Linie.</span><span class="sxs-lookup"><span data-stu-id="a510b-123">The value of the Angle cell for the first line.</span></span>  <br/> |
| <span data-ttu-id="a510b-124">_x2_</span><span class="sxs-lookup"><span data-stu-id="a510b-124">_x2_</span></span> <br/> |<span data-ttu-id="a510b-125">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a510b-125">Required</span></span>  <br/> |<span data-ttu-id="a510b-126">**Number**</span><span class="sxs-lookup"><span data-stu-id="a510b-126">**Number**</span></span> <br/> |<span data-ttu-id="a510b-127">Die _x_-Koordinate eines Punkts in der zweiten Reihe.</span><span class="sxs-lookup"><span data-stu-id="a510b-127">The  _x_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="a510b-128">_Y2_</span><span class="sxs-lookup"><span data-stu-id="a510b-128">_y2_</span></span> <br/> |<span data-ttu-id="a510b-129">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a510b-129">Required</span></span>  <br/> |<span data-ttu-id="a510b-130">**Number**</span><span class="sxs-lookup"><span data-stu-id="a510b-130">**Number**</span></span> <br/> |<span data-ttu-id="a510b-131">Die _y_-Koordinate eines Punkts in der zweiten Leitung.</span><span class="sxs-lookup"><span data-stu-id="a510b-131">The  _y_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="a510b-132">_angle2_</span><span class="sxs-lookup"><span data-stu-id="a510b-132">_angle2_</span></span> <br/> |<span data-ttu-id="a510b-133">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a510b-133">Required</span></span>  <br/> |<span data-ttu-id="a510b-134">**Number**</span><span class="sxs-lookup"><span data-stu-id="a510b-134">**Number**</span></span> <br/> |<span data-ttu-id="a510b-135">Der Wert der Zelle Winkel für die zweite Linie.</span><span class="sxs-lookup"><span data-stu-id="a510b-135">The value of the Angle cell for the second line.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a510b-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a510b-136">Return value</span></span>

<span data-ttu-id="a510b-137">Zahl</span><span class="sxs-lookup"><span data-stu-id="a510b-137">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a510b-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a510b-138">Remarks</span></span>

<span data-ttu-id="a510b-139">Die einzelnen Linien werden als ein Punkt (*x,y*) und ein Winkel definiert.</span><span class="sxs-lookup"><span data-stu-id="a510b-139">Each line is defined as a point (*x,y*) and an angle.</span></span> 
  
<span data-ttu-id="a510b-140">Von Microsoft Visio wird diese Funktion in der Zelle PinY eines Shapes verwendet, das an eine gedrehte Führungslinie geklebt ist.</span><span class="sxs-lookup"><span data-stu-id="a510b-140">Microsoft Visio uses this function in the PinY cell of a shape glued to a rotated guide.</span></span> 
  
<span data-ttu-id="a510b-141">Weisen die Linien keinen Schnittpunkt auf, gibt die Funktion einen Nullteilungsfehler (#DIV/0!) zurück. Visio ignoriert die Fehlermeldung und stellt den letzten bekannten Wert für den Punkt wieder her.</span><span class="sxs-lookup"><span data-stu-id="a510b-141">If the lines don't intersect, the function returns a divide-by-zero error (#DIV/0!), which Visio ignores, restoring the last known value for the point.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a510b-142">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a510b-142">Example</span></span>

<span data-ttu-id="a510b-143">INTERSECTy (VertFL! PinX, VertFL! PinY, VertFL! Angle, Horzfl! PinX, Horzfl! PinY, Horzfl! Winkel</span><span class="sxs-lookup"><span data-stu-id="a510b-143">INTERSECTY(VertGuide!PinX,VertGuide!PinY,VertGuide!Angle, HorzGuide!PinX,HorzGuide!PinY,HorzGuide!Angle)</span></span> 
  
<span data-ttu-id="a510b-144">Gibt die *y* -Koordinate des Schnittpunkts von VertFL und horzfl in Seiteneinheiten zurück.</span><span class="sxs-lookup"><span data-stu-id="a510b-144">Returns the  *y*  -coordinate of the intersection point of VertGuide and HorzGuide in page units.</span></span> 
  

