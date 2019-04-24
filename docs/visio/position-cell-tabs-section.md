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
ms.openlocfilehash: ef17b38d708103ca004594ba04ff5b8d1ada13bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307749"
---
# <a name="position-cell-tabs-section"></a><span data-ttu-id="3328d-105">Zelle "Position" (Abschnitt "Tabs")</span><span class="sxs-lookup"><span data-stu-id="3328d-105">Position Cell (Tabs Section)</span></span>

<span data-ttu-id="3328d-p102">Definiert die Position eines Tabstopps. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt die Tabstoppposition unverändert.</span><span class="sxs-lookup"><span data-stu-id="3328d-p102">Specifies the position of a tab stop. The tab position is independent of the scale of the drawing. If the drawing is scaled, the tab position remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3328d-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3328d-109">Remarks</span></span>

<span data-ttu-id="3328d-110">Wenn Sie einen Verweis auf die Zelle Position aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="3328d-110">To get a reference to the Position cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3328d-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="3328d-111">Cell name:</span></span>  <br/> | <span data-ttu-id="3328d-112">Registerkarten.</span><span class="sxs-lookup"><span data-stu-id="3328d-112">Tabs.</span></span>  <span data-ttu-id="3328d-113">*IJ* , wobei *i* und *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="3328d-113">*ij*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="3328d-114">Wenn Sie einen Verweis auf die Zelle Position nach Index aus einem Programm erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="3328d-114">To get a reference to the Position cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3328d-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="3328d-115">Section index:</span></span>  <br/> |<span data-ttu-id="3328d-116">**visSectionTab**</span><span class="sxs-lookup"><span data-stu-id="3328d-116">**visSectionTab**</span></span> <br/> |
| <span data-ttu-id="3328d-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="3328d-117">Row index:</span></span>  <br/> |<span data-ttu-id="3328d-118">**visRowTab** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3328d-118">**visRowTab** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3328d-119">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="3328d-119">Cell index:</span></span>  <br/> | <span data-ttu-id="3328d-120">(*j* \* 3) + **visTabPos**</span><span class="sxs-lookup"><span data-stu-id="3328d-120">(*j*  \*3) + **visTabPos**</span></span> <br/> |
   

