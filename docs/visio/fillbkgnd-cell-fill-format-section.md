---
title: Zelle "FillBkgnd" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm365
localization_priority: Normal
ms.assetid: 603d698f-a025-538c-8767-18e7716a9a5f
description: Legt die Farbe fest, die für den Hintergrund (Füllbereich) des Füllmusters des Shapes verwendet wird.
ms.openlocfilehash: f4df5d2b44a50380c996b9b2e0f7cda7d212093b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436643"
---
# <a name="fillbkgnd-cell-fill-format-section"></a><span data-ttu-id="e07fe-103">Zelle "FillBkgnd" (Abschnitt "Fill Format")</span><span class="sxs-lookup"><span data-stu-id="e07fe-103">FillBkgnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="e07fe-104">Legt die Farbe fest, die für den Hintergrund (Füllbereich) des Füllmusters des Shapes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e07fe-104">Determines the color used for the background (fill) of the shape's fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e07fe-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e07fe-105">Remarks</span></span>

<span data-ttu-id="e07fe-106">Wenn Sie die Farbe festlegen möchten, geben Sie eine Zahl von 0 bis 23 ein.</span><span class="sxs-lookup"><span data-stu-id="e07fe-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="e07fe-107">Verwenden Sie zum Eingeben einer benutzerdefinierten Farbe die RGB- oder HSL-Funktion.</span><span class="sxs-lookup"><span data-stu-id="e07fe-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="e07fe-108">Der Wert einer benutzerdefinierten Farbe ist die RGB-Farbe, und RGB(*r, g, b*), anstatt eine Zahl, wird im ShapeSheet-Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e07fe-108">The value of a custom color is its RGB color, and RGB(*r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="e07fe-109">Bei Verwendung in numerischen Vorgängen haben benutzerdefinierte Farben Werte von 24 und höher.</span><span class="sxs-lookup"><span data-stu-id="e07fe-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="e07fe-110">Die Fülltransparenz für den Hintergrund können Sie in der Zelle FillBkgndTrans festlegen.</span><span class="sxs-lookup"><span data-stu-id="e07fe-110">You can set the transparency of the background fill in the FillBkgndTrans cell.</span></span> 
  
<span data-ttu-id="e07fe-111">Um einen Verweis auf die FillBkgnd-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="e07fe-111">To get a reference to the FillBkgnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e07fe-112">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="e07fe-112">Cell name:</span></span>  <br/> | <span data-ttu-id="e07fe-113">FillBkgnd</span><span class="sxs-lookup"><span data-stu-id="e07fe-113">FillBkgnd</span></span>  <br/> |
   
<span data-ttu-id="e07fe-114">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die FillBkgnd-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="e07fe-114">To get a reference to the FillBkgnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e07fe-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="e07fe-115">Section index:</span></span>  <br/> |<span data-ttu-id="e07fe-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e07fe-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e07fe-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="e07fe-117">Row index:</span></span>  <br/> |<span data-ttu-id="e07fe-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="e07fe-118">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="e07fe-119">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="e07fe-119">Cell index:</span></span>  <br/> |<span data-ttu-id="e07fe-120">**visFillBkgnd**</span><span class="sxs-lookup"><span data-stu-id="e07fe-120">**visFillBkgnd**</span></span> <br/> |
   

