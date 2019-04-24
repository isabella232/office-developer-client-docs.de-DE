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
ms.openlocfilehash: 85f64c6111b492940d278a5558508a2dea6b1e1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341468"
---
# <a name="angle-cell-shape-transform-section"></a><span data-ttu-id="bf8a0-104">Zelle "Angle" (Abschnitt "Shape Transform")</span><span class="sxs-lookup"><span data-stu-id="bf8a0-104">Angle Cell (Shape Transform Section)</span></span>

<span data-ttu-id="bf8a0-p102">Stellt den tatsächlichen Drehwinkel des Shapes im Verhältnis zu seinem übergeordneten Objekt dar. Die Standardformel zur Bestimmung des Drehwinkels eines 1D-Shapes lautet: =ARCTAN2(EndeY-AnfangY,EndeX-AnfangX).</span><span class="sxs-lookup"><span data-stu-id="bf8a0-p102">Represents the shape's current angle of rotation in relation to its parent. The default formula for determining the rotation angle of a 1-D shape is: =ATAN2(EndY-BeginY,EndX-BeginX).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bf8a0-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf8a0-107">Remarks</span></span>

<span data-ttu-id="bf8a0-108">Wenn Sie einen Verweis auf die Zelle Angle aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="bf8a0-108">To get a reference to the Angle cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bf8a0-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="bf8a0-109">Cell name:</span></span>  <br/> | <span data-ttu-id="bf8a0-110">Winkel</span><span class="sxs-lookup"><span data-stu-id="bf8a0-110">Angle</span></span>  <br/> |
   
<span data-ttu-id="bf8a0-111">Wenn Sie einen Verweis auf die Zelle "Angle" aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="bf8a0-111">To get a reference to the Angle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bf8a0-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="bf8a0-112">Section index:</span></span>  <br/> |<span data-ttu-id="bf8a0-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bf8a0-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bf8a0-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="bf8a0-114">Row index:</span></span>  <br/> |<span data-ttu-id="bf8a0-115">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="bf8a0-115">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="bf8a0-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="bf8a0-116">Cell index:</span></span>  <br/> |<span data-ttu-id="bf8a0-117">**visXFormAngle**</span><span class="sxs-lookup"><span data-stu-id="bf8a0-117">**visXFormAngle**</span></span> <br/> |
   

