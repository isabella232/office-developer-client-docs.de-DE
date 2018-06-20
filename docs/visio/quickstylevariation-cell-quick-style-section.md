---
title: QuickStyleVariation Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: Bestimmt, ob die Formeln und die Werte der Text, Linie, innen und Füllung Farbe (oder eine Kombination dieser Eigenschaften) mithilfe von Farben außer Kraft setzen, Kontrast, wobei der Diagrammhintergrund. Wert ist eine bitweise OR 0, 1, 2, 4 und 8.
ms.openlocfilehash: fe6462798b61a0713f98196974876144cf4606e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797763"
---
# <a name="quickstylevariation-cell-quick-style-section"></a><span data-ttu-id="190c1-104">QuickStyleVariation Cell (Quick Style Section)</span><span class="sxs-lookup"><span data-stu-id="190c1-104">QuickStyleVariation Cell (Quick Style Section)</span></span>

<span data-ttu-id="190c1-105">Bestimmt, ob die Formeln und die Werte der Text, Linie, innen und Füllung Farbe (oder eine Kombination dieser Eigenschaften) mithilfe von Farben außer Kraft setzen, Kontrast, wobei der Diagrammhintergrund.</span><span class="sxs-lookup"><span data-stu-id="190c1-105">Determines whether to override the formulas and values of text, line, and fill color (or a combination of those properties) by using colors that contrast with the diagram background.</span></span> <span data-ttu-id="190c1-106">Wert ist eine bitweise OR 0, 1, 2, 4 und 8.</span><span class="sxs-lookup"><span data-stu-id="190c1-106">Value is a bitwise OR of 0, 1, 2, 4, and 8.</span></span>
  
|<span data-ttu-id="190c1-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="190c1-107">**Value**</span></span>|<span data-ttu-id="190c1-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="190c1-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="190c1-109">0</span><span class="sxs-lookup"><span data-stu-id="190c1-109">0</span></span>  <br/> |<span data-ttu-id="190c1-110">Text eines Shapes, Zeile oder Füllung Farbe (oder eine beliebige Kombination dieser Eigenschaften), um anhand der angegebenen Hintergrundfarbe des Designs sichtbar bleiben, werden nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="190c1-110">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="190c1-111">1</span><span class="sxs-lookup"><span data-stu-id="190c1-111">1</span></span>  <br/> |<span data-ttu-id="190c1-112">Text eines Shapes, Zeile oder Füllung Farbe (oder eine beliebige Kombination dieser Eigenschaften), um anhand der angegebenen Hintergrundfarbe des Designs sichtbar bleiben, werden nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="190c1-112">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="190c1-113">2</span><span class="sxs-lookup"><span data-stu-id="190c1-113">2</span></span>  <br/> |<span data-ttu-id="190c1-114">Textfarbe eines Shapes, zu ändern, wenn erforderlich ist, um anhand eines Designs gegebene Hintergrundfarbe sichtbar bleiben.</span><span class="sxs-lookup"><span data-stu-id="190c1-114">Alter a shape's text color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="190c1-115">4</span><span class="sxs-lookup"><span data-stu-id="190c1-115">4</span></span>  <br/> |<span data-ttu-id="190c1-116">Linienfarbe eines Shapes, zu ändern, wenn erforderlich ist, um anhand eines Designs gegebene Hintergrundfarbe sichtbar bleiben.</span><span class="sxs-lookup"><span data-stu-id="190c1-116">Alter a shape's line color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="190c1-117">8</span><span class="sxs-lookup"><span data-stu-id="190c1-117">8</span></span>  <br/> |<span data-ttu-id="190c1-118">Füllfarbe einer Form zu ändern, wenn erforderlich ist, um anhand eines Designs gegebene Hintergrundfarbe sichtbar bleiben.</span><span class="sxs-lookup"><span data-stu-id="190c1-118">Alter a shape's fill color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="190c1-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="190c1-119">Remarks</span></span>

<span data-ttu-id="190c1-120">Verwenden Sie die Zelle QuickStyleVariation, um Sichtbarkeit in Text oder Zeilen zu gewährleisten, wenn diese außerhalb alle sichtbaren Shape-Geometrie (beispielsweise in ein Shape, dessen TextBox-Objekt den unteren Rand der Form, wie in Netzwerkdiagramm ist) werden.</span><span class="sxs-lookup"><span data-stu-id="190c1-120">Use the QuickStyleVariation cell to guarantee visibility in either text or lines when they are outside any visible shape geometry (for example, in a shape whose textbox is below the bottom of the shape, such as those in Network Diagrams).</span></span> <span data-ttu-id="190c1-121">Die Zelle Standardwert ist 0, was bedeutet, dass ihr Verhalten inaktiv ist.</span><span class="sxs-lookup"><span data-stu-id="190c1-121">The cell's default value is 0, which means that its behavior is inactive.</span></span> <span data-ttu-id="190c1-122">Ein anderer Wert löst die Zelle Verhalten.</span><span class="sxs-lookup"><span data-stu-id="190c1-122">Any other value triggers the cell's behavior.</span></span>
  
<span data-ttu-id="190c1-123">Der Wert QuickStyleVariation überschreibt den Wert, der von der Funktion THEMEVAL erzeugt wird, während es in die Farbe "(Abschnitt" Character "), FillForegnd oder LineColor Zellen befindet (oder durch direkte Verweise auf diese drei Eigenschaften über THEMEVAL hergestellt (" CharacterColor"), THEMEVAL("FillColor") und THEMEVAL("LineColor")).</span><span class="sxs-lookup"><span data-stu-id="190c1-123">The QuickStyleVariation value overrides the value produced by the THEMEVAL function when it resides in the Color (Character Section), FillForegnd, or LineColor cells (or produced by direct references to these three properties by means of THEMEVAL("CharacterColor"), THEMEVAL("FillColor"), and THEMEVAL("LineColor")).</span></span>
  
<span data-ttu-id="190c1-124">Zum Abrufen eines Verweises auf die Zelle **QuickStyleVariation** nach Namen aus einer anderen Formel durch Abrufen des Werts des **N** -Attributs eines Elements **Zelle** oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="190c1-124">To get a reference to the **QuickStyleVariation** cell by name from another formula, by getting the value of the **N** attribute of a **Cell** element, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="190c1-125">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="190c1-125">Cell name:</span></span>  <br/> |<span data-ttu-id="190c1-126">QuickStyleVariation</span><span class="sxs-lookup"><span data-stu-id="190c1-126">QuickStyleVariation</span></span>  <br/> |
   
<span data-ttu-id="190c1-127">Wenn Sie einen Verweis auf die Zelle **QuickStyleVariation** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="190c1-127">To get a reference to the **QuickStyleVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="190c1-128">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="190c1-128">Section index:</span></span>  <br/> |<span data-ttu-id="190c1-129">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="190c1-129">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="190c1-130">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="190c1-130">Row index:</span></span>  <br/> |<span data-ttu-id="190c1-131">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="190c1-131">**visRowQuickStyleProperties**</span></span> <br/> |
|<span data-ttu-id="190c1-132">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="190c1-132">Cell index:</span></span>  <br/> |<span data-ttu-id="190c1-133">**visQuickStyleVariation**</span><span class="sxs-lookup"><span data-stu-id="190c1-133">**visQuickStyleVariation**</span></span> <br/> |
   

