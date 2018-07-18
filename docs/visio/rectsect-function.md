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
ms.openlocfilehash: 1f35704cdb827c9c751f11593436c110755d7777
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797772"
---
# <a name="rectsect-function"></a><span data-ttu-id="1359c-103">RECTSECT Function</span><span class="sxs-lookup"><span data-stu-id="1359c-103">RECTSECT Function</span></span>

<span data-ttu-id="1359c-104">Berechnet den Sektor eines Rechtecks *X* und *y* zugeordnet und gibt eine Ganzzahl zwischen 0 und 4, der angibt, des Sektors.</span><span class="sxs-lookup"><span data-stu-id="1359c-104">Calculates the sector of a rectangle associated with  *x*  and  *y*  and returns an integer 0 to 4, indicating the sector.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1359c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1359c-105">Syntax</span></span>

<span data-ttu-id="1359c-106">RECTSECT (** *Breite* **, ** *Höhe* **, ** *X* **, ** *y* **, ** *Option* **)</span><span class="sxs-lookup"><span data-stu-id="1359c-106">RECTSECT(** *width* **, ** *height* **, ** *x* **, ** *y* **, ** *option* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1359c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1359c-107">Parameters</span></span>

|<span data-ttu-id="1359c-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="1359c-108">**Name**</span></span>|<span data-ttu-id="1359c-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="1359c-109">**Required/Optional**</span></span>|<span data-ttu-id="1359c-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="1359c-110">**Data Type**</span></span>|<span data-ttu-id="1359c-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1359c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1359c-112">_width_</span><span class="sxs-lookup"><span data-stu-id="1359c-112">_width_</span></span> <br/> |<span data-ttu-id="1359c-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="1359c-113">Required</span></span>  <br/> |<span data-ttu-id="1359c-114">**String**</span><span class="sxs-lookup"><span data-stu-id="1359c-114">**String**</span></span> <br/> |<span data-ttu-id="1359c-115">Die Breite des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="1359c-115">Width of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="1359c-116">_height_</span><span class="sxs-lookup"><span data-stu-id="1359c-116">_height_</span></span> <br/> |<span data-ttu-id="1359c-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="1359c-117">Required</span></span>  <br/> |<span data-ttu-id="1359c-118">**String**</span><span class="sxs-lookup"><span data-stu-id="1359c-118">**String**</span></span> <br/> |<span data-ttu-id="1359c-119">Die Höhe des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="1359c-119">Height of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="1359c-120">_x_</span><span class="sxs-lookup"><span data-stu-id="1359c-120">_x_</span></span> <br/> |<span data-ttu-id="1359c-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="1359c-121">Required</span></span>  <br/> |<span data-ttu-id="1359c-122">**String**</span><span class="sxs-lookup"><span data-stu-id="1359c-122">**String**</span></span> <br/> |<span data-ttu-id="1359c-123">Eine x-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="1359c-123">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="1359c-124">_y_</span><span class="sxs-lookup"><span data-stu-id="1359c-124">_y_</span></span> <br/> |<span data-ttu-id="1359c-125">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="1359c-125">Required</span></span>  <br/> |<span data-ttu-id="1359c-126">**String**</span><span class="sxs-lookup"><span data-stu-id="1359c-126">**String**</span></span> <br/> |<span data-ttu-id="1359c-127">Eine y-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="1359c-127">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="1359c-128">_Option_</span><span class="sxs-lookup"><span data-stu-id="1359c-128">_option_</span></span> <br/> |<span data-ttu-id="1359c-129">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="1359c-129">Required</span></span>  <br/> |<span data-ttu-id="1359c-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="1359c-130">**Boolean**</span></span> <br/> |<span data-ttu-id="1359c-p101">Gibt an, wie Punkte auf den Diagonalen bewertet werden sollen. Legen Sie als Wert 0 fest, um den linken und rechten Sektor für Punkte auf einer Diagonalen zu verwenden. Legen Sie als Wert 1 fest, um den oberen und unteren Sektor für Punkte auf einer Diagonalen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1359c-p101">Specifies how points that fall on the diagonals are treated. Set the value to 0 to use the left and right sectors for points on a diagonal. Set the value to 1 to use the top and bottom sectors for points on a diagonal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1359c-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1359c-134">Remarks</span></span>

<span data-ttu-id="1359c-135">Berücksichtigen Sie ein Rechteck mit einer *Breite* und eine *Höhe* und einem Punkt (*X, y*) vom Mittelpunkt des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="1359c-135">Consider a rectangle that has a  *width*  and a  *height*  , and a point (*x,y*) from the center point of the rectangle.</span></span> <span data-ttu-id="1359c-136">Zeichnen Sie diagonale Linien durch die Ecken des Rechtecks in vier Bereiche und einen Mittelpunkt unterteilen.</span><span class="sxs-lookup"><span data-stu-id="1359c-136">Draw diagonal lines through the corners of the rectangle to divide it into four sectors and a center point.</span></span> <span data-ttu-id="1359c-137">Sektor 0 bis 4 darstellen der Mittelpunkt, rechts, oben, links und jeweils unten.</span><span class="sxs-lookup"><span data-stu-id="1359c-137">The sectors 0 through 4 represent the center-point, right, top, left, and bottom respectively.</span></span> 
  
![](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a><span data-ttu-id="1359c-138">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1359c-138">Example</span></span>

<span data-ttu-id="1359c-139">RECTSECT(1 cm, 2 cm, 1 cm, -7 cm, 0)</span><span class="sxs-lookup"><span data-stu-id="1359c-139">RECTSECT(1 in, 2 in, 1 in, -7 in, 0)</span></span> 
  
<span data-ttu-id="1359c-140">Gibt 4 zurück.</span><span class="sxs-lookup"><span data-stu-id="1359c-140">Returns 4.</span></span> 
  

