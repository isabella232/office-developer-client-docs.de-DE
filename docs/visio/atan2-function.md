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
description: Gibt den Winkel zwischen dem Vektor X, y und die Richtung der X-Achse. Das Ergebnis ist eine Zahl in der aktuellen Maßeinheit für Winkel.
ms.openlocfilehash: dfd62ce628a3a46ff14b3ffc3f07074a39c66e14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796395"
---
# <a name="atan2-function"></a><span data-ttu-id="56f44-104">ATAN2 Function</span><span class="sxs-lookup"><span data-stu-id="56f44-104">ATAN2 Function</span></span>

<span data-ttu-id="56f44-105">Gibt den Winkel zwischen dem Vektor *X, y* und die Richtung der *X* -Achse.</span><span class="sxs-lookup"><span data-stu-id="56f44-105">Returns the angle between the vector represented by  *x,y*  and the direction of the  *x*  -axis.</span></span> <span data-ttu-id="56f44-106">Das Ergebnis ist eine Zahl in der aktuellen Maßeinheit für Winkel.</span><span class="sxs-lookup"><span data-stu-id="56f44-106">The result is a number in the current unit of measure for angles.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="56f44-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="56f44-107">Syntax</span></span>

<span data-ttu-id="56f44-108">ATAN2 (** *y* **, ** *X* **)</span><span class="sxs-lookup"><span data-stu-id="56f44-108">ATAN2(** *y* **, ** *x* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="56f44-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="56f44-109">Parameters</span></span>

|<span data-ttu-id="56f44-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="56f44-110">**Name**</span></span>|<span data-ttu-id="56f44-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="56f44-111">**Required/Optional**</span></span>|<span data-ttu-id="56f44-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="56f44-112">**Data Type**</span></span>|<span data-ttu-id="56f44-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="56f44-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="56f44-114">_y_</span><span class="sxs-lookup"><span data-stu-id="56f44-114">_y_</span></span> <br/> |<span data-ttu-id="56f44-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="56f44-115">Required</span></span>  <br/> |<span data-ttu-id="56f44-116">**Numerische**</span><span class="sxs-lookup"><span data-stu-id="56f44-116">**Numeric**</span></span> <br/> |<span data-ttu-id="56f44-117">Die _y_-Wert des Punkts.</span><span class="sxs-lookup"><span data-stu-id="56f44-117">The  _y_-value of the point.</span></span>  <br/> |
| <span data-ttu-id="56f44-118">_x_</span><span class="sxs-lookup"><span data-stu-id="56f44-118">_x_</span></span> <br/> |<span data-ttu-id="56f44-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="56f44-119">Required</span></span>  <br/> |<span data-ttu-id="56f44-120">**Numerische**</span><span class="sxs-lookup"><span data-stu-id="56f44-120">**Numeric**</span></span> <br/> |<span data-ttu-id="56f44-121">Die _X_-Wert des Punkts.</span><span class="sxs-lookup"><span data-stu-id="56f44-121">The  _x_-value of the point.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56f44-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="56f44-122">Remarks</span></span>

<span data-ttu-id="56f44-123">Der Arkustangens ist der Winkel gegen den Uhrzeigersinn gemessen, aus der positiven *X* -Achse zu einer Zeile, die den Ursprung (0,0) und den durch die *x-* und *y* dargestellten Punkt überschneidet.</span><span class="sxs-lookup"><span data-stu-id="56f44-123">The arctangent is the angle measured counterclockwise from the positive  *x*  -axis to a line that intersects the origin (0,0) and the point represented by  *x*  and  *y*  .</span></span> <span data-ttu-id="56f44-124">In Microsoft Visio gibt ATAN2(0,0) den Wert 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="56f44-124">In Microsoft Visio, ATAN2(0,0) returns 0.</span></span> <span data-ttu-id="56f44-125">Um das Ergebnis von ATAN2 in einem anderen Winkelmaß zu erzwingen, verwenden Sie die Funktionen DEG oder RAD.</span><span class="sxs-lookup"><span data-stu-id="56f44-125">To force the result of ATAN2 into a different angular measurement, use the DEG or RAD function.</span></span> 
  
<span data-ttu-id="56f44-126">ATAN2-Funktion ist die Gegenfunktion von TAN-Funktion.</span><span class="sxs-lookup"><span data-stu-id="56f44-126">The ATAN2 function is the antifunction of the TAN function.</span></span> <span data-ttu-id="56f44-127">Die ATAN2-Funktion gibt den Winkel, dessen Tangens gleich *y* geteilt durch *x* ist.</span><span class="sxs-lookup"><span data-stu-id="56f44-127">The ATAN2 function returns the angle whose angle is equal to  *y*  divided by  *x*  .</span></span> <span data-ttu-id="56f44-128">Wenn ATAN2 (*y, X*) stellt einen Winkel in ein rechtwinkliges Dreieck und *y* ist die "gegenüberliegenden Seite" *X* ist der "angrenzenden Seite", damit die Funktion auch als ATAN2(Gegenkathete,Ankathete) geschrieben werden könnte.</span><span class="sxs-lookup"><span data-stu-id="56f44-128">If ATAN2(*y,x*) represents an angle in a right triangle,  *y*  is the "opposite side" and  *x*  is the "adjacent side," so the function could be written as ATAN2(opposite,adjacent).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="56f44-129">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="56f44-129">Example 1</span></span>

<span data-ttu-id="56f44-130">ATAN2(1.25,2.25)</span><span class="sxs-lookup"><span data-stu-id="56f44-130">ATAN2(1.25,2.25)</span></span>
  
<span data-ttu-id="56f44-131">Gibt 29,0456 deg zurück.</span><span class="sxs-lookup"><span data-stu-id="56f44-131">Returns 29.0456 deg</span></span>
  
## <a name="example-2"></a><span data-ttu-id="56f44-132">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="56f44-132">Example 2</span></span>

<span data-ttu-id="56f44-133">ATAN2(1,WURZEL(3))</span><span class="sxs-lookup"><span data-stu-id="56f44-133">ATAN2(1,SQRT(3))</span></span>
  
<span data-ttu-id="56f44-134">Gibt 30 deg zurück.</span><span class="sxs-lookup"><span data-stu-id="56f44-134">Returns 30 deg</span></span>
  
## <a name="example-3"></a><span data-ttu-id="56f44-135">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="56f44-135">Example 3</span></span>

<span data-ttu-id="56f44-136">ATAN2(1,1)</span><span class="sxs-lookup"><span data-stu-id="56f44-136">ATAN2(1,1)</span></span>
  
<span data-ttu-id="56f44-137">Gibt 45 deg zurück.</span><span class="sxs-lookup"><span data-stu-id="56f44-137">Returns 45 deg</span></span>
  

