---
title: QuickStyleVariation Cell (Quick Style section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: Bestimmt, ob die Formeln und Werte der Text-, Linien-und Füllfarbe (oder einer Kombination dieser Eigenschaften) mithilfe von Farben außer Kraft gesetzt werden, die mit dem Diagrammhintergrund in Kontrast stehen. Der Wert ist ein bitweises OR von 0, 1, 2, 4 und 8.
ms.openlocfilehash: 736e2287c00c24774ef8b677613235d642697f4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360014"
---
# <a name="quickstylevariation-cell-quick-style-section"></a><span data-ttu-id="04451-104">QuickStyleVariation Cell (Quick Style section)</span><span class="sxs-lookup"><span data-stu-id="04451-104">QuickStyleVariation Cell (Quick Style Section)</span></span>

<span data-ttu-id="04451-105">Bestimmt, ob die Formeln und Werte der Text-, Linien-und Füllfarbe (oder einer Kombination dieser Eigenschaften) mithilfe von Farben außer Kraft gesetzt werden, die mit dem Diagrammhintergrund in Kontrast stehen.</span><span class="sxs-lookup"><span data-stu-id="04451-105">Determines whether to override the formulas and values of text, line, and fill color (or a combination of those properties) by using colors that contrast with the diagram background.</span></span> <span data-ttu-id="04451-106">Der Wert ist ein bitweises OR von 0, 1, 2, 4 und 8.</span><span class="sxs-lookup"><span data-stu-id="04451-106">Value is a bitwise OR of 0, 1, 2, 4, and 8.</span></span>
  
|<span data-ttu-id="04451-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="04451-107">**Value**</span></span>|<span data-ttu-id="04451-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="04451-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="04451-109">0</span><span class="sxs-lookup"><span data-stu-id="04451-109">0</span></span>  <br/> |<span data-ttu-id="04451-110">Ändern Sie die Text-, Linien-oder Füllfarbe einer Form (oder eine Kombination dieser Eigenschaften) nicht so, dass Sie für die Hintergrundfarbe eines Designs sichtbar bleibt.</span><span class="sxs-lookup"><span data-stu-id="04451-110">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="04451-111">1</span><span class="sxs-lookup"><span data-stu-id="04451-111">1</span></span>  <br/> |<span data-ttu-id="04451-112">Ändern Sie die Text-, Linien-oder Füllfarbe einer Form (oder eine Kombination dieser Eigenschaften) nicht so, dass Sie für die Hintergrundfarbe eines Designs sichtbar bleibt.</span><span class="sxs-lookup"><span data-stu-id="04451-112">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="04451-113">2</span><span class="sxs-lookup"><span data-stu-id="04451-113">2</span></span>  <br/> |<span data-ttu-id="04451-114">Ändern Sie bei Bedarf die Textfarbe eines Shapes, damit es für die Hintergrundfarbe eines Designs sichtbar bleibt.</span><span class="sxs-lookup"><span data-stu-id="04451-114">Alter a shape's text color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="04451-115">4</span><span class="sxs-lookup"><span data-stu-id="04451-115">4</span></span>  <br/> |<span data-ttu-id="04451-116">Ändern Sie bei Bedarf die Linienfarbe eines Shapes, damit es für die Hintergrundfarbe eines Designs sichtbar bleibt.</span><span class="sxs-lookup"><span data-stu-id="04451-116">Alter a shape's line color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="04451-117">8</span><span class="sxs-lookup"><span data-stu-id="04451-117">8</span></span>  <br/> |<span data-ttu-id="04451-118">Ändern Sie bei Bedarf die Füllfarbe einer Form, um Sie für die Hintergrundfarbe eines Designs sichtbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="04451-118">Alter a shape's fill color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="04451-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04451-119">Remarks</span></span>

<span data-ttu-id="04451-120">Verwenden Sie die Zelle QuickStyleVariation, um die Sichtbarkeit von Text oder Zeilen zu gewährleisten, wenn Sie sich außerhalb einer sichtbaren Formen Geometrie befinden (beispielsweise in einem Shape, dessen TextBox sich unter dem unteren Rand der Form befindet, beispielsweise in Netzplänen).</span><span class="sxs-lookup"><span data-stu-id="04451-120">Use the QuickStyleVariation cell to guarantee visibility in either text or lines when they are outside any visible shape geometry (for example, in a shape whose textbox is below the bottom of the shape, such as those in Network Diagrams).</span></span> <span data-ttu-id="04451-121">Der Standardwert der Zelle ist 0, was bedeutet, dass das Verhalten inaktiv ist.</span><span class="sxs-lookup"><span data-stu-id="04451-121">The cell's default value is 0, which means that its behavior is inactive.</span></span> <span data-ttu-id="04451-122">Jeder andere Wert löst das Verhalten der Zelle aus.</span><span class="sxs-lookup"><span data-stu-id="04451-122">Any other value triggers the cell's behavior.</span></span>
  
<span data-ttu-id="04451-123">Der QuickStyleVariation-Wert überschreibt den von der THEMEVAL-Funktion erzeugten Wert, wenn er sich in den Zellen Color (Character section), Zelle FillForegnd oder Zelle LineColor (oder durch direkte Verweise auf diese drei Eigenschaften mittels THEMEVAL) befindet. Zu benutzende "), THEMEVAL (" FillColor ") und THEMEVAL (" Zelle LineColor ")).</span><span class="sxs-lookup"><span data-stu-id="04451-123">The QuickStyleVariation value overrides the value produced by the THEMEVAL function when it resides in the Color (Character Section), FillForegnd, or LineColor cells (or produced by direct references to these three properties by means of THEMEVAL("CharacterColor"), THEMEVAL("FillColor"), and THEMEVAL("LineColor")).</span></span>
  
<span data-ttu-id="04451-124">Wenn Sie einen Verweis auf die Zelle **QuickStyleVariation** aus einer anderen Formel nach Namen erhalten möchten, indem Sie den Wert des **N** -Attributs eines **Cell** -Elements oder mithilfe der **CellsU** -Eigenschaft aus einem Programm abrufen, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="04451-124">To get a reference to the **QuickStyleVariation** cell by name from another formula, by getting the value of the **N** attribute of a **Cell** element, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="04451-125">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="04451-125">Cell name:</span></span>  <br/> |<span data-ttu-id="04451-126">QuickStyleVariation</span><span class="sxs-lookup"><span data-stu-id="04451-126">QuickStyleVariation</span></span>  <br/> |
   
<span data-ttu-id="04451-127">Wenn Sie einen Verweis auf die Zelle **QuickStyleVariation** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="04451-127">To get a reference to the **QuickStyleVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="04451-128">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="04451-128">Section index:</span></span>  <br/> |<span data-ttu-id="04451-129">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="04451-129">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="04451-130">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="04451-130">Row index:</span></span>  <br/> |<span data-ttu-id="04451-131">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="04451-131">**visRowQuickStyleProperties**</span></span> <br/> |
|<span data-ttu-id="04451-132">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="04451-132">Cell index:</span></span>  <br/> |<span data-ttu-id="04451-133">**visQuickStyleVariation**</span><span class="sxs-lookup"><span data-stu-id="04451-133">**visQuickStyleVariation**</span></span> <br/> |
   

