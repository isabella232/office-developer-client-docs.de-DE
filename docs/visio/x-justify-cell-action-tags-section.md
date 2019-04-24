---
title: Zelle "X Justify" (Abschnitt "Action Tags")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026936
localization_priority: Normal
ms.assetid: a8995020-3eaa-2b2c-eca0-dd475de4d06f
description: Der x-Offset der Schaltfläche Aktionstag in Bezug auf den Punkt, der durch die Zellen X und Y definiert ist.
ms.openlocfilehash: f8542d2f3a22b12794d999323d202d7a5bece20b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284972"
---
# <a name="x-justify-cell-action-tags-section"></a><span data-ttu-id="5bea9-103">Zelle "X Justify" (Abschnitt "Action Tags")</span><span class="sxs-lookup"><span data-stu-id="5bea9-103">X Justify Cell (Action Tags Section)</span></span>

<span data-ttu-id="5bea9-104">Der *x* -Offset der Schaltfläche Aktionstag in Bezug auf den Punkt, der durch die Zellen X und Y definiert ist.</span><span class="sxs-lookup"><span data-stu-id="5bea9-104">The  *x*  -offset of the action tag button relative to the point defined by the X and Y cells.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5bea9-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="5bea9-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="5bea9-106">**Wert**</span><span class="sxs-lookup"><span data-stu-id="5bea9-106">**Value**</span></span>|<span data-ttu-id="5bea9-107">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5bea9-107">**Description**</span></span>|<span data-ttu-id="5bea9-108">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="5bea9-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="5bea9-109">0</span><span class="sxs-lookup"><span data-stu-id="5bea9-109">0</span></span>  <br/> | <span data-ttu-id="5bea9-110">Links ausgerichtet (Standard).</span><span class="sxs-lookup"><span data-stu-id="5bea9-110">Left justified (the default).</span></span>  <br/> |<span data-ttu-id="5bea9-111">**visSmartTagXJustifyLeft**</span><span class="sxs-lookup"><span data-stu-id="5bea9-111">**visSmartTagXJustifyLeft**</span></span> <br/> |
| <span data-ttu-id="5bea9-112">1</span><span class="sxs-lookup"><span data-stu-id="5bea9-112">1</span></span>  <br/> | <span data-ttu-id="5bea9-113">Zentriert.</span><span class="sxs-lookup"><span data-stu-id="5bea9-113">Centered.</span></span>  <br/> |<span data-ttu-id="5bea9-114">**visSmartTagXJustifyCenter**</span><span class="sxs-lookup"><span data-stu-id="5bea9-114">**visSmartTagXJustifyCenter**</span></span> <br/> |
| <span data-ttu-id="5bea9-115">2</span><span class="sxs-lookup"><span data-stu-id="5bea9-115">2</span></span>  <br/> | <span data-ttu-id="5bea9-116">Rechts ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="5bea9-116">Right justified.</span></span>  <br/> |<span data-ttu-id="5bea9-117">**visSmartTagXJustifyRight**</span><span class="sxs-lookup"><span data-stu-id="5bea9-117">**visSmartTagXJustifyRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5bea9-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5bea9-118">Remarks</span></span>

<span data-ttu-id="5bea9-119">Die Zellen X Blocksatz und Y-Ausrichtung legen fest, wo die Schaltfläche Aktionstag in Bezug auf den in den Zellen X und Y definierten Punkt angeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="5bea9-119">The X Justify and Y Justify cells determine where the action tag button is placed in relation to the point defined in the X and Y cells.</span></span> 
  
<span data-ttu-id="5bea9-120">Wenn Sie einen Verweis auf die Zelle X Blocksatz aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="5bea9-120">To get a reference to the X Justify cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5bea9-121">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="5bea9-121">Cell name:</span></span>  <br/> | <span data-ttu-id="5bea9-122">Smarttags.</span><span class="sxs-lookup"><span data-stu-id="5bea9-122">SmartTags.</span></span>  <span data-ttu-id="5bea9-123">*Name* . XJustify, wobei SmartTags.</span><span class="sxs-lookup"><span data-stu-id="5bea9-123">*name*  .XJustify           where SmartTags.</span></span> <span data-ttu-id="5bea9-124">*Name* ist der Name der Zeile mit dem Aktionstag.</span><span class="sxs-lookup"><span data-stu-id="5bea9-124">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="5bea9-125">Wenn Sie einen Verweis auf die Zelle X Blocksatz aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="5bea9-125">To get a reference to the X Justify cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5bea9-126">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="5bea9-126">Section index:</span></span>  <br/> |<span data-ttu-id="5bea9-127">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="5bea9-127">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="5bea9-128">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="5bea9-128">Row index:</span></span>  <br/> |<span data-ttu-id="5bea9-129">**visRowSmartTag** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="5bea9-129">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="5bea9-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="5bea9-130">Cell index:</span></span>  <br/> |<span data-ttu-id="5bea9-131">**visSmartTagXJustify**</span><span class="sxs-lookup"><span data-stu-id="5bea9-131">**visSmartTagXJustify**</span></span> <br/> |
   

