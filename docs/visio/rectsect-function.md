---
title: RECTSECT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251486
localization_priority: Normal
ms.assetid: e83343c5-df5f-bf74-f854-6380176693a2
description: Berechnet den Sektor eines Rechtecks, das x und y zugeordnet ist, und gibt eine ganze Zahl von 0 bis 4 zurück, die den Sektor angibt.
ms.openlocfilehash: 442ec0d614589c709a097ba314abad044d470df6
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160272"
---
# <a name="rectsect-function"></a><span data-ttu-id="fccbb-103">RECTSECT Function</span><span class="sxs-lookup"><span data-stu-id="fccbb-103">RECTSECT Function</span></span>

<span data-ttu-id="fccbb-104">Berechnet den Sektor eines Rechtecks, das  *x*  und  *y*  zugeordnet ist, und gibt eine ganze Zahl von 0 bis 4 zurück, die den Sektor angibt.</span><span class="sxs-lookup"><span data-stu-id="fccbb-104">Calculates the sector of a rectangle associated with  *x*  and  *y*  and returns an integer 0 to 4, indicating the sector.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="fccbb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fccbb-105">Syntax</span></span>

<span data-ttu-id="fccbb-106">RECTSECT(***width***, ***height***, ***x***, ***y***, ***option*** )</span><span class="sxs-lookup"><span data-stu-id="fccbb-106">RECTSECT(***width***, ***height***, ***x***, ***y***, ***option*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fccbb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fccbb-107">Parameters</span></span>

|<span data-ttu-id="fccbb-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="fccbb-108">**Name**</span></span>|<span data-ttu-id="fccbb-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="fccbb-109">**Required/Optional**</span></span>|<span data-ttu-id="fccbb-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="fccbb-110">**Data Type**</span></span>|<span data-ttu-id="fccbb-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fccbb-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fccbb-112">_width_</span><span class="sxs-lookup"><span data-stu-id="fccbb-112">_width_</span></span> <br/> |<span data-ttu-id="fccbb-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fccbb-113">Required</span></span>  <br/> |<span data-ttu-id="fccbb-114">**String**</span><span class="sxs-lookup"><span data-stu-id="fccbb-114">**String**</span></span> <br/> |<span data-ttu-id="fccbb-115">Die Breite des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="fccbb-115">Width of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="fccbb-116">_height_</span><span class="sxs-lookup"><span data-stu-id="fccbb-116">_height_</span></span> <br/> |<span data-ttu-id="fccbb-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fccbb-117">Required</span></span>  <br/> |<span data-ttu-id="fccbb-118">**String**</span><span class="sxs-lookup"><span data-stu-id="fccbb-118">**String**</span></span> <br/> |<span data-ttu-id="fccbb-119">Die Höhe des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="fccbb-119">Height of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="fccbb-120">_x_</span><span class="sxs-lookup"><span data-stu-id="fccbb-120">_x_</span></span> <br/> |<span data-ttu-id="fccbb-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fccbb-121">Required</span></span>  <br/> |<span data-ttu-id="fccbb-122">**String**</span><span class="sxs-lookup"><span data-stu-id="fccbb-122">**String**</span></span> <br/> |<span data-ttu-id="fccbb-123">Eine x-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="fccbb-123">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="fccbb-124">_y_</span><span class="sxs-lookup"><span data-stu-id="fccbb-124">_y_</span></span> <br/> |<span data-ttu-id="fccbb-125">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fccbb-125">Required</span></span>  <br/> |<span data-ttu-id="fccbb-126">**String**</span><span class="sxs-lookup"><span data-stu-id="fccbb-126">**String**</span></span> <br/> |<span data-ttu-id="fccbb-127">Eine y-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="fccbb-127">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="fccbb-128">_option_</span><span class="sxs-lookup"><span data-stu-id="fccbb-128">_option_</span></span> <br/> |<span data-ttu-id="fccbb-129">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fccbb-129">Required</span></span>  <br/> |<span data-ttu-id="fccbb-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="fccbb-130">**Boolean**</span></span> <br/> |<span data-ttu-id="fccbb-p101">Gibt an, wie Punkte auf den Diagonalen bewertet werden sollen. Legen Sie als Wert 0 fest, um den linken und rechten Sektor für Punkte auf einer Diagonalen zu verwenden. Legen Sie als Wert 1 fest, um den oberen und unteren Sektor für Punkte auf einer Diagonalen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="fccbb-p101">Specifies how points that fall on the diagonals are treated. Set the value to 0 to use the left and right sectors for points on a diagonal. Set the value to 1 to use the top and bottom sectors for points on a diagonal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fccbb-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fccbb-134">Remarks</span></span>

<span data-ttu-id="fccbb-135">Betrachten Sie ein Rechteck, das eine  *Breite*  und eine  *Höhe*  und einen Punkt (*x,y*) vom Mittelpunkt des Rechtecks hat.</span><span class="sxs-lookup"><span data-stu-id="fccbb-135">Consider a rectangle that has a  *width*  and a  *height*  , and a point (*x,y*) from the center point of the rectangle.</span></span> <span data-ttu-id="fccbb-136">Zeichnen Sie diagonale Linien durch die Ecken des Rechtecks, um es in vier Sektoren und einen Mittelpunkt zu teilen.</span><span class="sxs-lookup"><span data-stu-id="fccbb-136">Draw diagonal lines through the corners of the rectangle to divide it into four sectors and a center point.</span></span> <span data-ttu-id="fccbb-137">Die Sektoren 0 bis 4 stellen den Mittelpunkt, rechts, oben, links und unten dar.</span><span class="sxs-lookup"><span data-stu-id="fccbb-137">The sectors 0 through 4 represent the center-point, right, top, left, and bottom respectively.</span></span> 
  
![Die Sektoren 0 bis 4 stellen den Mittelpunkt, rechts, oben, links und unten dar.](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a><span data-ttu-id="fccbb-139">Beispiel</span><span class="sxs-lookup"><span data-stu-id="fccbb-139">Example</span></span>

<span data-ttu-id="fccbb-140">RECTSECT(1 cm, 2 cm, 1 cm, -7 cm, 0)</span><span class="sxs-lookup"><span data-stu-id="fccbb-140">RECTSECT(1 in, 2 in, 1 in, -7 in, 0)</span></span> 
  
<span data-ttu-id="fccbb-141">Gibt 4 zurück.</span><span class="sxs-lookup"><span data-stu-id="fccbb-141">Returns 4.</span></span> 
  

