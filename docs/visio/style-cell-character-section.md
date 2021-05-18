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
ms.openlocfilehash: 349bdc42485aa511011aeb85a43f1ab3e4ea853d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411428"
---
# <a name="style-cell-character-section"></a><span data-ttu-id="8b2aa-103">Zelle "Style" (Abschnitt "Character")</span><span class="sxs-lookup"><span data-stu-id="8b2aa-103">Style Cell (Character Section)</span></span>

<span data-ttu-id="8b2aa-104">Zeigt die Zeichenformatierung für einen Textbereich im Textblock des Shapes an.</span><span class="sxs-lookup"><span data-stu-id="8b2aa-104">Shows the character formatting applied to a range of text in the shape's text block.</span></span>
  
|<span data-ttu-id="8b2aa-105">**Format**</span><span class="sxs-lookup"><span data-stu-id="8b2aa-105">**Style**</span></span>|<span data-ttu-id="8b2aa-106">**Wert**</span><span class="sxs-lookup"><span data-stu-id="8b2aa-106">**Value**</span></span>|<span data-ttu-id="8b2aa-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="8b2aa-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="8b2aa-108">Fett</span><span class="sxs-lookup"><span data-stu-id="8b2aa-108">Bold</span></span>  <br/> | <span data-ttu-id="8b2aa-109">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="8b2aa-109">&amp;H1</span></span>  <br/> |<span data-ttu-id="8b2aa-110">**visBold**</span><span class="sxs-lookup"><span data-stu-id="8b2aa-110">**visBold**</span></span> <br/> |
| <span data-ttu-id="8b2aa-111">Kursiv</span><span class="sxs-lookup"><span data-stu-id="8b2aa-111">Italic</span></span>  <br/> | <span data-ttu-id="8b2aa-112">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="8b2aa-112">&amp;H2</span></span>  <br/> |<span data-ttu-id="8b2aa-113">**visItalic**</span><span class="sxs-lookup"><span data-stu-id="8b2aa-113">**visItalic**</span></span> <br/> |
| <span data-ttu-id="8b2aa-114">Unterstrichen</span><span class="sxs-lookup"><span data-stu-id="8b2aa-114">Underline</span></span>  <br/> | <span data-ttu-id="8b2aa-115">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="8b2aa-115">&amp;H4</span></span>  <br/> |<span data-ttu-id="8b2aa-116">**visUnderLine**</span><span class="sxs-lookup"><span data-stu-id="8b2aa-116">**visUnderLine**</span></span> <br/> |
| <span data-ttu-id="8b2aa-117">Kapitälchen</span><span class="sxs-lookup"><span data-stu-id="8b2aa-117">Small caps</span></span>  <br/> | <span data-ttu-id="8b2aa-118">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="8b2aa-118">&amp;H8</span></span>  <br/> |<span data-ttu-id="8b2aa-119">**visSmallCaps**</span><span class="sxs-lookup"><span data-stu-id="8b2aa-119">**visSmallCaps**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b2aa-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8b2aa-120">Remarks</span></span>

<span data-ttu-id="8b2aa-p101">Die Zelle Style enthält Formatierungsinformationen für einen Unterbereich des Texts eines Shapes, wenn der Abschnitt Character mehrere Zeilen enthält. Andernfalls enthält diese Zelle Formatierungsinformationen für den gesamten Text des Shapes.</span><span class="sxs-lookup"><span data-stu-id="8b2aa-p101">The Style cell contains formatting information applied to a sub-range of a shape's text if the Characters section contains multiple rows. Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="8b2aa-123">Der Wert stellt eine Binärzahl dar, in der jedes einzelne Bit eine Zeichenformatvorlage ist.</span><span class="sxs-lookup"><span data-stu-id="8b2aa-123">The value represents a binary number in which each bit indicates a character style.</span></span> <span data-ttu-id="8b2aa-124">Der Wert 3 stellt beispielsweise fett und kursiv formatierten Text dar.</span><span class="sxs-lookup"><span data-stu-id="8b2aa-124">For example, a value of 3 represents text formatted in both italic and bold.</span></span> <span data-ttu-id="8b2aa-125">Wenn der Wert von Style 0 ist, ist der Text überhaupt nicht formatiert.</span><span class="sxs-lookup"><span data-stu-id="8b2aa-125">If the value of Style is 0, the text is plain, or unformatted.</span></span> <span data-ttu-id="8b2aa-126">Sie können mit booleschen BIT-Funktionen auf ein bestimmtes Format \* testen.</span><span class="sxs-lookup"><span data-stu-id="8b2aa-126">You can test for a particular format using Boolean BIT\* functions.</span></span> <span data-ttu-id="8b2aa-127">Ausführliche Informationen zu diesen Funktionen finden Sie in Ihrer Programmierungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="8b2aa-127">See your programming documentation for details about these functions.</span></span>
  
