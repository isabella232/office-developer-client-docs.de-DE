---
title: Zelle "QuickStyleVariation" (Abschnitt "Quick Style")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: Bestimmt, ob die Formeln und Werte der Text-, Linien- und Füllfarbe (oder einer Kombination dieser Eigenschaften) mithilfe von Farben überschrieben werden, die mit dem Diagrammhintergrund kontrastieren. Der Wert ist ein bitweiser OR-Wert von 0, 1, 2, 4 und 8.
ms.openlocfilehash: 736e2287c00c24774ef8b677613235d642697f4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433794"
---
# <a name="quickstylevariation-cell-quick-style-section"></a><span data-ttu-id="e833a-104">Zelle "QuickStyleVariation" (Abschnitt "Quick Style")</span><span class="sxs-lookup"><span data-stu-id="e833a-104">QuickStyleVariation Cell (Quick Style Section)</span></span>

<span data-ttu-id="e833a-105">Bestimmt, ob die Formeln und Werte der Text-, Linien- und Füllfarbe (oder einer Kombination dieser Eigenschaften) mithilfe von Farben überschrieben werden, die mit dem Diagrammhintergrund kontrastieren.</span><span class="sxs-lookup"><span data-stu-id="e833a-105">Determines whether to override the formulas and values of text, line, and fill color (or a combination of those properties) by using colors that contrast with the diagram background.</span></span> <span data-ttu-id="e833a-106">Der Wert ist ein bitweiser OR-Wert von 0, 1, 2, 4 und 8.</span><span class="sxs-lookup"><span data-stu-id="e833a-106">Value is a bitwise OR of 0, 1, 2, 4, and 8.</span></span>
  
|<span data-ttu-id="e833a-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e833a-107">**Value**</span></span>|<span data-ttu-id="e833a-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e833a-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e833a-109">0</span><span class="sxs-lookup"><span data-stu-id="e833a-109">0</span></span>  <br/> |<span data-ttu-id="e833a-110">Ändern Sie die Text-, Linien- oder Füllfarbe eines Shapes (oder eine Kombination dieser Eigenschaften) nicht, um für die angegebene Hintergrundfarbe eines Designs sichtbar zu bleiben.</span><span class="sxs-lookup"><span data-stu-id="e833a-110">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="e833a-111">1</span><span class="sxs-lookup"><span data-stu-id="e833a-111">1</span></span>  <br/> |<span data-ttu-id="e833a-112">Ändern Sie die Text-, Linien- oder Füllfarbe eines Shapes (oder eine Kombination dieser Eigenschaften) nicht, um für die angegebene Hintergrundfarbe eines Designs sichtbar zu bleiben.</span><span class="sxs-lookup"><span data-stu-id="e833a-112">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="e833a-113">2</span><span class="sxs-lookup"><span data-stu-id="e833a-113">2</span></span>  <br/> |<span data-ttu-id="e833a-114">Ändern Sie gegebenenfalls die Textfarbe eines Shapes, um für die angegebene Hintergrundfarbe eines Designs sichtbar zu bleiben.</span><span class="sxs-lookup"><span data-stu-id="e833a-114">Alter a shape's text color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="e833a-115">4 </span><span class="sxs-lookup"><span data-stu-id="e833a-115">4</span></span>  <br/> |<span data-ttu-id="e833a-116">Ändern Sie gegebenenfalls die Linienfarbe eines Shapes, um für die angegebene Hintergrundfarbe eines Designs sichtbar zu bleiben.</span><span class="sxs-lookup"><span data-stu-id="e833a-116">Alter a shape's line color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="e833a-117">8 </span><span class="sxs-lookup"><span data-stu-id="e833a-117">8</span></span>  <br/> |<span data-ttu-id="e833a-118">Ändern Sie die Füllfarbe eines Shapes, um bei Bedarf für die angegebene Hintergrundfarbe eines Designs sichtbar zu bleiben.</span><span class="sxs-lookup"><span data-stu-id="e833a-118">Alter a shape's fill color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e833a-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e833a-119">Remarks</span></span>

<span data-ttu-id="e833a-120">Verwenden Sie die Zelle QuickStyleVariation, um die Sichtbarkeit in Text oder Zeilen zu gewährleisten, wenn sie sich außerhalb einer sichtbaren Formgeometrie befinden (z. B. in einer Form, deren Textfeld sich unterhalb des unteren Rands der Form befindet, z. B. in Netzwerkdiagrammen).</span><span class="sxs-lookup"><span data-stu-id="e833a-120">Use the QuickStyleVariation cell to guarantee visibility in either text or lines when they are outside any visible shape geometry (for example, in a shape whose textbox is below the bottom of the shape, such as those in Network Diagrams).</span></span> <span data-ttu-id="e833a-121">Der Standardwert der Zelle ist 0, was bedeutet, dass ihr Verhalten inaktiv ist.</span><span class="sxs-lookup"><span data-stu-id="e833a-121">The cell's default value is 0, which means that its behavior is inactive.</span></span> <span data-ttu-id="e833a-122">Jeder andere Wert löst das Verhalten der Zelle aus.</span><span class="sxs-lookup"><span data-stu-id="e833a-122">Any other value triggers the cell's behavior.</span></span>
  
<span data-ttu-id="e833a-123">Der QuickStyleVariation-Wert überschreibt den von der THEMEVAL-Funktion erzeugten Wert, wenn er sich in den Zellen Color (Character Section), FillForegnd oder LineColor befindet (oder durch direkte Verweise auf diese drei Eigenschaften durch THEMEVAL("CharacterColor"), THEMEVAL("FillColor") und THEMEVAL("LineColor")) erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="e833a-123">The QuickStyleVariation value overrides the value produced by the THEMEVAL function when it resides in the Color (Character Section), FillForegnd, or LineColor cells (or produced by direct references to these three properties by means of THEMEVAL("CharacterColor"), THEMEVAL("FillColor"), and THEMEVAL("LineColor")).</span></span>
  
<span data-ttu-id="e833a-124">Verwenden Sie zum Abrufen eines Verweises auf die **QuickStyleVariation-Zelle** anhand des Namens aus einer anderen Formel, indem Sie den Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abrufen:</span><span class="sxs-lookup"><span data-stu-id="e833a-124">To get a reference to the **QuickStyleVariation** cell by name from another formula, by getting the value of the **N** attribute of a **Cell** element, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e833a-125">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="e833a-125">Cell name:</span></span>  <br/> |<span data-ttu-id="e833a-126">QuickStyleVariation</span><span class="sxs-lookup"><span data-stu-id="e833a-126">QuickStyleVariation</span></span>  <br/> |
   
<span data-ttu-id="e833a-127">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **QuickStyleVariation-Zelle** nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="e833a-127">To get a reference to the **QuickStyleVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e833a-128">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="e833a-128">Section index:</span></span>  <br/> |<span data-ttu-id="e833a-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e833a-129">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e833a-130">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="e833a-130">Row index:</span></span>  <br/> |<span data-ttu-id="e833a-131">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="e833a-131">**visRowQuickStyleProperties**</span></span> <br/> |
|<span data-ttu-id="e833a-132">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="e833a-132">Cell index:</span></span>  <br/> |<span data-ttu-id="e833a-133">**visQuickStyleVariation**</span><span class="sxs-lookup"><span data-stu-id="e833a-133">**visQuickStyleVariation**</span></span> <br/> |
   

