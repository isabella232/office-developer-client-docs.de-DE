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
description: Die x-Koordinatenposition in den lokalen Koordinaten des Shapes, um die sich die Aktionstagschaltfläche befindet.
ms.openlocfilehash: 9f26bec81563c9813a88ed5c69730266834ee101
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431113"
---
# <a name="x-cell-action-tags-section"></a><span data-ttu-id="b8c7b-103">Zelle "X" (Abschnitt "Action Tags")</span><span class="sxs-lookup"><span data-stu-id="b8c7b-103">X Cell (Action Tags Section)</span></span>

<span data-ttu-id="b8c7b-104">Die  x-Koordinatenposition in den lokalen Koordinaten des Shapes, um die sich die Aktionstagschaltfläche befindet.</span><span class="sxs-lookup"><span data-stu-id="b8c7b-104">The  *x*  -coordinate position in the shape's local coordinates around which the action tag button is placed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b8c7b-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b8c7b-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b8c7b-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b8c7b-106">Remarks</span></span>

<span data-ttu-id="b8c7b-107">Die Zellen X und Y definieren einen Punkt in den lokalen Koordinaten des Shapes, und die Zellen X Justify und Y Justify definieren, wo die Schaltfläche Aktionstag in Bezug auf diesen Punkt platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8c7b-107">The X and Y cells define a point in the shape's local coordinates, and the X Justify and Y Justify cells define where to place the action tag button in relation to that point.</span></span> 
  
<span data-ttu-id="b8c7b-108">Um einen Verweis auf die Zelle X anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="b8c7b-108">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b8c7b-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b8c7b-109">Cell name:</span></span>  <br/> |<span data-ttu-id="b8c7b-110">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="b8c7b-110">SmartTags.</span></span> <span data-ttu-id="b8c7b-111">*Name*  . X, wobei SmartTags.</span><span class="sxs-lookup"><span data-stu-id="b8c7b-111">*name*  .X           where SmartTags.</span></span> <span data-ttu-id="b8c7b-112">*Name*  ist der Name der Aktionstagzeile</span><span class="sxs-lookup"><span data-stu-id="b8c7b-112">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="b8c7b-113">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die X-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="b8c7b-113">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b8c7b-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b8c7b-114">Section index:</span></span>  <br/> |<span data-ttu-id="b8c7b-115">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="b8c7b-115">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="b8c7b-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b8c7b-116">Row index:</span></span>  <br/> |<span data-ttu-id="b8c7b-117">**visRowSmartTag**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b8c7b-117">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b8c7b-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b8c7b-118">Cell index:</span></span>  <br/> |<span data-ttu-id="b8c7b-119">**visSmartTagX**</span><span class="sxs-lookup"><span data-stu-id="b8c7b-119">**visSmartTagX**</span></span> <br/> |
   