<span data-ttu-id="8b2aa-128">Verwenden Sie zum Erhalten eines Verweises auf die Zelle Style anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="8b2aa-128">To get a reference to the Style cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8b2aa-129">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="8b2aa-129">Cell name:</span></span>  <br/> | <span data-ttu-id="8b2aa-130">Char.Style[  *i*  ] wobei  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="8b2aa-130">Char.Style[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="8b2aa-131">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Style nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="8b2aa-131">To get a reference to the Style cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8b2aa-132">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="8b2aa-132">Section index:</span></span>  <br/> |<span data-ttu-id="8b2aa-133">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="8b2aa-133">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="8b2aa-134">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="8b2aa-134">Row index:</span></span>  <br/> |<span data-ttu-id="8b2aa-135">**visRowCharacter**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="8b2aa-135">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="8b2aa-136">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="8b2aa-136">Cell index:</span></span>  <br/> |<span data-ttu-id="8b2aa-137">**visCharacterStyle**</span><span class="sxs-lookup"><span data-stu-id="8b2aa-137">**visCharacterStyle**</span></span> <br/> |
   
 <span data-ttu-id="8b2aa-138">*Beispiel*</span><span class="sxs-lookup"><span data-stu-id="8b2aa-138">*Example*</span></span> 
  
<span data-ttu-id="8b2aa-139">Die Zelle Farbe in der ersten Zeile des Abschnitts Character eines Shapes enthält die folgende Formel:</span><span class="sxs-lookup"><span data-stu-id="8b2aa-139">Suppose the Color cell in the first row of a shape's Character section is set to this formula:</span></span>
  
<span data-ttu-id="8b2aa-140">= IF(BITAND(Char.Style,1)=1,4,3)</span><span class="sxs-lookup"><span data-stu-id="8b2aa-140">= IF(BITAND(Char.Style,1)=1,4,3)</span></span>
  
<span data-ttu-id="8b2aa-p103">Wenn das erste Zeichen des Shape-Texts fett formatiert ist, ist der von der ersten Zeile mit Zeicheneigenschaften formatierte Text blau (4). Andernfalls ist er grün (3). Dieses Beispiel setzt voraus, dass die Standardfarben verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b2aa-p103">Then if the first character of the shape's text is bold, the text covered by the first Character properties row will be blue (4); otherwise it will be green (3). This example assumes default colors are in effect.</span></span>
  
<span data-ttu-id="8b2aa-p104">Nachfolgend finden Sie ein Beispiel zum Festlegen eines Werts für die Zelle Style in einem Programm. Der erste Befehl verweist namentlich auf die Zelle Style, und der zweite Befehl verweist per Index auf die Zelle Style. Mit beiden Befehlen wird der von der zweiten Zeile des Abschnitts Character eines Shapes abgedeckte Text kursiv formatiert.</span><span class="sxs-lookup"><span data-stu-id="8b2aa-p104">The following is an example of setting the Style cell in a program. The first statement references the Style cell by name, and the second statement references the Style cell by index. Both statements apply italic to the text covered by the second row of a shape's Character section.</span></span>
  

