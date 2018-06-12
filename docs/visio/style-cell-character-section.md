---
title: Zelle "Style" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251249
localization_priority: Normal
ms.assetid: 4372f1e1-f0a9-2f63-ff79-58f2afdceed5
description: Zeigt die Zeichenformatierung für einen Textbereich im Textblock des Shapes an.
ms.openlocfilehash: 48bda5eb798f439e2616b2b910d7ec5ac719d060
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798192"
---
# <a name="style-cell-character-section"></a><span data-ttu-id="e819e-103">Zelle "Style" (Abschnitt "Character")</span><span class="sxs-lookup"><span data-stu-id="e819e-103">Style Cell (Character Section)</span></span>

<span data-ttu-id="e819e-104">Zeigt die Zeichenformatierung für einen Textbereich im Textblock des Shapes an.</span><span class="sxs-lookup"><span data-stu-id="e819e-104">Shows the character formatting applied to a range of text in the shape's text block.</span></span>
  
|<span data-ttu-id="e819e-105">**Style**</span><span class="sxs-lookup"><span data-stu-id="e819e-105">**Style**</span></span>|<span data-ttu-id="e819e-106">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e819e-106">**Value**</span></span>|<span data-ttu-id="e819e-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="e819e-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="e819e-108">Fett</span><span class="sxs-lookup"><span data-stu-id="e819e-108">Bold</span></span>  <br/> | <span data-ttu-id="e819e-109">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="e819e-109">&amp;H1</span></span>  <br/> |<span data-ttu-id="e819e-110">**visBold**</span><span class="sxs-lookup"><span data-stu-id="e819e-110">**visBold**</span></span> <br/> |
| <span data-ttu-id="e819e-111">Kursiv</span><span class="sxs-lookup"><span data-stu-id="e819e-111">Italic</span></span>  <br/> | <span data-ttu-id="e819e-112">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="e819e-112">&amp;H2</span></span>  <br/> |<span data-ttu-id="e819e-113">**visItalic**</span><span class="sxs-lookup"><span data-stu-id="e819e-113">**visItalic**</span></span> <br/> |
| <span data-ttu-id="e819e-114">Unterstrichen</span><span class="sxs-lookup"><span data-stu-id="e819e-114">Underline</span></span>  <br/> | <span data-ttu-id="e819e-115">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="e819e-115">&amp;H4</span></span>  <br/> |<span data-ttu-id="e819e-116">**visUnderLine**</span><span class="sxs-lookup"><span data-stu-id="e819e-116">**visUnderLine**</span></span> <br/> |
| <span data-ttu-id="e819e-117">Kapitälchen</span><span class="sxs-lookup"><span data-stu-id="e819e-117">Small caps</span></span>  <br/> | <span data-ttu-id="e819e-118">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="e819e-118">&amp;H8</span></span>  <br/> |<span data-ttu-id="e819e-119">**visSmallCaps**</span><span class="sxs-lookup"><span data-stu-id="e819e-119">**visSmallCaps**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e819e-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e819e-120">Remarks</span></span>

<span data-ttu-id="e819e-p101">Die Zelle Style enthält Formatierungsinformationen für einen Unterbereich des Texts eines Shapes, wenn der Abschnitt Character mehrere Zeilen enthält. Andernfalls enthält diese Zelle Formatierungsinformationen für den gesamten Text des Shapes.</span><span class="sxs-lookup"><span data-stu-id="e819e-p101">The Style cell contains formatting information applied to a sub-range of a shape's text if the Characters section contains multiple rows. Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="e819e-123">Der Wert stellt eine binäre Zahl in denen jedes Bit eine Zeichenformatvorlage angibt.</span><span class="sxs-lookup"><span data-stu-id="e819e-123">The value represents a binary number in which each bit indicates a character style.</span></span> <span data-ttu-id="e819e-124">Beispielsweise stellt einen Wert von 3 Text fett und kursiv formatiert.</span><span class="sxs-lookup"><span data-stu-id="e819e-124">For example, a value of 3 represents text formatted in both italic and bold.</span></span> <span data-ttu-id="e819e-125">Wenn der Wert der Style 0 ist, wird der Text einfache oder unformatierte.</span><span class="sxs-lookup"><span data-stu-id="e819e-125">If the value of Style is 0, the text is plain, or unformatted.</span></span> <span data-ttu-id="e819e-126">Sie können ein bestimmtes Format mit Boolean BIT testen\* Funktionen.</span><span class="sxs-lookup"><span data-stu-id="e819e-126">You can test for a particular format using Boolean BIT\* functions.</span></span> <span data-ttu-id="e819e-127">Finden Sie unter Dokumentation zu Ihrem Programmierung Informationen zu diesen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="e819e-127">See your programming documentation for details about these functions.</span></span>
  
<span data-ttu-id="e819e-128">Wenn Sie einen Verweis auf die Zelle Style nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e819e-128">To get a reference to the Style cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e819e-129">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="e819e-129">Cell name:</span></span>  <br/> | <span data-ttu-id="e819e-130">Char.Style [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="e819e-130">Char.Style[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="e819e-131">Wenn Sie einen Verweis auf die Zelle Style aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="e819e-131">To get a reference to the Style cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e819e-132">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="e819e-132">Section index:</span></span>  <br/> |<span data-ttu-id="e819e-133">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="e819e-133">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="e819e-134">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="e819e-134">Row index:</span></span>  <br/> |<span data-ttu-id="e819e-135">**VisRowCharacter** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e819e-135">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e819e-136">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="e819e-136">Cell index:</span></span>  <br/> |<span data-ttu-id="e819e-137">**visCharacterStyle**</span><span class="sxs-lookup"><span data-stu-id="e819e-137">**visCharacterStyle**</span></span> <br/> |
   
 <span data-ttu-id="e819e-138">*Beispiel*</span><span class="sxs-lookup"><span data-stu-id="e819e-138">*Example*</span></span> 
  
<span data-ttu-id="e819e-139">Die Zelle Farbe in der ersten Zeile des Abschnitts Character eines Shapes enthält die folgende Formel:</span><span class="sxs-lookup"><span data-stu-id="e819e-139">Suppose the Color cell in the first row of a shape's Character section is set to this formula:</span></span>
  
<span data-ttu-id="e819e-140">= IF(BITAND(Char.Style,1)=1,4,3)</span><span class="sxs-lookup"><span data-stu-id="e819e-140">= IF(BITAND(Char.Style,1)=1,4,3)</span></span>
  
<span data-ttu-id="e819e-p103">Wenn das erste Zeichen des Shape-Texts fett formatiert ist, ist der von der ersten Zeile mit Zeicheneigenschaften formatierte Text blau (4). Andernfalls ist er grün (3). Dieses Beispiel setzt voraus, dass die Standardfarben verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e819e-p103">Then if the first character of the shape's text is bold, the text covered by the first Character properties row will be blue (4); otherwise it will be green (3). This example assumes default colors are in effect.</span></span>
  
<span data-ttu-id="e819e-p104">Nachfolgend finden Sie ein Beispiel zum Festlegen eines Werts für die Zelle Style in einem Programm. Der erste Befehl verweist namentlich auf die Zelle Style, und der zweite Befehl verweist per Index auf die Zelle Style. Mit beiden Befehlen wird der von der zweiten Zeile des Abschnitts Character eines Shapes abgedeckte Text kursiv formatiert.</span><span class="sxs-lookup"><span data-stu-id="e819e-p104">The following is an example of setting the Style cell in a program. The first statement references the Style cell by name, and the second statement references the Style cell by index. Both statements apply italic to the text covered by the second row of a shape's Character section.</span></span>
  

