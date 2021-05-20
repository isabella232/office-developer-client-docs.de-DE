---
title: ATAN2-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251397
localization_priority: Normal
ms.assetid: 524278fb-196e-9cf9-e27b-d03642beeee4
description: Gibt den Winkel zwischen dem durch x,y dargestellten Vektor und der Richtung der x-Achse zurück. Das Resultat ist eine Zahl in der aktuellen Maßeinheit für Winkel.
ms.openlocfilehash: 906c024f2a78d6e11c1bbf770c14d04299cadca8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436482"
---
# <a name="atan2-function"></a><span data-ttu-id="a9bed-104">ATAN2 Function</span><span class="sxs-lookup"><span data-stu-id="a9bed-104">ATAN2 Function</span></span>

<span data-ttu-id="a9bed-105">Gibt den Winkel zwischen dem durch  *x,y*  dargestellten Vektor und der Richtung der  *x-Achse*  zurück.</span><span class="sxs-lookup"><span data-stu-id="a9bed-105">Returns the angle between the vector represented by  *x,y*  and the direction of the  *x*  -axis.</span></span> <span data-ttu-id="a9bed-106">Das Resultat ist eine Zahl in der aktuellen Maßeinheit für Winkel.</span><span class="sxs-lookup"><span data-stu-id="a9bed-106">The result is a number in the current unit of measure for angles.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a9bed-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9bed-107">Syntax</span></span>

<span data-ttu-id="a9bed-108">ATAN2(\*\* *y* \*\*, \*\* *x* \*\* )</span><span class="sxs-lookup"><span data-stu-id="a9bed-108">ATAN2(\*\* *y* \*\*, \*\* *x* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a9bed-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9bed-109">Parameters</span></span>

|<span data-ttu-id="a9bed-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="a9bed-110">**Name**</span></span>|<span data-ttu-id="a9bed-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="a9bed-111">**Required/Optional**</span></span>|<span data-ttu-id="a9bed-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a9bed-112">**Data Type**</span></span>|<span data-ttu-id="a9bed-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a9bed-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a9bed-114">_y_</span><span class="sxs-lookup"><span data-stu-id="a9bed-114">_y_</span></span> <br/> |<span data-ttu-id="a9bed-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a9bed-115">Required</span></span>  <br/> |<span data-ttu-id="a9bed-116">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="a9bed-116">**Numeric**</span></span> <br/> |<span data-ttu-id="a9bed-117">Der  _y-Wert_ des Punkts.</span><span class="sxs-lookup"><span data-stu-id="a9bed-117">The  _y_-value of the point.</span></span>  <br/> |
| <span data-ttu-id="a9bed-118">_x_</span><span class="sxs-lookup"><span data-stu-id="a9bed-118">_x_</span></span> <br/> |<span data-ttu-id="a9bed-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a9bed-119">Required</span></span>  <br/> |<span data-ttu-id="a9bed-120">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="a9bed-120">**Numeric**</span></span> <br/> |<span data-ttu-id="a9bed-121">Der  _x-Wert_ des Punkts.</span><span class="sxs-lookup"><span data-stu-id="a9bed-121">The  _x_-value of the point.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9bed-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a9bed-122">Remarks</span></span>

<span data-ttu-id="a9bed-123">Das arctangent ist der Winkel, der gegen den Uhrzeigersinn von der positiven *x-Achse* zu einer Linie gemessen wird, die den Ursprung (0,0) und den durch *x* und y dargestellten Punkt *überschneidet.*</span><span class="sxs-lookup"><span data-stu-id="a9bed-123">The arctangent is the angle measured counterclockwise from the positive  *x*  -axis to a line that intersects the origin (0,0) and the point represented by  *x*  and  *y*  .</span></span> <span data-ttu-id="a9bed-124">Atan2(0,0) gibt in Microsoft Visio 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="a9bed-124">In Microsoft Visio, ATAN2(0,0) returns 0.</span></span> <span data-ttu-id="a9bed-125">Verwenden Sie die DEG- oder RAD-Funktion, um das Ergebnis von ATAN2 in eine andere Winkelmessung zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="a9bed-125">To force the result of ATAN2 into a different angular measurement, use the DEG or RAD function.</span></span> 
  
<span data-ttu-id="a9bed-126">Die ATAN2-Funktion ist die Antifunktion der TAN-Funktion.</span><span class="sxs-lookup"><span data-stu-id="a9bed-126">The ATAN2 function is the antifunction of the TAN function.</span></span> <span data-ttu-id="a9bed-127">Die ATAN2-Funktion gibt den Winkel zurück, dessen Winkel *y* dividiert durch *x ist.*</span><span class="sxs-lookup"><span data-stu-id="a9bed-127">The ATAN2 function returns the angle whose angle is equal to  *y*  divided by  *x*  .</span></span> <span data-ttu-id="a9bed-128">Wenn ATAN2(*y,x*) einen Winkel in einem rechten Dreieck darstellt,  *ist y*  die "gegenüberliegende Seite" und  *x*  die "angrenzende Seite", sodass die Funktion als ATAN2(gegenüber, nebenan) geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="a9bed-128">If ATAN2(*y,x*) represents an angle in a right triangle,  *y*  is the "opposite side" and  *x*  is the "adjacent side," so the function could be written as ATAN2(opposite,adjacent).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="a9bed-129">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a9bed-129">Example 1</span></span>

<span data-ttu-id="a9bed-130">ATAN2(1.25,2.25)</span><span class="sxs-lookup"><span data-stu-id="a9bed-130">ATAN2(1.25,2.25)</span></span>
  
<span data-ttu-id="a9bed-131">Gibt 29,0456 deg zurück.</span><span class="sxs-lookup"><span data-stu-id="a9bed-131">Returns 29.0456 deg</span></span>
  
## <a name="example-2"></a><span data-ttu-id="a9bed-132">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a9bed-132">Example 2</span></span>

<span data-ttu-id="a9bed-133">ATAN2(1,SQRT(3))</span><span class="sxs-lookup"><span data-stu-id="a9bed-133">ATAN2(1,SQRT(3))</span></span>
  
<span data-ttu-id="a9bed-134">Gibt 30 deg zurück.</span><span class="sxs-lookup"><span data-stu-id="a9bed-134">Returns 30 deg</span></span>
  
## <a name="example-3"></a><span data-ttu-id="a9bed-135">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a9bed-135">Example 3</span></span>

<span data-ttu-id="a9bed-136">ATAN2(1,1)</span><span class="sxs-lookup"><span data-stu-id="a9bed-136">ATAN2(1,1)</span></span>
  
<span data-ttu-id="a9bed-137">Gibt 45 deg zurück.</span><span class="sxs-lookup"><span data-stu-id="a9bed-137">Returns 45 deg</span></span>
  

