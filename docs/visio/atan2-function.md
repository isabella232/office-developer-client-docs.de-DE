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
description: Gibt den Winkel zwischen dem durch x, y und der Richtung der x-Achse dargestellten Vektor zurück. Das Resultat ist eine Zahl in der aktuellen Maßeinheit für Winkel.
ms.openlocfilehash: 906c024f2a78d6e11c1bbf770c14d04299cadca8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341482"
---
# <a name="atan2-function"></a><span data-ttu-id="fdd9a-104">ATAN2 Function</span><span class="sxs-lookup"><span data-stu-id="fdd9a-104">ATAN2 Function</span></span>

<span data-ttu-id="fdd9a-105">Gibt den Winkel zwischen dem durch *x, y* und der Richtung der *x* -Achse dargestellten Vektor zurück.</span><span class="sxs-lookup"><span data-stu-id="fdd9a-105">Returns the angle between the vector represented by  *x,y*  and the direction of the  *x*  -axis.</span></span> <span data-ttu-id="fdd9a-106">Das Resultat ist eine Zahl in der aktuellen Maßeinheit für Winkel.</span><span class="sxs-lookup"><span data-stu-id="fdd9a-106">The result is a number in the current unit of measure for angles.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="fdd9a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fdd9a-107">Syntax</span></span>

<span data-ttu-id="fdd9a-108">ATAN2 (\* \* *y* \* \*, \* \* *x* \* \*)</span><span class="sxs-lookup"><span data-stu-id="fdd9a-108">ATAN2(\*\* *y* \*\*, \*\* *x* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fdd9a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fdd9a-109">Parameters</span></span>

|<span data-ttu-id="fdd9a-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="fdd9a-110">**Name**</span></span>|<span data-ttu-id="fdd9a-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="fdd9a-111">**Required/Optional**</span></span>|<span data-ttu-id="fdd9a-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="fdd9a-112">**Data Type**</span></span>|<span data-ttu-id="fdd9a-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fdd9a-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fdd9a-114">_y_</span><span class="sxs-lookup"><span data-stu-id="fdd9a-114">_y_</span></span> <br/> |<span data-ttu-id="fdd9a-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fdd9a-115">Required</span></span>  <br/> |<span data-ttu-id="fdd9a-116">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="fdd9a-116">**Numeric**</span></span> <br/> |<span data-ttu-id="fdd9a-117">Der _y_-Wert des Punkts.</span><span class="sxs-lookup"><span data-stu-id="fdd9a-117">The  _y_-value of the point.</span></span>  <br/> |
| <span data-ttu-id="fdd9a-118">_x_</span><span class="sxs-lookup"><span data-stu-id="fdd9a-118">_x_</span></span> <br/> |<span data-ttu-id="fdd9a-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fdd9a-119">Required</span></span>  <br/> |<span data-ttu-id="fdd9a-120">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="fdd9a-120">**Numeric**</span></span> <br/> |<span data-ttu-id="fdd9a-121">Der _x_-Wert des Punkts.</span><span class="sxs-lookup"><span data-stu-id="fdd9a-121">The  _x_-value of the point.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fdd9a-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fdd9a-122">Remarks</span></span>

<span data-ttu-id="fdd9a-123">Der Arctangent ist der Winkel, der von der positiven *x* -Achse gegen den Uhrzeigersinn gemessen wird, zu einer Linie, die den Ursprung (0,0) und den durch *x* und *y* dargestellten Punkt schneidet.</span><span class="sxs-lookup"><span data-stu-id="fdd9a-123">The arctangent is the angle measured counterclockwise from the positive  *x*  -axis to a line that intersects the origin (0,0) and the point represented by  *x*  and  *y*  .</span></span> <span data-ttu-id="fdd9a-124">In Microsoft Visio gibt ATAN2 (0, 0) 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="fdd9a-124">In Microsoft Visio, ATAN2(0,0) returns 0.</span></span> <span data-ttu-id="fdd9a-125">Wenn Sie das Ergebnis von ATAN2 in eine andere Winkelmessung erzwingen möchten, verwenden Sie die DEG-oder die RAD-Funktion.</span><span class="sxs-lookup"><span data-stu-id="fdd9a-125">To force the result of ATAN2 into a different angular measurement, use the DEG or RAD function.</span></span> 
  
<span data-ttu-id="fdd9a-126">Die ATAN2-Funktion ist die antifunktion der TAN-Funktion.</span><span class="sxs-lookup"><span data-stu-id="fdd9a-126">The ATAN2 function is the antifunction of the TAN function.</span></span> <span data-ttu-id="fdd9a-127">Die ATAN2-Funktion gibt den Winkel zurück, dessen Winkel gleich *y* geteilt durch *x* ist.</span><span class="sxs-lookup"><span data-stu-id="fdd9a-127">The ATAN2 function returns the angle whose angle is equal to  *y*  divided by  *x*  .</span></span> <span data-ttu-id="fdd9a-128">Wenn ATAN2 (*y, x*) einen Winkel in einem rechtwinkligen Dreieck darstellt, ist *y* die "Gegenseite" und *x* die benachbarte Seite, sodass die Funktion als atan2 (gegenüber, benachbart) geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="fdd9a-128">If ATAN2(*y,x*) represents an angle in a right triangle,  *y*  is the "opposite side" and  *x*  is the "adjacent side," so the function could be written as ATAN2(opposite,adjacent).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="fdd9a-129">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fdd9a-129">Example 1</span></span>

<span data-ttu-id="fdd9a-130">ATAN2 (1.25, 2.25)</span><span class="sxs-lookup"><span data-stu-id="fdd9a-130">ATAN2(1.25,2.25)</span></span>
  
<span data-ttu-id="fdd9a-131">Gibt 29,0456 deg zurück.</span><span class="sxs-lookup"><span data-stu-id="fdd9a-131">Returns 29.0456 deg</span></span>
  
## <a name="example-2"></a><span data-ttu-id="fdd9a-132">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fdd9a-132">Example 2</span></span>

<span data-ttu-id="fdd9a-133">ATAN2 (1, SQRT (3))</span><span class="sxs-lookup"><span data-stu-id="fdd9a-133">ATAN2(1,SQRT(3))</span></span>
  
<span data-ttu-id="fdd9a-134">Gibt 30 deg zurück.</span><span class="sxs-lookup"><span data-stu-id="fdd9a-134">Returns 30 deg</span></span>
  
## <a name="example-3"></a><span data-ttu-id="fdd9a-135">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="fdd9a-135">Example 3</span></span>

<span data-ttu-id="fdd9a-136">ATAN2 (1, 1)</span><span class="sxs-lookup"><span data-stu-id="fdd9a-136">ATAN2(1,1)</span></span>
  
<span data-ttu-id="fdd9a-137">Gibt 45 deg zurück.</span><span class="sxs-lookup"><span data-stu-id="fdd9a-137">Returns 45 deg</span></span>
  

