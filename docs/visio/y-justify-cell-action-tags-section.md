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
description: Der y-Offset der Schaltfläche Aktionstag in Bezug auf den Punkt, der durch die Zellen X und Y definiert ist.
ms.openlocfilehash: d7a1f5c1feda3624c9f96039e7247c737a91a813
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357015"
---
# <a name="y-justify-cell-action-tags-section"></a><span data-ttu-id="f1ba3-103">Zelle "Y Justify" (Abschnitt "Action Tags")</span><span class="sxs-lookup"><span data-stu-id="f1ba3-103">Y Justify Cell (Action Tags Section)</span></span>

<span data-ttu-id="f1ba3-104">Der *y* -Offset der Schaltfläche Aktionstag in Bezug auf den Punkt, der durch die Zellen X und y definiert ist.</span><span class="sxs-lookup"><span data-stu-id="f1ba3-104">The  *y*  -offset of the action tag button relative to the point defined by the X and Y cells.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f1ba3-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f1ba3-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="f1ba3-106">**Wert**</span><span class="sxs-lookup"><span data-stu-id="f1ba3-106">**Value**</span></span>|<span data-ttu-id="f1ba3-107">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f1ba3-107">**Description**</span></span>|<span data-ttu-id="f1ba3-108">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="f1ba3-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="f1ba3-109">0</span><span class="sxs-lookup"><span data-stu-id="f1ba3-109">0</span></span>  <br/> | <span data-ttu-id="f1ba3-110">Oben ausgerichtet (Standard).</span><span class="sxs-lookup"><span data-stu-id="f1ba3-110">Top justified (the default).</span></span>  <br/> |<span data-ttu-id="f1ba3-111">**visSmartTagYJustifyTop**</span><span class="sxs-lookup"><span data-stu-id="f1ba3-111">**visSmartTagYJustifyTop**</span></span> <br/> |
| <span data-ttu-id="f1ba3-112">1</span><span class="sxs-lookup"><span data-stu-id="f1ba3-112">1</span></span>  <br/> | <span data-ttu-id="f1ba3-113">Zentriert.</span><span class="sxs-lookup"><span data-stu-id="f1ba3-113">Centered.</span></span>  <br/> |<span data-ttu-id="f1ba3-114">**visSmartTagYJustifyMiddle**</span><span class="sxs-lookup"><span data-stu-id="f1ba3-114">**visSmartTagYJustifyMiddle**</span></span> <br/> |
| <span data-ttu-id="f1ba3-115">2</span><span class="sxs-lookup"><span data-stu-id="f1ba3-115">2</span></span>  <br/> | <span data-ttu-id="f1ba3-116">Unten ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="f1ba3-116">Bottom justified.</span></span>  <br/> |<span data-ttu-id="f1ba3-117">**visSmartTagYJustifyBottom**</span><span class="sxs-lookup"><span data-stu-id="f1ba3-117">**visSmartTagYJustifyBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1ba3-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1ba3-118">Remarks</span></span>

<span data-ttu-id="f1ba3-119">Die Zellen X Blocksatz und Y-Ausrichtung legen fest, wo die Schaltfläche Aktionstag in Bezug auf den in den Zellen X und Y definierten Punkt angeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="f1ba3-119">The X Justify and Y Justify cells determine where the action tag button is placed in relation to the point defined in the X and Y cells.</span></span>
  
<span data-ttu-id="f1ba3-120">Wenn Sie einen Verweis auf die Zelle Y Blocksatz aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f1ba3-120">To get a reference to the Y Justify cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f1ba3-121">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="f1ba3-121">Cell name:</span></span>  <br/> | <span data-ttu-id="f1ba3-122">Smarttags.</span><span class="sxs-lookup"><span data-stu-id="f1ba3-122">SmartTags.</span></span>  <span data-ttu-id="f1ba3-123">*Name* . YJustify, wobei SmartTags.</span><span class="sxs-lookup"><span data-stu-id="f1ba3-123">*name*  .YJustify           where SmartTags.</span></span> <span data-ttu-id="f1ba3-124">*Name* ist der Name der Zeile mit dem Aktionstag.</span><span class="sxs-lookup"><span data-stu-id="f1ba3-124">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="f1ba3-125">Wenn Sie einen Verweis auf die Zelle Y Blocksatz aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="f1ba3-125">To get a reference to the Y Justify cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f1ba3-126">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="f1ba3-126">Section index:</span></span>  <br/> |<span data-ttu-id="f1ba3-127">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="f1ba3-127">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="f1ba3-128">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="f1ba3-128">Row index:</span></span>  <br/> |<span data-ttu-id="f1ba3-129">**visRowSmartTag** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f1ba3-129">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f1ba3-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="f1ba3-130">Cell index:</span></span>  <br/> |<span data-ttu-id="f1ba3-131">**visSmartTagYJustify**</span><span class="sxs-lookup"><span data-stu-id="f1ba3-131">**visSmartTagYJustify**</span></span> <br/> |
   

