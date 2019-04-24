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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345320"
---
# <a name="about-the-formula-tracing-window"></a><span data-ttu-id="3b6e8-103">Informationen zum Fenster "Formelprotokollierung"</span><span class="sxs-lookup"><span data-stu-id="3b6e8-103">About the Formula Tracing Window</span></span>

<span data-ttu-id="3b6e8-104">Das Fenster **Formelprotokollierung** bietet Shape-Entwicklern Informationen über gegenseitige Abhängigkeiten zwischen Zellen, sowohl für abhängige Zellen (Zellen mit einer Abhängigkeit gegenüber einer bestimmten Zelle) als auch für Vorgängerzellen (Zellen, von denen eine bestimmte Zelle abhängt).</span><span class="sxs-lookup"><span data-stu-id="3b6e8-104">The **Formula Tracing** window is designed to provide shape developers with information about cell interdependencies—both dependent cells (cells that have a dependency on a given cell), and precedent cells (cells that a given cell depends on).</span></span> 
  
<span data-ttu-id="3b6e8-105">Die Zellen in einem Microsoft Visio-ShapeSheet enthalten Werte und Formeln.</span><span class="sxs-lookup"><span data-stu-id="3b6e8-105">The cells in a Microsoft Visio ShapeSheet contain values and formulas.</span></span> <span data-ttu-id="3b6e8-106">Formeln können wiederum Verweise auf andere Zellen enthalten, sodass Sie die Möglichkeit haben, einen Wert in einer Zelle basierend auf dem Wert einer anderen Zelle zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="3b6e8-106">Formulas can, in turn, have references to other cells, giving you the power to calculate a value in one cell based on another cell's value.</span></span> <span data-ttu-id="3b6e8-107">Beim Erstellen und Verwalten komplexer Shapes ist das Erkennen all dieser Abhängigkeiten jedoch unter Umständen sehr schwierig, da eine Formel auf eine beliebige Zelle in der Zeichnung verweisen kann, wobei es egal ist, ob es sich um eine Zelle in demselben ShapeSheet oder um eine Zelle eines anderen Objekts in der Zeichnung handelt, beispielsweise um eine Seite, eine Formatvorlage, einen Master oder ein anderes Shape.</span><span class="sxs-lookup"><span data-stu-id="3b6e8-107">When creating or maintaining complex shapes, however, it can be difficult to identify all these interdependencies because a formula can reference any cell in the drawing, whether it's a cell in the same ShapeSheet, or a cell belonging to another object in the drawing, for example, a page, style, master, or another shape.</span></span> 
  
<span data-ttu-id="3b6e8-108">Das Fenster für die **Formelprotokollierung** enthält Informationen, die Ihnen helfen, die Auswirkungen von Änderungen, die Sie an Zellen vornehmen, zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="3b6e8-108">The **Formula Tracing** window provides information to help you understand the implications of changes you make to cells.</span></span> 
  
## <a name="displaying-the-formula-tracing-window"></a><span data-ttu-id="3b6e8-109">Anzeigen des Fensters für die Formelprotokollierung</span><span class="sxs-lookup"><span data-stu-id="3b6e8-109">Displaying the Formula Tracing Window</span></span>

<span data-ttu-id="3b6e8-110">Klicken Sie zum Anzeigen des Fensters für die **Formel Ablaufverfolgung** , wobei das ShapeSheet-Fenster aktiv ist, unter **ShapeSheet-Tools** auf der Registerkarte \* \* Design \* \* in der Gruppe **Formelprotokollierung** auf **Fenster anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="3b6e8-110">To view the **Formula Tracing** window, with the ShapeSheet window active, under **ShapeSheet Tools** on the \*\* Design \*\* tab, in the **Formula Tracing** group, click **Show Window**.</span></span> <span data-ttu-id="3b6e8-111">Das Fenster für die **Formelprotokollierung** wird standardmäßig im ShapeSheet-Fenster angedockt, es handelt sich jedoch um ein verankertes Fenster, das angedockt, unverankert oder mit anderen verfügbaren verankerten ShapeSheet-Fenstern zusammengeführt werden kann, beispielsweise im Fenster **Format-Explorer** .</span><span class="sxs-lookup"><span data-stu-id="3b6e8-111">The **Formula Tracing** window appears docked in the ShapeSheet window by default, but is an anchored window that can be docked, floated or merged with other available anchored ShapeSheet windows, for example, the **Style Explorer** window.</span></span> 
  
