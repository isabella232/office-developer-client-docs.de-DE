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
description: Berechnet den Sektor eines Rechtecks zugeordnete x und y und gibt eine Ganzzahl zwischen 0 und 4, der angibt, des Sektors.
ms.openlocfilehash: fb7ed37ac498765e21c62d7180413cdbcb932502
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395084"
---
# <a name="rectsect-function"></a><span data-ttu-id="2b8f7-103">RECTSECT Function</span><span class="sxs-lookup"><span data-stu-id="2b8f7-103">RECTSECT Function</span></span>

<span data-ttu-id="2b8f7-104">Berechnet den Sektor eines Rechtecks *X* und *y* zugeordnet und gibt eine Ganzzahl zwischen 0 und 4, der angibt, des Sektors.</span><span class="sxs-lookup"><span data-stu-id="2b8f7-104">Calculates the sector of a rectangle associated with  *x*  and  *y*  and returns an integer 0 to 4, indicating the sector.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2b8f7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b8f7-105">Syntax</span></span>

<span data-ttu-id="2b8f7-106">RECTSECT (\*\* *Breite* \*\*, \*\* *Höhe* \*\*, \*\* *X* \*\*, \*\* *y* \*\*, \*\* *Option* \*\*)</span><span class="sxs-lookup"><span data-stu-id="2b8f7-106">RECTSECT(\*\* *width* \*\*, \*\* *height* \*\*, \*\* *x* \*\*, \*\* *y* \*\*, \*\* *option* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2b8f7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b8f7-107">Parameters</span></span>

|<span data-ttu-id="2b8f7-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="2b8f7-108">**Name**</span></span>|<span data-ttu-id="2b8f7-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="2b8f7-109">**Required/Optional**</span></span>|<span data-ttu-id="2b8f7-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="2b8f7-110">**Data Type**</span></span>|<span data-ttu-id="2b8f7-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2b8f7-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2b8f7-112">_width_</span><span class="sxs-lookup"><span data-stu-id="2b8f7-112">_width_</span></span> <br/> |<span data-ttu-id="2b8f7-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2b8f7-113">Required</span></span>  <br/> |<span data-ttu-id="2b8f7-114">**String**</span><span class="sxs-lookup"><span data-stu-id="2b8f7-114">**String**</span></span> <br/> |<span data-ttu-id="2b8f7-115">Die Breite des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="2b8f7-115">Width of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="2b8f7-116">_height_</span><span class="sxs-lookup"><span data-stu-id="2b8f7-116">_height_</span></span> <br/> |<span data-ttu-id="2b8f7-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2b8f7-117">Required</span></span>  <br/> |<span data-ttu-id="2b8f7-118">**String**</span><span class="sxs-lookup"><span data-stu-id="2b8f7-118">**String**</span></span> <br/> |<span data-ttu-id="2b8f7-119">Die Höhe des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="2b8f7-119">Height of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="2b8f7-120">_x_</span><span class="sxs-lookup"><span data-stu-id="2b8f7-120">_x_</span></span> <br/> |<span data-ttu-id="2b8f7-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2b8f7-121">Required</span></span>  <br/> |<span data-ttu-id="2b8f7-122">**String**</span><span class="sxs-lookup"><span data-stu-id="2b8f7-122">**String**</span></span> <br/> |<span data-ttu-id="2b8f7-123">Eine x-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="2b8f7-123">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="2b8f7-124">_y_</span><span class="sxs-lookup"><span data-stu-id="2b8f7-124">_y_</span></span> <br/> |<span data-ttu-id="2b8f7-125">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2b8f7-125">Required</span></span>  <br/> |<span data-ttu-id="2b8f7-126">**String**</span><span class="sxs-lookup"><span data-stu-id="2b8f7-126">**String**</span></span> <br/> |<span data-ttu-id="2b8f7-127">Eine y-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="2b8f7-127">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="2b8f7-128">_Option_</span><span class="sxs-lookup"><span data-stu-id="2b8f7-128">_option_</span></span> <br/> |<span data-ttu-id="2b8f7-129">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2b8f7-129">Required</span></span>  <br/> |<span data-ttu-id="2b8f7-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="2b8f7-130">**Boolean**</span></span> <br/> |<span data-ttu-id="2b8f7-p101">Gibt an, wie Punkte auf den Diagonalen bewertet werden sollen. Legen Sie als Wert 0 fest, um den linken und rechten Sektor für Punkte auf einer Diagonalen zu verwenden. Legen Sie als Wert 1 fest, um den oberen und unteren Sektor für Punkte auf einer Diagonalen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2b8f7-p101">Specifies how points that fall on the diagonals are treated. Set the value to 0 to use the left and right sectors for points on a diagonal. Set the value to 1 to use the top and bottom sectors for points on a diagonal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b8f7-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b8f7-134">Remarks</span></span>

<span data-ttu-id="2b8f7-135">Berücksichtigen Sie ein Rechteck mit einer *Breite* und eine *Höhe* und einem Punkt (*X, y*) vom Mittelpunkt des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="2b8f7-135">Consider a rectangle that has a  *width*  and a  *height*  , and a point (*x,y*) from the center point of the rectangle.</span></span> <span data-ttu-id="2b8f7-136">Zeichnen Sie diagonale Linien durch die Ecken des Rechtecks in vier Bereiche und einen Mittelpunkt unterteilen.</span><span class="sxs-lookup"><span data-stu-id="2b8f7-136">Draw diagonal lines through the corners of the rectangle to divide it into four sectors and a center point.</span></span> <span data-ttu-id="2b8f7-137">Sektor 0 bis 4 darstellen der Mittelpunkt, rechts, oben, links und jeweils unten.</span><span class="sxs-lookup"><span data-stu-id="2b8f7-137">The sectors 0 through 4 represent the center-point, right, top, left, and bottom respectively.</span></span> 
  
![Bereiche von 0 bis 4 darstellen der Mittelpunkt, rechts, oben, links und jeweils unten](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a><span data-ttu-id="2b8f7-139">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2b8f7-139">Example</span></span>

<span data-ttu-id="2b8f7-140">RECTSECT(1 cm, 2 cm, 1 cm, -7 cm, 0)</span><span class="sxs-lookup"><span data-stu-id="2b8f7-140">RECTSECT(1 in, 2 in, 1 in, -7 in, 0)</span></span> 
  
<span data-ttu-id="2b8f7-141">Gibt 4 zurück.</span><span class="sxs-lookup"><span data-stu-id="2b8f7-141">Returns 4.</span></span> 
  

