---
title: Informationen zum Formatexplorerfenster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm60119
localization_priority: Normal
ms.assetid: bfdc1a63-c355-c759-bdfa-ce27e3ad10e7
description: Das Format-Explorer-Fenster bietet Shape-Entwickler schnell bestimmen, welche Shape-Zellen erben Sie von einer bestimmten Formatvorlage oder die Formatvorlage, von der eine Zelle seinen Wert erbt.
ms.openlocfilehash: 25af478b8ac4e35c7ae0b88bf69aad21d679da17
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796356"
---
# <a name="about-the-style-explorer-window"></a><span data-ttu-id="4c0e3-103">Informationen zum Formatexplorerfenster</span><span class="sxs-lookup"><span data-stu-id="4c0e3-103">About the Style Explorer Window</span></span>

<span data-ttu-id="4c0e3-104">Das **Format-Explorer** -Fenster bietet Shape-Entwickler schnell bestimmen, welche Shape-Zellen erben Sie von einer bestimmten Formatvorlage oder die Formatvorlage, von der eine Zelle seinen Wert erbt.</span><span class="sxs-lookup"><span data-stu-id="4c0e3-104">The **Style Explorer** window provides shape developers with a quick way to determine which shape cells inherit from a given style, or the style from which a given cell inherits its value.</span></span> 
  
<span data-ttu-id="4c0e3-p101">Formatvorlagen sind benannte Sammlungen von Formatierungsattributen, die auf ein Shape angewendet werden können. In Microsoft Visio können in einer einzigen Formatvorlage Text-, Zeilen- und Füllattribute als effiziente Möglichkeit zum Sicherstellen der Konsistenz in Shapes eingebunden werden. Zudem kann eine Formatvorlage für eine Klasse von Attributen (Text, Linien und Füllung) oder eine beliebige Kombinationen von Attributen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="4c0e3-p101">Styles are named collections of formatting attributes that you can apply to a shape. In Microsoft Visio, a single style can define text, line, and fill attributes as an efficient way to ensure consistency in your shapes. Additionally, you can also define a style for any one class of attribute (text, line, or fill) or any combination of attributes.</span></span> 
  
<span data-ttu-id="4c0e3-108">Im Gegensatz zu Shapes, auf die Sie Formatierungsattribute individuell angewendet haben, stellen Shapes mit Formatierungseinstellungen aus Formatvorlagen nicht nur die Konsistenz sicher. Sie bieten auch beim Erstellen, Verschieben, Skalieren und Drehen eine höhere Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="4c0e3-108">Unlike shapes to which you've applied formatting attributes individually, shapes that derive their formatting from a style not only ensure consistency but also respond better when they are created, moved, scaled, or rotated.</span></span> 
  
<span data-ttu-id="4c0e3-109">Das **Format-Explorer** -Fenster enthält die Informationen, die Sie die Auswirkungen von Änderungen besser zu verstehen, die Sie Shapes vornehmen müssen.</span><span class="sxs-lookup"><span data-stu-id="4c0e3-109">The **Style Explorer** window provides the information you need to understand better the implications of changes you make to shapes.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4c0e3-110">Im ShapeSheet-Fenster schwarz formatiert angezeigte Zellenwerte sind geerbte Werte, blau formatierte Werte sind lokale Werte.</span><span class="sxs-lookup"><span data-stu-id="4c0e3-110">Cell values that appear black in the ShapeSheet window are inherited; those that appear blue are local.</span></span> 
  
## <a name="using-the-style-explorer-window"></a><span data-ttu-id="4c0e3-111">Verwenden des Fensters "Format-Explorer"</span><span class="sxs-lookup"><span data-stu-id="4c0e3-111">Using the Style Explorer window</span></span>

<span data-ttu-id="4c0e3-112">Wählen Sie **Format-Explorer**aus, um das **Format-Explorer** -Fenster, in das ShapeSheet-Fenster aktiv ist, klicken Sie auf der Registerkarte **ShapeSheet-Tools – Entwurf** in der Gruppe **Ansicht** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4c0e3-112">To view the **Style Explorer** window, with the ShapeSheet window active, on the **ShapeSheet Tools Design** tab, in the **View** group, select **Style Explorer**.</span></span> <span data-ttu-id="4c0e3-113">Das **Format-Explorer** -Fenster angedockt im ShapeSheet-Fenster wird standardmäßig angezeigt, jedoch ist ein verankertes Fenster, das angedockt werden kann, Mauszeiger halten, oder mit anderen verfügbaren verankerten ShapeSheet-Fenster, **beispielsweise das Formelprotokollierungsfenster** zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="4c0e3-113">The **Style Explorer** window appears docked in the ShapeSheet window by default, but is an anchored window that can be docked, floated, or merged with other available anchored ShapeSheet windows, for example, the **Formula Tracing** window.</span></span> <span data-ttu-id="4c0e3-114">Das Fenster **Format-Explorer** enthält eine Baumstruktur aller Formatvorlagen, die in der aktuellen Zeichnung definiert.</span><span class="sxs-lookup"><span data-stu-id="4c0e3-114">The **Style Explorer** window contains a treeview display of all the styles defined in the current drawing.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4c0e3-115">Wenn Sie Informationen über eine Formatvorlage erhalten möchten, können Sie die Formatvorlage im Fenster **Format-Explorer** auf das dazugehörige ShapeSheet anzuzeigen mit der Maustaste.</span><span class="sxs-lookup"><span data-stu-id="4c0e3-115">To get information about a style, you can right-click the style in the **Style Explorer** window to view its ShapeSheet.</span></span> 
  
<span data-ttu-id="4c0e3-116">Das Fenster **Format-Explorer** enthält die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="4c0e3-116">The **Style Explorer** window provides the following information:</span></span> 
  
- <span data-ttu-id="4c0e3-117">Die Zellen, die ihre Werte aus einer ausgewählten Formatvorlage erben. Beim Auswählen einer Formatvorlage im Fenster **Format-Explorer** werden alle Zellen im ShapeSheet-Fenster, die von der Formatvorlage erben ohne Schraffierung, während Zellen, die nicht von der Formatvorlage erben, hell schraffiert dargestellt werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4c0e3-117">The cells that inherit their values from a selected style.When you select a style in the **Style Explorer** window, all cells in the ShapeSheet window that inherit from that style appear without hatching, while cells that do not inherit from that style appear lightly hatched.</span></span> 
    
- <span data-ttu-id="4c0e3-118">Informationen über die Formatvorlage, von der eine ausgewählte Zelle ihren Wert erbt.Beim Auswählen einer ShapeSheet-Zelle wird die Formatvorlage, von der sie ihren Wert erbt, auf der Taskleiste unterhalb des ShapeSheet-Fensters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4c0e3-118">The style from which a selected cell inherits its value.When you select a ShapeSheet cell, the style from which it inherits its value is displayed on the taskbar under the ShapeSheet window.</span></span> 
    

