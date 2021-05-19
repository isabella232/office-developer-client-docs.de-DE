---
title: Zelle "LineColor" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm535
localization_priority: Normal
ms.assetid: d857b48b-9a3d-a1e1-5ad2-6816a492c8ab
description: Definiert die Linienfarbe eines Shapes.
ms.openlocfilehash: d0b4ebee6d96bc67c9ca45e8a6194cb91ed6c7f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416937"
---
# <a name="linecolor-cell-line-format-section"></a><span data-ttu-id="232f9-103">Zelle "LineColor" (Abschnitt "Line Format")</span><span class="sxs-lookup"><span data-stu-id="232f9-103">LineColor Cell (Line Format Section)</span></span>

<span data-ttu-id="232f9-104">Definiert die Linienfarbe eines Shapes.</span><span class="sxs-lookup"><span data-stu-id="232f9-104">Determines the line color of the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="232f9-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="232f9-105">Remarks</span></span>

<span data-ttu-id="232f9-106">Geben Sie zum Festlegen der Linienfarbe eine Zahl zwischen 0 und 23 ein, bei der es sich um einen Index in einer Auflistung von Linienfarben handelt.</span><span class="sxs-lookup"><span data-stu-id="232f9-106">To set the line color, enter a number from 0 to 23, which is an index into a collection of line colors.</span></span> <span data-ttu-id="232f9-107">Sie können die Linienfarbsammlung im Dialogfeld Linie anzeigen (klicken Sie auf der Registerkarte **Start** in der **Gruppe Shape** auf **Linie,** zeigen Sie auf **Gewichtung,** und klicken Sie dann auf **Weitere Linien**). </span><span class="sxs-lookup"><span data-stu-id="232f9-107">You can view the line color collection in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span> <span data-ttu-id="232f9-108">Sie können den Wert von LineColor auch im Dialogfeld **Zeile** festlegen.</span><span class="sxs-lookup"><span data-stu-id="232f9-108">You can also set the value of LineColor in the **Line** dialog box.</span></span> 
  
<span data-ttu-id="232f9-109">Verwenden Sie zum Eingeben einer benutzerdefinierten Farbe die RGB- oder HSL-Funktion.</span><span class="sxs-lookup"><span data-stu-id="232f9-109">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="232f9-110">Der Wert einer benutzerdefinierten Farbe ist die RGB-Farbe, und RGB( *r, g, b*), anstatt eine Zahl, wird im ShapeSheet-Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="232f9-110">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="232f9-111">Bei Verwendung in numerischen Vorgängen haben benutzerdefinierte Farben Werte von 24 und höher.</span><span class="sxs-lookup"><span data-stu-id="232f9-111">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="232f9-112">Die Transparenz der Linienfarbe können Sie in der Zelle LineColorTrans festlegen.</span><span class="sxs-lookup"><span data-stu-id="232f9-112">You can set the transparency of the line color in the LineColorTrans cell.</span></span>
  
<span data-ttu-id="232f9-113">Verwenden Sie zum Erhalten eines Verweises auf die Zelle LineColor anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="232f9-113">To get a reference to the LineColor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="232f9-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="232f9-114">Cell name:</span></span>  <br/> |<span data-ttu-id="232f9-115">LineColor</span><span class="sxs-lookup"><span data-stu-id="232f9-115">LineColor</span></span>  <br/> |
   
<span data-ttu-id="232f9-116">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die LineColor-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="232f9-116">To get a reference to the LineColor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="232f9-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="232f9-117">Section index:</span></span>  <br/> |<span data-ttu-id="232f9-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="232f9-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="232f9-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="232f9-119">Row index:</span></span>  <br/> |<span data-ttu-id="232f9-120">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="232f9-120">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="232f9-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="232f9-121">Cell index:</span></span>  <br/> |<span data-ttu-id="232f9-122">**visLineColor**</span><span class="sxs-lookup"><span data-stu-id="232f9-122">**visLineColor**</span></span> <br/> |
   

