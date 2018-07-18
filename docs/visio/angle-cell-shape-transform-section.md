---
title: Zelle "Angle" (Abschnitt "Shape Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251196
localization_priority: Normal
ms.assetid: d05a001c-9001-90d9-5028-f38b90acc53e
description: 'Stellt den tatsächlichen Drehwinkel des Shapes im Verhältnis zu seinem übergeordneten Objekt dar. Die Standardformel zur Bestimmung des Drehwinkels eines 1D-Shapes lautet: =ARCTAN2(EndeY-AnfangY,EndeX-AnfangX).'
ms.openlocfilehash: ff052c5b254f9b49a97f5d362a4643e16a27b85d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796391"
---
# <a name="angle-cell-shape-transform-section"></a><span data-ttu-id="97c9f-104">Angle Cell (Shape Transform Section)</span><span class="sxs-lookup"><span data-stu-id="97c9f-104">Angle Cell (Shape Transform Section)</span></span>

<span data-ttu-id="97c9f-p102">Stellt den tatsächlichen Drehwinkel des Shapes im Verhältnis zu seinem übergeordneten Objekt dar. Die Standardformel zur Bestimmung des Drehwinkels eines 1D-Shapes lautet: =ARCTAN2(EndeY-AnfangY,EndeX-AnfangX).</span><span class="sxs-lookup"><span data-stu-id="97c9f-p102">Represents the shape's current angle of rotation in relation to its parent. The default formula for determining the rotation angle of a 1-D shape is: =ATAN2(EndY-BeginY,EndX-BeginX).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="97c9f-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="97c9f-107">Remarks</span></span>

<span data-ttu-id="97c9f-108">Wenn Sie einen Verweis auf die Zelle Angle aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="97c9f-108">To get a reference to the Angle cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="97c9f-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="97c9f-109">Cell name:</span></span>  <br/> | <span data-ttu-id="97c9f-110">Angle</span><span class="sxs-lookup"><span data-stu-id="97c9f-110">Angle</span></span>  <br/> |
   
<span data-ttu-id="97c9f-111">Wenn Sie einen Verweis auf die Zelle Angle aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="97c9f-111">To get a reference to the Angle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="97c9f-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="97c9f-112">Section index:</span></span>  <br/> |<span data-ttu-id="97c9f-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="97c9f-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="97c9f-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="97c9f-114">Row index:</span></span>  <br/> |<span data-ttu-id="97c9f-115">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="97c9f-115">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="97c9f-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="97c9f-116">Cell index:</span></span>  <br/> |<span data-ttu-id="97c9f-117">**visXFormAngle**</span><span class="sxs-lookup"><span data-stu-id="97c9f-117">**visXFormAngle**</span></span> <br/> |
   

