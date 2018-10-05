---
title: Informationen zum Formelprotokollierungsfenster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm60118
localization_priority: Normal
ms.assetid: 0cdacd4e-74dc-32c3-2eb2-219bf7fcb532
description: Das Fenster Formelprotokollierung bietet Shape-Entwicklern Informationen über gegenseitige Abhängigkeiten zwischen Zellen, sowohl für abhängige Zellen (Zellen mit einer Abhängigkeit gegenüber einer bestimmten Zelle) als auch für Vorgängerzellen (Zellen, von denen eine bestimmte Zelle abhängt).
ms.openlocfilehash: f5f9d6a7ba3ab7049715d31342cfe7aa68ea053f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385326"
---
# <a name="about-the-formula-tracing-window"></a><span data-ttu-id="ac1fc-103">Informationen zur zum Formelablauffenster</span><span class="sxs-lookup"><span data-stu-id="ac1fc-103">About the Formula Tracing Window</span></span>

<span data-ttu-id="ac1fc-104">Das Fenster **Formelprotokollierung** bietet Shape-Entwicklern Informationen über gegenseitige Abhängigkeiten zwischen Zellen, sowohl für abhängige Zellen (Zellen mit einer Abhängigkeit gegenüber einer bestimmten Zelle) als auch für Vorgängerzellen (Zellen, von denen eine bestimmte Zelle abhängt).</span><span class="sxs-lookup"><span data-stu-id="ac1fc-104">The **Formula Tracing** window is designed to provide shape developers with information about cell interdependencies—both dependent cells (cells that have a dependency on a given cell), and precedent cells (cells that a given cell depends on).</span></span> 
  
<span data-ttu-id="ac1fc-105">Die Zellen in einem Microsoft Visio-ShapeSheet enthalten Werte und Formeln.</span><span class="sxs-lookup"><span data-stu-id="ac1fc-105">The cells in a Microsoft Visio ShapeSheet contain values and formulas.</span></span> <span data-ttu-id="ac1fc-106">Formeln können wiederum Verweise auf andere Zellen, was Ihnen die Möglichkeit, einen Wert in einer Zelle basierend auf einer anderen Zelle Wert berechnen lassen.</span><span class="sxs-lookup"><span data-stu-id="ac1fc-106">Formulas can, in turn, have references to other cells, giving you the power to calculate a value in one cell based on another cell's value.</span></span> <span data-ttu-id="ac1fc-107">Beim Erstellen oder Verwalten komplexer Shapes, kann jedoch es schwierig sein, alle diese Abhängigkeiten identifiziert werden, da eine Formel, die eine beliebige Zelle in der Zeichnung verwiesen werden kann, ob es sich um eine Zelle in der gleichen ShapeSheet oder eine Zelle, die in ein anderes Objekt in der Zeichnung gehören ist, beispielsweise einer Seite, Formatvorlage, Master-Shape oder eine andere Form.</span><span class="sxs-lookup"><span data-stu-id="ac1fc-107">When creating or maintaining complex shapes, however, it can be difficult to identify all these interdependencies because a formula can reference any cell in the drawing, whether it's a cell in the same ShapeSheet, or a cell belonging to another object in the drawing, for example, a page, style, master, or another shape.</span></span> 
  
<span data-ttu-id="ac1fc-108">Im Fenster **Formelprotokollierung** enthält Informationen, mit denen das Verständnis die Auswirkungen von Änderungen, die Sie Zellen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="ac1fc-108">The **Formula Tracing** window provides information to help you understand the implications of changes you make to cells.</span></span> 
  
## <a name="displaying-the-formula-tracing-window"></a><span data-ttu-id="ac1fc-109">Anzeigen von Formelprotokollierungsfenster</span><span class="sxs-lookup"><span data-stu-id="ac1fc-109">Displaying the Formula Tracing Window</span></span>

<span data-ttu-id="ac1fc-110">So zeigen Sie das Fenster **Formelprotokollierung** im ShapeSheet-Fenster aktiv ist, klicken Sie unter **ShapeSheet-Tools** auf an der \*\* Design \*\* klicken auf der Registerkarte in der Gruppe **Formelprotokollierung** **Fenster anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="ac1fc-110">To view the **Formula Tracing** window, with the ShapeSheet window active, under **ShapeSheet Tools** on the \*\* Design \*\* tab, in the **Formula Tracing** group, click **Show Window**.</span></span> <span data-ttu-id="ac1fc-111">**Das Formelprotokollierungsfenster** angedockten im ShapeSheet-Fenster wird standardmäßig angezeigt, jedoch ist ein verankertes Fenster, das angedockt, Mauszeiger halten oder zusammengeführt werden kann mit anderen verfügbaren verankerten ShapeSheet-Fenster, beispielsweise das **Format-Explorer** -Fenster.</span><span class="sxs-lookup"><span data-stu-id="ac1fc-111">The **Formula Tracing** window appears docked in the ShapeSheet window by default, but is an anchored window that can be docked, floated or merged with other available anchored ShapeSheet windows, for example, the **Style Explorer** window.</span></span> 
  
