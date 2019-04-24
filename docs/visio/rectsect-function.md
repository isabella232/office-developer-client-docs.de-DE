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
description: Berechnet den Bereich eines Rechtecks, das mit x und y verknüpft ist, und gibt eine ganze Zahl zwischen 0 und 4 zurück, die den Sektor angibt.
ms.openlocfilehash: fb7ed37ac498765e21c62d7180413cdbcb932502
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360030"
---
# <a name="rectsect-function"></a><span data-ttu-id="687db-103">RECTSECT Function</span><span class="sxs-lookup"><span data-stu-id="687db-103">RECTSECT Function</span></span>

<span data-ttu-id="687db-104">Berechnet den Bereich eines Rechtecks, das mit *x* und *y* verknüpft ist, und gibt eine ganze Zahl zwischen 0 und 4 zurück, die den Sektor angibt.</span><span class="sxs-lookup"><span data-stu-id="687db-104">Calculates the sector of a rectangle associated with  *x*  and  *y*  and returns an integer 0 to 4, indicating the sector.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="687db-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="687db-105">Syntax</span></span>

<span data-ttu-id="687db-106">RECTSECT (\* \* *Breite* \* \*, \* \* *Höhe* \* \*, \* \* *x* \* \*, \* \* *y* \* \*, \* \* *Option* \* \*)</span><span class="sxs-lookup"><span data-stu-id="687db-106">RECTSECT(\*\* *width* \*\*, \*\* *height* \*\*, \*\* *x* \*\*, \*\* *y* \*\*, \*\* *option* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="687db-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="687db-107">Parameters</span></span>

|<span data-ttu-id="687db-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="687db-108">**Name**</span></span>|<span data-ttu-id="687db-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="687db-109">**Required/Optional**</span></span>|<span data-ttu-id="687db-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="687db-110">**Data Type**</span></span>|<span data-ttu-id="687db-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="687db-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="687db-112">_width_</span><span class="sxs-lookup"><span data-stu-id="687db-112">_width_</span></span> <br/> |<span data-ttu-id="687db-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="687db-113">Required</span></span>  <br/> |<span data-ttu-id="687db-114">**String**</span><span class="sxs-lookup"><span data-stu-id="687db-114">**String**</span></span> <br/> |<span data-ttu-id="687db-115">Die Breite des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="687db-115">Width of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="687db-116">_height_</span><span class="sxs-lookup"><span data-stu-id="687db-116">_height_</span></span> <br/> |<span data-ttu-id="687db-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="687db-117">Required</span></span>  <br/> |<span data-ttu-id="687db-118">**String**</span><span class="sxs-lookup"><span data-stu-id="687db-118">**String**</span></span> <br/> |<span data-ttu-id="687db-119">Die Höhe des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="687db-119">Height of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="687db-120">_x_</span><span class="sxs-lookup"><span data-stu-id="687db-120">_x_</span></span> <br/> |<span data-ttu-id="687db-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="687db-121">Required</span></span>  <br/> |<span data-ttu-id="687db-122">**String**</span><span class="sxs-lookup"><span data-stu-id="687db-122">**String**</span></span> <br/> |<span data-ttu-id="687db-123">Eine x-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="687db-123">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="687db-124">_y_</span><span class="sxs-lookup"><span data-stu-id="687db-124">_y_</span></span> <br/> |<span data-ttu-id="687db-125">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="687db-125">Required</span></span>  <br/> |<span data-ttu-id="687db-126">**String**</span><span class="sxs-lookup"><span data-stu-id="687db-126">**String**</span></span> <br/> |<span data-ttu-id="687db-127">Eine y-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="687db-127">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="687db-128">_Option_</span><span class="sxs-lookup"><span data-stu-id="687db-128">_option_</span></span> <br/> |<span data-ttu-id="687db-129">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="687db-129">Required</span></span>  <br/> |<span data-ttu-id="687db-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="687db-130">**Boolean**</span></span> <br/> |<span data-ttu-id="687db-p101">Gibt an, wie Punkte auf den Diagonalen bewertet werden sollen. Legen Sie als Wert 0 fest, um den linken und rechten Sektor für Punkte auf einer Diagonalen zu verwenden. Legen Sie als Wert 1 fest, um den oberen und unteren Sektor für Punkte auf einer Diagonalen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="687db-p101">Specifies how points that fall on the diagonals are treated. Set the value to 0 to use the left and right sectors for points on a diagonal. Set the value to 1 to use the top and bottom sectors for points on a diagonal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="687db-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="687db-134">Remarks</span></span>

<span data-ttu-id="687db-135">Betrachten Sie ein Rechteck mit einer *Breite* und einer *Höhe* und einen Punkt (*x, y*) vom Mittelpunkt des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="687db-135">Consider a rectangle that has a  *width*  and a  *height*  , and a point (*x,y*) from the center point of the rectangle.</span></span> <span data-ttu-id="687db-136">Zeichnen Sie diagonale Linien durch die Ecken des Rechtecks, um Sie in vier Sektoren und einen Mittelpunkt zu teilen.</span><span class="sxs-lookup"><span data-stu-id="687db-136">Draw diagonal lines through the corners of the rectangle to divide it into four sectors and a center point.</span></span> <span data-ttu-id="687db-137">Die Sektoren 0 bis 4 stellen den Mittelpunkt, rechts, oben, Links und unten dar.</span><span class="sxs-lookup"><span data-stu-id="687db-137">The sectors 0 through 4 represent the center-point, right, top, left, and bottom respectively.</span></span> 
  
![Sektoren 0 bis 4 stellen den Mittelpunkt, rechts, oben, Links und unten dar.](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a><span data-ttu-id="687db-139">Beispiel</span><span class="sxs-lookup"><span data-stu-id="687db-139">Example</span></span>

<span data-ttu-id="687db-140">RECTSECT(1 cm, 2 cm, 1 cm, -7 cm, 0)</span><span class="sxs-lookup"><span data-stu-id="687db-140">RECTSECT(1 in, 2 in, 1 in, -7 in, 0)</span></span> 
  
<span data-ttu-id="687db-141">Gibt 4 zurück.</span><span class="sxs-lookup"><span data-stu-id="687db-141">Returns 4.</span></span> 
  

