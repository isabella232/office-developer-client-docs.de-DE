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
description: Berechnet den Bereich eines mit x und y verknüpften Rechtecks und gibt eine ganze Zahl von 0 bis 4 zurück, die den Sektor angibt.
ms.openlocfilehash: 442ec0d614589c709a097ba314abad044d470df6
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160272"
---
# <a name="rectsect-function"></a><span data-ttu-id="87fe3-103">RECTSECT Function</span><span class="sxs-lookup"><span data-stu-id="87fe3-103">RECTSECT Function</span></span>

<span data-ttu-id="87fe3-104">Berechnet den Bereich eines mit *x* und *y* verknüpften Rechtecks und gibt eine ganze Zahl von 0 bis 4 zurück, die den Sektor angibt.</span><span class="sxs-lookup"><span data-stu-id="87fe3-104">Calculates the sector of a rectangle associated with  *x*  and  *y*  and returns an integer 0 to 4, indicating the sector.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="87fe3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="87fe3-105">Syntax</span></span>

<span data-ttu-id="87fe3-106">RECTSECT (***Breite***, ***Höhe***, ***x***, ***y***, ***Option*** )</span><span class="sxs-lookup"><span data-stu-id="87fe3-106">RECTSECT(***width***, ***height***, ***x***, ***y***, ***option*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="87fe3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="87fe3-107">Parameters</span></span>

|<span data-ttu-id="87fe3-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="87fe3-108">**Name**</span></span>|<span data-ttu-id="87fe3-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="87fe3-109">**Required/Optional**</span></span>|<span data-ttu-id="87fe3-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="87fe3-110">**Data Type**</span></span>|<span data-ttu-id="87fe3-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="87fe3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="87fe3-112">_width_</span><span class="sxs-lookup"><span data-stu-id="87fe3-112">_width_</span></span> <br/> |<span data-ttu-id="87fe3-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="87fe3-113">Required</span></span>  <br/> |<span data-ttu-id="87fe3-114">**String**</span><span class="sxs-lookup"><span data-stu-id="87fe3-114">**String**</span></span> <br/> |<span data-ttu-id="87fe3-115">Die Breite des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="87fe3-115">Width of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="87fe3-116">_height_</span><span class="sxs-lookup"><span data-stu-id="87fe3-116">_height_</span></span> <br/> |<span data-ttu-id="87fe3-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="87fe3-117">Required</span></span>  <br/> |<span data-ttu-id="87fe3-118">**String**</span><span class="sxs-lookup"><span data-stu-id="87fe3-118">**String**</span></span> <br/> |<span data-ttu-id="87fe3-119">Die Höhe des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="87fe3-119">Height of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="87fe3-120">_x_</span><span class="sxs-lookup"><span data-stu-id="87fe3-120">_x_</span></span> <br/> |<span data-ttu-id="87fe3-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="87fe3-121">Required</span></span>  <br/> |<span data-ttu-id="87fe3-122">**String**</span><span class="sxs-lookup"><span data-stu-id="87fe3-122">**String**</span></span> <br/> |<span data-ttu-id="87fe3-123">Eine x-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="87fe3-123">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="87fe3-124">_y_</span><span class="sxs-lookup"><span data-stu-id="87fe3-124">_y_</span></span> <br/> |<span data-ttu-id="87fe3-125">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="87fe3-125">Required</span></span>  <br/> |<span data-ttu-id="87fe3-126">**String**</span><span class="sxs-lookup"><span data-stu-id="87fe3-126">**String**</span></span> <br/> |<span data-ttu-id="87fe3-127">Eine y-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="87fe3-127">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="87fe3-128">_Option_</span><span class="sxs-lookup"><span data-stu-id="87fe3-128">_option_</span></span> <br/> |<span data-ttu-id="87fe3-129">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="87fe3-129">Required</span></span>  <br/> |<span data-ttu-id="87fe3-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="87fe3-130">**Boolean**</span></span> <br/> |<span data-ttu-id="87fe3-p101">Gibt an, wie Punkte auf den Diagonalen bewertet werden sollen. Legen Sie als Wert 0 fest, um den linken und rechten Sektor für Punkte auf einer Diagonalen zu verwenden. Legen Sie als Wert 1 fest, um den oberen und unteren Sektor für Punkte auf einer Diagonalen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="87fe3-p101">Specifies how points that fall on the diagonals are treated. Set the value to 0 to use the left and right sectors for points on a diagonal. Set the value to 1 to use the top and bottom sectors for points on a diagonal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87fe3-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87fe3-134">Remarks</span></span>

<span data-ttu-id="87fe3-135">Stellen Sie sich ein Rechteck mit einer *Breite* und einer *Höhe* sowie einen Punkt (*x, y*) vom Mittelpunkt des Rechtecks vor.</span><span class="sxs-lookup"><span data-stu-id="87fe3-135">Consider a rectangle that has a  *width*  and a  *height*  , and a point (*x,y*) from the center point of the rectangle.</span></span> <span data-ttu-id="87fe3-136">Zeichnen Sie diagonale Linien durch die Ecken des Rechtecks, um Sie in vier Sektoren und einen Mittelpunkt zu unterteilen.</span><span class="sxs-lookup"><span data-stu-id="87fe3-136">Draw diagonal lines through the corners of the rectangle to divide it into four sectors and a center point.</span></span> <span data-ttu-id="87fe3-137">Die Sektoren 0 bis 4 stellen den Mittelpunkt, den rechten, oberen, linken und unteren Teil dar.</span><span class="sxs-lookup"><span data-stu-id="87fe3-137">The sectors 0 through 4 represent the center-point, right, top, left, and bottom respectively.</span></span> 
  
![Die Sektoren 0 bis 4 stellen den Mittelpunkt, den rechten, oberen, linken und unteren Bereich dar.](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a><span data-ttu-id="87fe3-139">Beispiel</span><span class="sxs-lookup"><span data-stu-id="87fe3-139">Example</span></span>

<span data-ttu-id="87fe3-140">RECTSECT(1 cm, 2 cm, 1 cm, -7 cm, 0)</span><span class="sxs-lookup"><span data-stu-id="87fe3-140">RECTSECT(1 in, 2 in, 1 in, -7 in, 0)</span></span> 
  
<span data-ttu-id="87fe3-141">Gibt 4 zurück.</span><span class="sxs-lookup"><span data-stu-id="87fe3-141">Returns 4.</span></span> 
  

