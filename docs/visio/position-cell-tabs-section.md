---
title: Zelle "Position" (Abschnitt "Tabs")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251755
localization_priority: Normal
ms.assetid: 40d7e38e-b3b0-8616-ed27-1f963a841e03
description: Definiert die Position eines Tabstopps. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt die Tabstoppposition unverändert.
ms.openlocfilehash: 06f3a9fd5cfdf78f5383e70f32f8514b0adab114
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797727"
---
# <a name="position-cell-tabs-section"></a><span data-ttu-id="28979-105">Zelle "Position" (Abschnitt "Tabs")</span><span class="sxs-lookup"><span data-stu-id="28979-105">Position Cell (Tabs Section)</span></span>

<span data-ttu-id="28979-p102">Definiert die Position eines Tabstopps. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt die Tabstoppposition unverändert.</span><span class="sxs-lookup"><span data-stu-id="28979-p102">Specifies the position of a tab stop. The tab position is independent of the scale of the drawing. If the drawing is scaled, the tab position remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="28979-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="28979-109">Remarks</span></span>

<span data-ttu-id="28979-110">Wenn Sie einen Verweis auf die Zelle Position aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="28979-110">To get a reference to the Position cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="28979-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="28979-111">Cell name:</span></span>  <br/> | <span data-ttu-id="28979-112">Registerkarten.</span><span class="sxs-lookup"><span data-stu-id="28979-112">Tabs.</span></span>  <span data-ttu-id="28979-113">*Ij* wobei *i* und *j* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="28979-113">*ij*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="28979-114">Wenn Sie einen Verweis auf die Zelle Position aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="28979-114">To get a reference to the Position cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="28979-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="28979-115">Section index:</span></span>  <br/> |<span data-ttu-id="28979-116">**visSectionTab**</span><span class="sxs-lookup"><span data-stu-id="28979-116">**visSectionTab**</span></span> <br/> |
| <span data-ttu-id="28979-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="28979-117">Row index:</span></span>  <br/> |<span data-ttu-id="28979-118">**VisRowTab** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="28979-118">**visRowTab** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="28979-119">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="28979-119">Cell index:</span></span>  <br/> | <span data-ttu-id="28979-120">(*j* \* 3) + **VisTabPos**</span><span class="sxs-lookup"><span data-stu-id="28979-120">(*j*  \*3) + **visTabPos**</span></span> <br/> |
   

