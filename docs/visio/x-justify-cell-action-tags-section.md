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
description: Die x - Abstand der Schaltfläche Aktionstag in Bezug auf den Punkt, der durch die Zellen X und Y definiert ist.
ms.openlocfilehash: 043d7b198ae5a529c623545fb54ef5aa1d32217d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798435"
---
# <a name="x-justify-cell-action-tags-section"></a><span data-ttu-id="2b1ed-103">X Justify Cell (Action Tags Section)</span><span class="sxs-lookup"><span data-stu-id="2b1ed-103">X Justify Cell (Action Tags Section)</span></span>

<span data-ttu-id="2b1ed-104">Die *X* -Abstand der Schaltfläche Aktionstag in Bezug auf den Punkt, der durch die Zellen X und Y definiert ist.</span><span class="sxs-lookup"><span data-stu-id="2b1ed-104">The  *x*  -offset of the action tag button relative to the point defined by the X and Y cells.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2b1ed-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2b1ed-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="2b1ed-106">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2b1ed-106">**Value**</span></span>|<span data-ttu-id="2b1ed-107">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2b1ed-107">**Description**</span></span>|<span data-ttu-id="2b1ed-108">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="2b1ed-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="2b1ed-109">0</span><span class="sxs-lookup"><span data-stu-id="2b1ed-109">0</span></span>  <br/> | <span data-ttu-id="2b1ed-110">Links ausgerichtet (Standard).</span><span class="sxs-lookup"><span data-stu-id="2b1ed-110">Left justified (the default).</span></span>  <br/> |<span data-ttu-id="2b1ed-111">**visSmartTagXJustifyLeft**</span><span class="sxs-lookup"><span data-stu-id="2b1ed-111">**visSmartTagXJustifyLeft**</span></span> <br/> |
| <span data-ttu-id="2b1ed-112">1</span><span class="sxs-lookup"><span data-stu-id="2b1ed-112">1</span></span>  <br/> | <span data-ttu-id="2b1ed-113">Zentriert.</span><span class="sxs-lookup"><span data-stu-id="2b1ed-113">Centered.</span></span>  <br/> |<span data-ttu-id="2b1ed-114">**visSmartTagXJustifyCenter**</span><span class="sxs-lookup"><span data-stu-id="2b1ed-114">**visSmartTagXJustifyCenter**</span></span> <br/> |
| <span data-ttu-id="2b1ed-115">2</span><span class="sxs-lookup"><span data-stu-id="2b1ed-115">2</span></span>  <br/> | <span data-ttu-id="2b1ed-116">Rechts ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="2b1ed-116">Right justified.</span></span>  <br/> |<span data-ttu-id="2b1ed-117">**visSmartTagXJustifyRight**</span><span class="sxs-lookup"><span data-stu-id="2b1ed-117">**visSmartTagXJustifyRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b1ed-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2b1ed-118">Remarks</span></span>

<span data-ttu-id="2b1ed-119">Die Zellen X Justify und Y Justify bestimmen, wo die Schaltfläche Aktionstag in Bezug auf die Zellen X und Y definierten Punkt platziert wird.</span><span class="sxs-lookup"><span data-stu-id="2b1ed-119">The X Justify and Y Justify cells determine where the action tag button is placed in relation to the point defined in the X and Y cells.</span></span> 
  
<span data-ttu-id="2b1ed-120">Zum Abrufen eines Verweises auf die Zelle X Justify nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2b1ed-120">To get a reference to the X Justify cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2b1ed-121">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2b1ed-121">Cell name:</span></span>  <br/> | <span data-ttu-id="2b1ed-122">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="2b1ed-122">SmartTags.</span></span>  <span data-ttu-id="2b1ed-123">*Name* . XJustify wobei SmartTags.</span><span class="sxs-lookup"><span data-stu-id="2b1ed-123">*name*  .XJustify           where SmartTags.</span></span> <span data-ttu-id="2b1ed-124">*Name* ist der Name der Zeile Aktionstag</span><span class="sxs-lookup"><span data-stu-id="2b1ed-124">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="2b1ed-125">Wenn Sie einen Verweis auf die Zelle X Justify aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="2b1ed-125">To get a reference to the X Justify cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2b1ed-126">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2b1ed-126">Section index:</span></span>  <br/> |<span data-ttu-id="2b1ed-127">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="2b1ed-127">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="2b1ed-128">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2b1ed-128">Row index:</span></span>  <br/> |<span data-ttu-id="2b1ed-129">**VisRowSmartTag** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2b1ed-129">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="2b1ed-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="2b1ed-130">Cell index:</span></span>  <br/> |<span data-ttu-id="2b1ed-131">**visSmartTagXJustify**</span><span class="sxs-lookup"><span data-stu-id="2b1ed-131">**visSmartTagXJustify**</span></span> <br/> |
   

