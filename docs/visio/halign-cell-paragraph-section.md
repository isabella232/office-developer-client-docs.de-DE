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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360179"
---
# <a name="halign-cell-paragraph-section"></a><span data-ttu-id="dde17-103">Zelle "HAlign" (Abschnitt "Paragraph")</span><span class="sxs-lookup"><span data-stu-id="dde17-103">HAlign Cell (Paragraph Section)</span></span>

<span data-ttu-id="dde17-104">Definiert die horizontale Ausrichtung des Texts im Textblock des Shapes.</span><span class="sxs-lookup"><span data-stu-id="dde17-104">Determines the horizontal alignment of text in the shape's text block.</span></span>
  
|<span data-ttu-id="dde17-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="dde17-105">**Value**</span></span>|<span data-ttu-id="dde17-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dde17-106">**Description**</span></span>|<span data-ttu-id="dde17-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="dde17-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="dde17-108">0</span><span class="sxs-lookup"><span data-stu-id="dde17-108">0</span></span>  <br/> | <span data-ttu-id="dde17-109">Linksbündig</span><span class="sxs-lookup"><span data-stu-id="dde17-109">Left align</span></span>  <br/> |<span data-ttu-id="dde17-110">**visHorzLeft**</span><span class="sxs-lookup"><span data-stu-id="dde17-110">**visHorzLeft**</span></span> <br/> |
| <span data-ttu-id="dde17-111">1</span><span class="sxs-lookup"><span data-stu-id="dde17-111">1</span></span>  <br/> | <span data-ttu-id="dde17-112">Zentriert</span><span class="sxs-lookup"><span data-stu-id="dde17-112">Center</span></span>  <br/> |<span data-ttu-id="dde17-113">**visHorzCenter**</span><span class="sxs-lookup"><span data-stu-id="dde17-113">**visHorzCenter**</span></span> <br/> |
| <span data-ttu-id="dde17-114">2</span><span class="sxs-lookup"><span data-stu-id="dde17-114">2</span></span>  <br/> | <span data-ttu-id="dde17-115">Rechtsbündig</span><span class="sxs-lookup"><span data-stu-id="dde17-115">Right align</span></span>  <br/> |<span data-ttu-id="dde17-116">**visHorzRight**</span><span class="sxs-lookup"><span data-stu-id="dde17-116">**visHorzRight**</span></span> <br/> |
| <span data-ttu-id="dde17-117">3</span><span class="sxs-lookup"><span data-stu-id="dde17-117">3</span></span>  <br/> | <span data-ttu-id="dde17-118">Ausrichten</span><span class="sxs-lookup"><span data-stu-id="dde17-118">Justify</span></span>  <br/> |<span data-ttu-id="dde17-119">**visHorzJustify**</span><span class="sxs-lookup"><span data-stu-id="dde17-119">**visHorzJustify**</span></span> <br/> |
| <span data-ttu-id="dde17-120">4</span><span class="sxs-lookup"><span data-stu-id="dde17-120">4</span></span>  <br/> | <span data-ttu-id="dde17-121">Blocksatz erzwingen</span><span class="sxs-lookup"><span data-stu-id="dde17-121">Force justify</span></span>  <br/> |<span data-ttu-id="dde17-122">**visHorzForce**</span><span class="sxs-lookup"><span data-stu-id="dde17-122">**visHorzForce**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dde17-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dde17-123">Remarks</span></span>

<span data-ttu-id="dde17-124">Beim Blocksatz wird Platz zwischen den Wörtern in jeder Zeile (nicht in der letzten Zeile) des Absatzes geschaffen, um sowohl die rechte als auch die linke Seite von Text an den Seitenrändern auszurichten.</span><span class="sxs-lookup"><span data-stu-id="dde17-124">Justify adds space between words in every line except the last line of the paragraph to align both the left and right sides of text with the margins.</span></span>
  
<span data-ttu-id="dde17-125">Bei Blocksatz erzwingen wird jede Zeile im Absatz ausgerichtet, einschließlich der letzten Zeile.</span><span class="sxs-lookup"><span data-stu-id="dde17-125">Force justify justifies every line in the paragraph, including the last.</span></span>
  
<span data-ttu-id="dde17-126">Wenn Sie einen Verweis auf die Zelle HAlign aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="dde17-126">To get a reference to the HAlign cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dde17-127">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="dde17-127">Cell name:</span></span>  <br/> | <span data-ttu-id="dde17-128">Abs. HAlign [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="dde17-128">Para.HorzAlign[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="dde17-129">Wenn Sie einen Verweis auf die Zelle HAlign aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="dde17-129">To get a reference to the HAlign cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dde17-130">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="dde17-130">Section index:</span></span>  <br/> |<span data-ttu-id="dde17-131">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="dde17-131">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="dde17-132">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="dde17-132">Row index:</span></span>  <br/> |<span data-ttu-id="dde17-133">**visRowParagraph** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="dde17-133">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="dde17-134">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="dde17-134">Cell index:</span></span>  <br/> |<span data-ttu-id="dde17-135">**visHorzAlign**</span><span class="sxs-lookup"><span data-stu-id="dde17-135">**visHorzAlign**</span></span> <br/> |
   

