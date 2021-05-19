---
title: Zelle "LocPinY" (Abschnitt "Shape Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm685
localization_priority: Normal
ms.assetid: a29c5d4e-d3d6-d984-495a-4b0b130352ef
description: 'Stellt die y-Koordinate des Drehpunkts der Form (Drehungsmitte) im Verhältnis zum Ursprung der Form dar. Die Standardformel zum Bestimmen von LocPinY ist:'
ms.openlocfilehash: e65bfec8fdcf2be1ee92c23b7afcb183c95ea9fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410595"
---
# <a name="locpiny-cell-shape-transform-section"></a><span data-ttu-id="65d55-104">Zelle "LocPinY" (Abschnitt "Shape Transform")</span><span class="sxs-lookup"><span data-stu-id="65d55-104">LocPinY Cell (Shape Transform Section)</span></span>

<span data-ttu-id="65d55-105">Stellt  die y-Koordinate des Drehpunkts der Form (Drehungsmitte) im Verhältnis zum Ursprung der Form dar.</span><span class="sxs-lookup"><span data-stu-id="65d55-105">Represents the  *y*  -coordinate of the shape's pin (center of rotation) in relation to the origin of the shape.</span></span> <span data-ttu-id="65d55-106">Die Standardformel zum Bestimmen von LocPinY ist:</span><span class="sxs-lookup"><span data-stu-id="65d55-106">The default formula for determining LocPinY is:</span></span> 
  
<span data-ttu-id="65d55-107">= Höhe \* 0,5</span><span class="sxs-lookup"><span data-stu-id="65d55-107">= Height \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="65d55-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="65d55-108">Remarks</span></span>

<span data-ttu-id="65d55-109">Um einen Verweis auf die LocPinY-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="65d55-109">To get a reference to the LocPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="65d55-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="65d55-110">Cell name:</span></span>  <br/> | <span data-ttu-id="65d55-111">LocPinY</span><span class="sxs-lookup"><span data-stu-id="65d55-111">LocPinY</span></span>  <br/> |
   
<span data-ttu-id="65d55-112">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die LocPinY-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="65d55-112">To get a reference to the LocPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="65d55-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="65d55-113">Section index:</span></span>  <br/> |<span data-ttu-id="65d55-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="65d55-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="65d55-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="65d55-115">Row index:</span></span>  <br/> |<span data-ttu-id="65d55-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="65d55-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="65d55-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="65d55-117">Cell index:</span></span>  <br/> |<span data-ttu-id="65d55-118">**visXFormLocPinY**</span><span class="sxs-lookup"><span data-stu-id="65d55-118">**visXFormLocPinY**</span></span> <br/> |
   

