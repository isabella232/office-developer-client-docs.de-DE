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
ms.openlocfilehash: a48619e2531c0a69ad63af3b88ae9f019019b1fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414739"
---
# <a name="halign-cell-paragraph-section"></a><span data-ttu-id="a67b1-103">Zelle "HAlign" (Abschnitt "Paragraph")</span><span class="sxs-lookup"><span data-stu-id="a67b1-103">HAlign Cell (Paragraph Section)</span></span>

<span data-ttu-id="a67b1-104">Definiert die horizontale Ausrichtung des Texts im Textblock des Shapes.</span><span class="sxs-lookup"><span data-stu-id="a67b1-104">Determines the horizontal alignment of text in the shape's text block.</span></span>
  
|<span data-ttu-id="a67b1-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a67b1-105">**Value**</span></span>|<span data-ttu-id="a67b1-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a67b1-106">**Description**</span></span>|<span data-ttu-id="a67b1-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="a67b1-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="a67b1-108">0</span><span class="sxs-lookup"><span data-stu-id="a67b1-108">0</span></span>  <br/> | <span data-ttu-id="a67b1-109">Linksbündig</span><span class="sxs-lookup"><span data-stu-id="a67b1-109">Left align</span></span>  <br/> |<span data-ttu-id="a67b1-110">**visHorzLeft**</span><span class="sxs-lookup"><span data-stu-id="a67b1-110">**visHorzLeft**</span></span> <br/> |
| <span data-ttu-id="a67b1-111">1</span><span class="sxs-lookup"><span data-stu-id="a67b1-111">1</span></span>  <br/> | <span data-ttu-id="a67b1-112">Zentriert</span><span class="sxs-lookup"><span data-stu-id="a67b1-112">Center</span></span>  <br/> |<span data-ttu-id="a67b1-113">**visHorzCenter**</span><span class="sxs-lookup"><span data-stu-id="a67b1-113">**visHorzCenter**</span></span> <br/> |
| <span data-ttu-id="a67b1-114">2</span><span class="sxs-lookup"><span data-stu-id="a67b1-114">2</span></span>  <br/> | <span data-ttu-id="a67b1-115">Rechtsbündig</span><span class="sxs-lookup"><span data-stu-id="a67b1-115">Right align</span></span>  <br/> |<span data-ttu-id="a67b1-116">**visHorzRight**</span><span class="sxs-lookup"><span data-stu-id="a67b1-116">**visHorzRight**</span></span> <br/> |
| <span data-ttu-id="a67b1-117">3</span><span class="sxs-lookup"><span data-stu-id="a67b1-117">3</span></span>  <br/> | <span data-ttu-id="a67b1-118">Ausrichten</span><span class="sxs-lookup"><span data-stu-id="a67b1-118">Justify</span></span>  <br/> |<span data-ttu-id="a67b1-119">**visHorzJustify**</span><span class="sxs-lookup"><span data-stu-id="a67b1-119">**visHorzJustify**</span></span> <br/> |
| <span data-ttu-id="a67b1-120">4</span><span class="sxs-lookup"><span data-stu-id="a67b1-120">4</span></span>  <br/> | <span data-ttu-id="a67b1-121">Blocksatz erzwingen</span><span class="sxs-lookup"><span data-stu-id="a67b1-121">Force justify</span></span>  <br/> |<span data-ttu-id="a67b1-122">**visHorzForce**</span><span class="sxs-lookup"><span data-stu-id="a67b1-122">**visHorzForce**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a67b1-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a67b1-123">Remarks</span></span>

<span data-ttu-id="a67b1-124">Beim Blocksatz wird Platz zwischen den Wörtern in jeder Zeile (nicht in der letzten Zeile) des Absatzes geschaffen, um sowohl die rechte als auch die linke Seite von Text an den Seitenrändern auszurichten.</span><span class="sxs-lookup"><span data-stu-id="a67b1-124">Justify adds space between words in every line except the last line of the paragraph to align both the left and right sides of text with the margins.</span></span>
  
<span data-ttu-id="a67b1-125">Bei Blocksatz erzwingen wird jede Zeile im Absatz ausgerichtet, einschließlich der letzten Zeile.</span><span class="sxs-lookup"><span data-stu-id="a67b1-125">Force justify justifies every line in the paragraph, including the last.</span></span>
  
<span data-ttu-id="a67b1-126">Wenn Sie einen Verweis auf die Zelle HAlign aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a67b1-126">To get a reference to the HAlign cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a67b1-127">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a67b1-127">Cell name:</span></span>  <br/> | <span data-ttu-id="a67b1-128">Abs. HAlign [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="a67b1-128">Para.HorzAlign[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="a67b1-129">Wenn Sie einen Verweis auf die Zelle HAlign aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a67b1-129">To get a reference to the HAlign cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a67b1-130">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a67b1-130">Section index:</span></span>  <br/> |<span data-ttu-id="a67b1-131">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="a67b1-131">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="a67b1-132">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a67b1-132">Row index:</span></span>  <br/> |<span data-ttu-id="a67b1-133">**visRowParagraph** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a67b1-133">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a67b1-134">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a67b1-134">Cell index:</span></span>  <br/> |<span data-ttu-id="a67b1-135">**visHorzAlign**</span><span class="sxs-lookup"><span data-stu-id="a67b1-135">**visHorzAlign**</span></span> <br/> |
   

