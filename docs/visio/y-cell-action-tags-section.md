---
title: Zelle "Y" (Abschnitt "Action Tags")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026934
localization_priority: Normal
ms.assetid: b213fc46-7f80-99fd-60ba-8ddf3d0f6ee3
description: Die y-Koordinatenposition in den lokalen Koordinaten des Shapes, um die sich die Schaltfläche Aktionstag befindet.
ms.openlocfilehash: 02797a849a262cb506f4617aadaccedabccdab77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430224"
---
# <a name="y-cell-action-tags-section"></a><span data-ttu-id="07432-103">Zelle "Y" (Abschnitt "Action Tags")</span><span class="sxs-lookup"><span data-stu-id="07432-103">Y Cell (Action Tags Section)</span></span>

<span data-ttu-id="07432-104">Die *y* -Koordinatenposition in den lokalen Koordinaten des Shapes, um die sich die Schaltfläche Aktionstag befindet.</span><span class="sxs-lookup"><span data-stu-id="07432-104">The  *y*  -coordinate position in the shape's local coordinates around which the action tag button is placed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="07432-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="07432-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="07432-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07432-106">Remarks</span></span>

<span data-ttu-id="07432-107">Die Zellen X und Y definieren einen Punkt in den lokalen Koordinaten des Shapes, und die Zellen X Justify und Y Justify definieren, wo die Schaltfläche Aktionstag in Bezug auf diesen Punkt platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="07432-107">The X and Y cells define a point in the shape's local coordinates, and the X Justify and Y Justify cells define where to place the action tag button in relation to that point.</span></span> 
  
<span data-ttu-id="07432-108">Wenn Sie einen Verweis auf die Zelle Y aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="07432-108">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="07432-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="07432-109">Cell name:</span></span>  <br/> | <span data-ttu-id="07432-110">Smarttags.</span><span class="sxs-lookup"><span data-stu-id="07432-110">SmartTags.</span></span>  <span data-ttu-id="07432-111">*Name* . Y, wobei SmartTags.</span><span class="sxs-lookup"><span data-stu-id="07432-111">*name*  .Y           where SmartTags.</span></span> <span data-ttu-id="07432-112">*Name* ist der Name der Zeile mit dem Aktionstag.</span><span class="sxs-lookup"><span data-stu-id="07432-112">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="07432-113">Wenn Sie einen Verweis auf die Zelle Y nach Index aus einem Programm erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="07432-113">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="07432-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="07432-114">Section index:</span></span>  <br/> |<span data-ttu-id="07432-115">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="07432-115">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="07432-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="07432-116">Row index:</span></span>  <br/> |<span data-ttu-id="07432-117">**visRowSmartTag** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="07432-117">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="07432-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="07432-118">Cell index:</span></span>  <br/> |<span data-ttu-id="07432-119">**visSmartTagY**</span><span class="sxs-lookup"><span data-stu-id="07432-119">**visSmartTagY**</span></span> <br/> |
   

