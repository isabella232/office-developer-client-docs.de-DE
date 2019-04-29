---
title: Zelle "X" (Abschnitt "Action Tags")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60093
localization_priority: Normal
ms.assetid: d13e362b-9b69-30c5-003a-9c5df2aa29f6
description: Die x-Koordinate in den lokalen Koordinaten des Shapes, um die sich die Schaltfläche Aktionstag befindet.
ms.openlocfilehash: 9f26bec81563c9813a88ed5c69730266834ee101
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431113"
---
# <a name="x-cell-action-tags-section"></a><span data-ttu-id="9c84c-103">Zelle "X" (Abschnitt "Action Tags")</span><span class="sxs-lookup"><span data-stu-id="9c84c-103">X Cell (Action Tags Section)</span></span>

<span data-ttu-id="9c84c-104">Die *x* -Koordinate in den lokalen Koordinaten des Shapes, um die sich die Schaltfläche Aktionstag befindet.</span><span class="sxs-lookup"><span data-stu-id="9c84c-104">The  *x*  -coordinate position in the shape's local coordinates around which the action tag button is placed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9c84c-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9c84c-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9c84c-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c84c-106">Remarks</span></span>

<span data-ttu-id="9c84c-107">Die Zellen X und Y definieren einen Punkt in den lokalen Koordinaten des Shapes, und die Zellen X Justify und Y Justify definieren, wo die Schaltfläche Aktionstag in Bezug auf diesen Punkt platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c84c-107">The X and Y cells define a point in the shape's local coordinates, and the X Justify and Y Justify cells define where to place the action tag button in relation to that point.</span></span> 
  
<span data-ttu-id="9c84c-108">Wenn Sie einen Verweis auf die Zelle X aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9c84c-108">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9c84c-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9c84c-109">Cell name:</span></span>  <br/> |<span data-ttu-id="9c84c-110">Smarttags.</span><span class="sxs-lookup"><span data-stu-id="9c84c-110">SmartTags.</span></span> <span data-ttu-id="9c84c-111">*Name* . X, wobei SmartTags.</span><span class="sxs-lookup"><span data-stu-id="9c84c-111">*name*  .X           where SmartTags.</span></span> <span data-ttu-id="9c84c-112">*Name* ist der Name der Zeile mit dem Aktionstag.</span><span class="sxs-lookup"><span data-stu-id="9c84c-112">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="9c84c-113">Wenn Sie einen Verweis auf die Zelle X aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="9c84c-113">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9c84c-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9c84c-114">Section index:</span></span>  <br/> |<span data-ttu-id="9c84c-115">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="9c84c-115">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="9c84c-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9c84c-116">Row index:</span></span>  <br/> |<span data-ttu-id="9c84c-117">**visRowSmartTag** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9c84c-117">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="9c84c-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9c84c-118">Cell index:</span></span>  <br/> |<span data-ttu-id="9c84c-119">**visSmartTagX**</span><span class="sxs-lookup"><span data-stu-id="9c84c-119">**visSmartTagX**</span></span> <br/> |
   

