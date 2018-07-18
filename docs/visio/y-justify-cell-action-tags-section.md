---
title: Zelle "Y Justify" (Abschnitt "Action Tags")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026937
localization_priority: Normal
ms.assetid: 27042b62-7623-95d7-7e10-f589d74605c7
description: Die y-Abstand der Schaltfläche Aktionstag in Bezug auf den Punkt, der durch die Zellen X und Y definiert ist.
ms.openlocfilehash: 8f8323d1f392654bf118ece2f78890f2a1b860ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798465"
---
# <a name="y-justify-cell-action-tags-section"></a><span data-ttu-id="f0bfc-103">Y Justify Cell (Action Tags Section)</span><span class="sxs-lookup"><span data-stu-id="f0bfc-103">Y Justify Cell (Action Tags Section)</span></span>

<span data-ttu-id="f0bfc-104">Die *y* -Abstand der Schaltfläche Aktionstag in Bezug auf den Punkt, der durch die Zellen X und Y definiert ist.</span><span class="sxs-lookup"><span data-stu-id="f0bfc-104">The  *y*  -offset of the action tag button relative to the point defined by the X and Y cells.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f0bfc-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f0bfc-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="f0bfc-106">**Wert**</span><span class="sxs-lookup"><span data-stu-id="f0bfc-106">**Value**</span></span>|<span data-ttu-id="f0bfc-107">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f0bfc-107">**Description**</span></span>|<span data-ttu-id="f0bfc-108">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="f0bfc-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="f0bfc-109">0</span><span class="sxs-lookup"><span data-stu-id="f0bfc-109">0</span></span>  <br/> | <span data-ttu-id="f0bfc-110">Oben ausgerichtet (Standard).</span><span class="sxs-lookup"><span data-stu-id="f0bfc-110">Top justified (the default).</span></span>  <br/> |<span data-ttu-id="f0bfc-111">**visSmartTagYJustifyTop**</span><span class="sxs-lookup"><span data-stu-id="f0bfc-111">**visSmartTagYJustifyTop**</span></span> <br/> |
| <span data-ttu-id="f0bfc-112">1</span><span class="sxs-lookup"><span data-stu-id="f0bfc-112">1</span></span>  <br/> | <span data-ttu-id="f0bfc-113">Zentriert.</span><span class="sxs-lookup"><span data-stu-id="f0bfc-113">Centered.</span></span>  <br/> |<span data-ttu-id="f0bfc-114">**visSmartTagYJustifyMiddle**</span><span class="sxs-lookup"><span data-stu-id="f0bfc-114">**visSmartTagYJustifyMiddle**</span></span> <br/> |
| <span data-ttu-id="f0bfc-115">2</span><span class="sxs-lookup"><span data-stu-id="f0bfc-115">2</span></span>  <br/> | <span data-ttu-id="f0bfc-116">Unten ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="f0bfc-116">Bottom justified.</span></span>  <br/> |<span data-ttu-id="f0bfc-117">**visSmartTagYJustifyBottom**</span><span class="sxs-lookup"><span data-stu-id="f0bfc-117">**visSmartTagYJustifyBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0bfc-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0bfc-118">Remarks</span></span>

<span data-ttu-id="f0bfc-119">Die Zellen X Justify und Y Justify bestimmen, wo die Schaltfläche Aktionstag in Bezug auf die Zellen X und Y definierten Punkt platziert wird.</span><span class="sxs-lookup"><span data-stu-id="f0bfc-119">The X Justify and Y Justify cells determine where the action tag button is placed in relation to the point defined in the X and Y cells.</span></span>
  
<span data-ttu-id="f0bfc-120">Wenn Sie einen Verweis auf die Zelle Y Justify aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f0bfc-120">To get a reference to the Y Justify cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f0bfc-121">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="f0bfc-121">Cell name:</span></span>  <br/> | <span data-ttu-id="f0bfc-122">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="f0bfc-122">SmartTags.</span></span>  <span data-ttu-id="f0bfc-123">*Name* . YJustify wobei SmartTags.</span><span class="sxs-lookup"><span data-stu-id="f0bfc-123">*name*  .YJustify           where SmartTags.</span></span> <span data-ttu-id="f0bfc-124">*Name* ist der Name der Zeile Aktionstag</span><span class="sxs-lookup"><span data-stu-id="f0bfc-124">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="f0bfc-125">Wenn Sie einen Verweis auf die Zelle Y Justify aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="f0bfc-125">To get a reference to the Y Justify cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f0bfc-126">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="f0bfc-126">Section index:</span></span>  <br/> |<span data-ttu-id="f0bfc-127">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="f0bfc-127">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="f0bfc-128">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="f0bfc-128">Row index:</span></span>  <br/> |<span data-ttu-id="f0bfc-129">**VisRowSmartTag** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f0bfc-129">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f0bfc-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="f0bfc-130">Cell index:</span></span>  <br/> |<span data-ttu-id="f0bfc-131">**visSmartTagYJustify**</span><span class="sxs-lookup"><span data-stu-id="f0bfc-131">**visSmartTagYJustify**</span></span> <br/> |
   

