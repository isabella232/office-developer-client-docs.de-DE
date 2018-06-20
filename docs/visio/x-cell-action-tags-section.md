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
description: Die x - Koordinatenposition in lokalen Koordinaten des Shapes, um die herum die Schaltfläche Aktionstag platziert wird.
ms.openlocfilehash: f6b3a57b825c96398058e7b71e3cebeb8480dd49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798424"
---
# <a name="x-cell-action-tags-section"></a><span data-ttu-id="a9a6c-103">Zelle "X" (Abschnitt "Action Tags")</span><span class="sxs-lookup"><span data-stu-id="a9a6c-103">X Cell (Action Tags Section)</span></span>

<span data-ttu-id="a9a6c-104">Die *X* -Koordinatenposition in lokalen Koordinaten des Shapes, um die herum die Schaltfläche Aktionstag platziert wird.</span><span class="sxs-lookup"><span data-stu-id="a9a6c-104">The  *x*  -coordinate position in the shape's local coordinates around which the action tag button is placed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a9a6c-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a9a6c-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a9a6c-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a9a6c-106">Remarks</span></span>

<span data-ttu-id="a9a6c-107">Die Zellen X und Y definieren einen Punkt in den lokalen Koordinaten des Shapes, und die Zellen X Justify und Y Justify definieren, wo die Schaltfläche Aktionstag in Bezug auf diesen Punkt platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9a6c-107">The X and Y cells define a point in the shape's local coordinates, and the X Justify and Y Justify cells define where to place the action tag button in relation to that point.</span></span> 
  
<span data-ttu-id="a9a6c-108">Wenn Sie einen Verweis auf die Zelle X nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a9a6c-108">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a9a6c-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a9a6c-109">Cell name:</span></span>  <br/> |<span data-ttu-id="a9a6c-110">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="a9a6c-110">SmartTags.</span></span> <span data-ttu-id="a9a6c-111">*Name* . X Where SmartTags.</span><span class="sxs-lookup"><span data-stu-id="a9a6c-111">*name*  .X           where SmartTags.</span></span> <span data-ttu-id="a9a6c-112">*Name* ist der Name der Zeile Aktionstag</span><span class="sxs-lookup"><span data-stu-id="a9a6c-112">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="a9a6c-113">Wenn Sie einen Verweis auf die Zelle X aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a9a6c-113">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a9a6c-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a9a6c-114">Section index:</span></span>  <br/> |<span data-ttu-id="a9a6c-115">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="a9a6c-115">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="a9a6c-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a9a6c-116">Row index:</span></span>  <br/> |<span data-ttu-id="a9a6c-117">**VisRowSmartTag** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a9a6c-117">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a9a6c-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a9a6c-118">Cell index:</span></span>  <br/> |<span data-ttu-id="a9a6c-119">**visSmartTagX**</span><span class="sxs-lookup"><span data-stu-id="a9a6c-119">**visSmartTagX**</span></span> <br/> |
   

