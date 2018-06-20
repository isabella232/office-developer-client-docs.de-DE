---
title: Zelle "HAlign" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm425
localization_priority: Normal
ms.assetid: a8d6b622-60b3-e43f-b6a1-55db561204ed
description: Definiert die horizontale Ausrichtung des Texts im Textblock des Shapes.
ms.openlocfilehash: 224e495e8aea70c418a0ab7f5a7d56975d9868e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797139"
---
# <a name="halign-cell-paragraph-section"></a><span data-ttu-id="9fafe-103">HAlign Cell (Paragraph Section)</span><span class="sxs-lookup"><span data-stu-id="9fafe-103">HAlign Cell (Paragraph Section)</span></span>

<span data-ttu-id="9fafe-104">Definiert die horizontale Ausrichtung des Texts im Textblock des Shapes.</span><span class="sxs-lookup"><span data-stu-id="9fafe-104">Determines the horizontal alignment of text in the shape's text block.</span></span>
  
|<span data-ttu-id="9fafe-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9fafe-105">**Value**</span></span>|<span data-ttu-id="9fafe-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9fafe-106">**Description**</span></span>|<span data-ttu-id="9fafe-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="9fafe-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="9fafe-108">0</span><span class="sxs-lookup"><span data-stu-id="9fafe-108">0</span></span>  <br/> | <span data-ttu-id="9fafe-109">Linksbündig</span><span class="sxs-lookup"><span data-stu-id="9fafe-109">Left align</span></span>  <br/> |<span data-ttu-id="9fafe-110">**visHorzLeft**</span><span class="sxs-lookup"><span data-stu-id="9fafe-110">**visHorzLeft**</span></span> <br/> |
| <span data-ttu-id="9fafe-111">1</span><span class="sxs-lookup"><span data-stu-id="9fafe-111">1</span></span>  <br/> | <span data-ttu-id="9fafe-112">Mittig</span><span class="sxs-lookup"><span data-stu-id="9fafe-112">Center</span></span>  <br/> |<span data-ttu-id="9fafe-113">**visHorzCenter**</span><span class="sxs-lookup"><span data-stu-id="9fafe-113">**visHorzCenter**</span></span> <br/> |
| <span data-ttu-id="9fafe-114">2</span><span class="sxs-lookup"><span data-stu-id="9fafe-114">2</span></span>  <br/> | <span data-ttu-id="9fafe-115">Rechtsbündig</span><span class="sxs-lookup"><span data-stu-id="9fafe-115">Right align</span></span>  <br/> |<span data-ttu-id="9fafe-116">**visHorzRight**</span><span class="sxs-lookup"><span data-stu-id="9fafe-116">**visHorzRight**</span></span> <br/> |
| <span data-ttu-id="9fafe-117">3</span><span class="sxs-lookup"><span data-stu-id="9fafe-117">3</span></span>  <br/> | <span data-ttu-id="9fafe-118">Blocksatz</span><span class="sxs-lookup"><span data-stu-id="9fafe-118">Justify</span></span>  <br/> |<span data-ttu-id="9fafe-119">**visHorzJustify**</span><span class="sxs-lookup"><span data-stu-id="9fafe-119">**visHorzJustify**</span></span> <br/> |
| <span data-ttu-id="9fafe-120">4</span><span class="sxs-lookup"><span data-stu-id="9fafe-120">4</span></span>  <br/> | <span data-ttu-id="9fafe-121">Blocksatz erzwingen</span><span class="sxs-lookup"><span data-stu-id="9fafe-121">Force justify</span></span>  <br/> |<span data-ttu-id="9fafe-122">**visHorzForce**</span><span class="sxs-lookup"><span data-stu-id="9fafe-122">**visHorzForce**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9fafe-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9fafe-123">Remarks</span></span>

<span data-ttu-id="9fafe-124">Beim Blocksatz wird Platz zwischen den Wörtern in jeder Zeile (nicht in der letzten Zeile) des Absatzes geschaffen, um sowohl die rechte als auch die linke Seite von Text an den Seitenrändern auszurichten.</span><span class="sxs-lookup"><span data-stu-id="9fafe-124">Justify adds space between words in every line except the last line of the paragraph to align both the left and right sides of text with the margins.</span></span>
  
<span data-ttu-id="9fafe-125">Bei Blocksatz erzwingen wird jede Zeile im Absatz ausgerichtet, einschließlich der letzten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9fafe-125">Force justify justifies every line in the paragraph, including the last.</span></span>
  
<span data-ttu-id="9fafe-126">Wenn Sie einen Verweis auf die Zelle HAlign nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9fafe-126">To get a reference to the HAlign cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9fafe-127">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9fafe-127">Cell name:</span></span>  <br/> | <span data-ttu-id="9fafe-128">Para.HorzAlign [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="9fafe-128">Para.HorzAlign[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="9fafe-129">Wenn Sie einen Verweis auf die Zelle HAlign aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="9fafe-129">To get a reference to the HAlign cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9fafe-130">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9fafe-130">Section index:</span></span>  <br/> |<span data-ttu-id="9fafe-131">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="9fafe-131">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="9fafe-132">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9fafe-132">Row index:</span></span>  <br/> |<span data-ttu-id="9fafe-133">**VisRowParagraph** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9fafe-133">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="9fafe-134">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9fafe-134">Cell index:</span></span>  <br/> |<span data-ttu-id="9fafe-135">**visHorzAlign**</span><span class="sxs-lookup"><span data-stu-id="9fafe-135">**visHorzAlign**</span></span> <br/> |
   

