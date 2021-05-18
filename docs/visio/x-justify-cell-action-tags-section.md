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
description: Der x-Offset der Aktionstagschaltfläche relativ zum durch die X- und Y-Zellen definierten Punkt.
ms.openlocfilehash: f8542d2f3a22b12794d999323d202d7a5bece20b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414123"
---
# <a name="x-justify-cell-action-tags-section"></a><span data-ttu-id="aaac4-103">Zelle "X Justify" (Abschnitt "Action Tags")</span><span class="sxs-lookup"><span data-stu-id="aaac4-103">X Justify Cell (Action Tags Section)</span></span>

<span data-ttu-id="aaac4-104">Der  *x-Offset*  der Aktionstagschaltfläche relativ zum durch die X- und Y-Zellen definierten Punkt.</span><span class="sxs-lookup"><span data-stu-id="aaac4-104">The  *x*  -offset of the action tag button relative to the point defined by the X and Y cells.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="aaac4-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="aaac4-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="aaac4-106">**Wert**</span><span class="sxs-lookup"><span data-stu-id="aaac4-106">**Value**</span></span>|<span data-ttu-id="aaac4-107">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aaac4-107">**Description**</span></span>|<span data-ttu-id="aaac4-108">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="aaac4-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="aaac4-109">0</span><span class="sxs-lookup"><span data-stu-id="aaac4-109">0</span></span>  <br/> | <span data-ttu-id="aaac4-110">Links ausgerichtet (Standard).</span><span class="sxs-lookup"><span data-stu-id="aaac4-110">Left justified (the default).</span></span>  <br/> |<span data-ttu-id="aaac4-111">**visSmartTagXJustifyLeft**</span><span class="sxs-lookup"><span data-stu-id="aaac4-111">**visSmartTagXJustifyLeft**</span></span> <br/> |
| <span data-ttu-id="aaac4-112">1</span><span class="sxs-lookup"><span data-stu-id="aaac4-112">1</span></span>  <br/> | <span data-ttu-id="aaac4-113">Zentriert.</span><span class="sxs-lookup"><span data-stu-id="aaac4-113">Centered.</span></span>  <br/> |<span data-ttu-id="aaac4-114">**visSmartTagXJustifyCenter**</span><span class="sxs-lookup"><span data-stu-id="aaac4-114">**visSmartTagXJustifyCenter**</span></span> <br/> |
| <span data-ttu-id="aaac4-115">2</span><span class="sxs-lookup"><span data-stu-id="aaac4-115">2</span></span>  <br/> | <span data-ttu-id="aaac4-116">Rechts ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="aaac4-116">Right justified.</span></span>  <br/> |<span data-ttu-id="aaac4-117">**visSmartTagXJustifyRight**</span><span class="sxs-lookup"><span data-stu-id="aaac4-117">**visSmartTagXJustifyRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aaac4-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aaac4-118">Remarks</span></span>

<span data-ttu-id="aaac4-119">Die Zellen X Justify und Y Justify bestimmen, wo die Aktionstagschaltfläche im Verhältnis zum in den X- und Y-Zellen definierten Punkt platziert wird.</span><span class="sxs-lookup"><span data-stu-id="aaac4-119">The X Justify and Y Justify cells determine where the action tag button is placed in relation to the point defined in the X and Y cells.</span></span> 
  
<span data-ttu-id="aaac4-120">Verwenden Sie zum Erhalten eines Verweises auf die Zelle X Justify anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="aaac4-120">To get a reference to the X Justify cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aaac4-121">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="aaac4-121">Cell name:</span></span>  <br/> | <span data-ttu-id="aaac4-122">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="aaac4-122">SmartTags.</span></span>  <span data-ttu-id="aaac4-123">*Name*  . XJustify where SmartTags.</span><span class="sxs-lookup"><span data-stu-id="aaac4-123">*name*  .XJustify           where SmartTags.</span></span> <span data-ttu-id="aaac4-124">*Name*  ist der Name der Aktionstagzeile</span><span class="sxs-lookup"><span data-stu-id="aaac4-124">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="aaac4-125">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die X Justify-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="aaac4-125">To get a reference to the X Justify cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aaac4-126">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="aaac4-126">Section index:</span></span>  <br/> |<span data-ttu-id="aaac4-127">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="aaac4-127">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="aaac4-128">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="aaac4-128">Row index:</span></span>  <br/> |<span data-ttu-id="aaac4-129">**visRowSmartTag**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="aaac4-129">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="aaac4-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="aaac4-130">Cell index:</span></span>  <br/> |<span data-ttu-id="aaac4-131">**visSmartTagXJustify**</span><span class="sxs-lookup"><span data-stu-id="aaac4-131">**visSmartTagXJustify**</span></span> <br/> |
   