## <a name="tracing-dependent-cells"></a><span data-ttu-id="ac1fc-112">Verfolgen abhängiger Zellen</span><span class="sxs-lookup"><span data-stu-id="ac1fc-112">Tracing dependent cells</span></span>

<span data-ttu-id="ac1fc-p103">Zum Anzeigen einer Liste von Zellen, die von einer bestimmten Zelle abhängig sind, wählen Sie die betreffende Zelle im ShapeSheet-Fenster aus. In diesem Beispiel ist die Zelle Width ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="ac1fc-p103">To see a list of cells that are dependent on a particular cell, select that cell in the ShapeSheet window. In this example, the Width cell is selected.</span></span> 
  
![Zelle "Width" aktiviert ist](media/ShapeSheetDependents_UI_01_ZA01039814.gif)
  
<span data-ttu-id="ac1fc-116">Klicken Sie zum Anzeigen von ihr abhängigen Zellen klicken, in der Gruppe **Formelprotokollierung**auf **Spur zum Nachfolger**.</span><span class="sxs-lookup"><span data-stu-id="ac1fc-116">To view its dependent cells, in the **Formula Tracing**group, click **Trace Dependents**.</span></span>
  
<span data-ttu-id="ac1fc-p104">Eine Liste aller von der Zelle Width abhängigen Zellen wird im Fenster Formelprotokollierung angezeigt. Sie können zu einer beliebigen Zelle in der Liste navigieren, indem Sie auf den entsprechenden Eintrag im Fenster Formelprotokollierung doppelklicken.</span><span class="sxs-lookup"><span data-stu-id="ac1fc-p104">A list of all the cells with a dependency on the Width cell appears in the **Formula Tracing** window. You can navigate to any cell in the list by double-clicking its entry in the **Formula Tracing** window.</span></span> 
  
![Alle Zellen mit einer Abhängigkeit auf die Zelle Width angezeigt werden, klicken Sie im Fenster Formelprotokollierung](media/ShapeSheetDependents_UI_02_ZA01039815.gif)
  
## <a name="tracing-precendent-cells"></a><span data-ttu-id="ac1fc-120">Verfolgen Precendent Zellen</span><span class="sxs-lookup"><span data-stu-id="ac1fc-120">Tracing precendent cells</span></span>

<span data-ttu-id="ac1fc-p105">Wenn eine Liste aller Zellen angezeigt werden soll, von denen eine bestimmte Zelle abhängt, wählen Sie zunächst die Zelle im ShapeSheet-Fenster aus. In diesem Beispiel ist die Zelle Geometry1.X2 ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="ac1fc-p105">To see a list of cells that a particular cell is dependent upon, first select the cell in the ShapeSheet window. In this example, the Geometry1.X2 cell is selected.</span></span> 
  
![Geometry1.X2 Zelle ist ausgewählt.](media/ShapeSheetPrecedents_UI_01_ZA01039817.gif)
  
<span data-ttu-id="ac1fc-124">Klicken Sie zum Anzeigen ihrer Vorgängerzellen klicken, in der Gruppe **Formelprotokollierung**auf **Spur zum Vorgänger**.</span><span class="sxs-lookup"><span data-stu-id="ac1fc-124">To view its precedent cells, in the **Formula Tracing**group, click **Trace Precedents**.</span></span>
  
<span data-ttu-id="ac1fc-125">Eine Liste aller Zellen, die die Zelle Geometry1.X2 abhängig ist, wird im Fenster **Formelprotokollierung** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ac1fc-125">A list of all the cells that the Geometry1.X2 cell is dependent upon appears in the **Formula Tracing** window.</span></span> <span data-ttu-id="ac1fc-126">Sie können auf eine beliebige Zelle in der Liste navigieren, indem Sie den Eintrag im Fenster **Formelprotokollierung** doppelklicken.</span><span class="sxs-lookup"><span data-stu-id="ac1fc-126">You can navigate to any cell in the list by double-clicking its entry in the **Formula Tracing** window.</span></span> 
  
![Alle Zellen, denen die Zelle Geometry1.X2 abhängig ist angezeigt wird, klicken Sie im Fenster Formelprotokollierung](media/ShapeSheetPrecedents_UI_02_ZA01039818.gif)
  