## <a name="tracing-dependent-cells"></a><span data-ttu-id="3b6e8-112">Verfolgen abhängiger Zellen</span><span class="sxs-lookup"><span data-stu-id="3b6e8-112">Tracing dependent cells</span></span>

<span data-ttu-id="3b6e8-p103">Zum Anzeigen einer Liste von Zellen, die von einer bestimmten Zelle abhängig sind, wählen Sie die betreffende Zelle im ShapeSheet-Fenster aus. In diesem Beispiel ist die Zelle Width ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="3b6e8-p103">To see a list of cells that are dependent on a particular cell, select that cell in the ShapeSheet window. In this example, the Width cell is selected.</span></span> 
  
![Die Zelle "width" ist ausgewählt](media/ShapeSheetDependents_UI_01_ZA01039814.gif)
  
<span data-ttu-id="3b6e8-116">Um die abhängigen Zellen anzuzeigen, klicken Sie in der Gruppe **Formelprotokollierung**auf **Ablauf Verfolgungs abhängige**.</span><span class="sxs-lookup"><span data-stu-id="3b6e8-116">To view its dependent cells, in the **Formula Tracing**group, click **Trace Dependents**.</span></span>
  
<span data-ttu-id="3b6e8-117">Eine Liste aller Zellen mit einer Abhängigkeit von der Zelle Breite wird im Fenster **Formelprotokollierung** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3b6e8-117">A list of all the cells with a dependency on the Width cell appears in the **Formula Tracing** window.</span></span> <span data-ttu-id="3b6e8-118">Sie können zu einer beliebigen Zelle in der Liste navigieren, indem Sie im Fenster **Formelprotokollierung** auf den entsprechenden Eintrag doppelklicken.</span><span class="sxs-lookup"><span data-stu-id="3b6e8-118">You can navigate to any cell in the list by double-clicking its entry in the **Formula Tracing** window.</span></span> 
  
![Alle Zellen mit einer Abhängigkeit von der Zelle "Breite" werden im Fenster "Formel Ablaufverfolgung" angezeigt.](media/ShapeSheetDependents_UI_02_ZA01039815.gif)
  
## <a name="tracing-precendent-cells"></a><span data-ttu-id="3b6e8-120">NachVerfolgen von precendent-Zellen</span><span class="sxs-lookup"><span data-stu-id="3b6e8-120">Tracing precendent cells</span></span>

<span data-ttu-id="3b6e8-p105">Wenn eine Liste aller Zellen angezeigt werden soll, von denen eine bestimmte Zelle abhängt, wählen Sie zunächst die Zelle im ShapeSheet-Fenster aus. In diesem Beispiel ist die Zelle Geometry1.X2 ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="3b6e8-p105">To see a list of cells that a particular cell is dependent upon, first select the cell in the ShapeSheet window. In this example, the Geometry1.X2 cell is selected.</span></span> 
  
![Zelle Geometry1. x2 ist ausgewählt](media/ShapeSheetPrecedents_UI_01_ZA01039817.gif)
  
<span data-ttu-id="3b6e8-124">Zum Anzeigen der Vorgängerzellen klicken Sie in der Gruppe **Formelprotokollierung**auf **Vorgänger**-Traces.</span><span class="sxs-lookup"><span data-stu-id="3b6e8-124">To view its precedent cells, in the **Formula Tracing**group, click **Trace Precedents**.</span></span>
  
<span data-ttu-id="3b6e8-125">Eine Liste aller Zellen, von denen die Zelle Geometry1. x2 abhängig ist, wird im Fenster **Formelprotokollierung** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3b6e8-125">A list of all the cells that the Geometry1.X2 cell is dependent upon appears in the **Formula Tracing** window.</span></span> <span data-ttu-id="3b6e8-126">Sie können zu einer beliebigen Zelle in der Liste navigieren, indem Sie im Fenster **Formelprotokollierung** auf den entsprechenden Eintrag doppelklicken.</span><span class="sxs-lookup"><span data-stu-id="3b6e8-126">You can navigate to any cell in the list by double-clicking its entry in the **Formula Tracing** window.</span></span> 
  
![Alle Zellen, von denen die Zelle Geometry1. x2 abhängig ist, werden im Fenster Formelprotokollierung angezeigt.](media/ShapeSheetPrecedents_UI_02_ZA01039818.gif)
  

