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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322512"
---
# <a name="fillbkgnd-cell-fill-format-section"></a><span data-ttu-id="0fc59-103">Zelle "FillBkgnd" (Abschnitt "Fill Format")</span><span class="sxs-lookup"><span data-stu-id="0fc59-103">FillBkgnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="0fc59-104">Legt die Farbe fest, die für den Hintergrund (Füllbereich) des Füllmusters des Shapes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0fc59-104">Determines the color used for the background (fill) of the shape's fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0fc59-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0fc59-105">Remarks</span></span>

<span data-ttu-id="0fc59-106">Wenn Sie die Farbe festlegen möchten, geben Sie eine Zahl von 0 bis 23 ein.</span><span class="sxs-lookup"><span data-stu-id="0fc59-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="0fc59-107">Verwenden Sie die RGB-oder die GSL-Funktion, um eine benutzerdefinierte Farbe einzugeben.</span><span class="sxs-lookup"><span data-stu-id="0fc59-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="0fc59-108">Der Wert einer benutzerdefinierten Farbe ist ihre RGB-Farbe, und RGB (*r, g, b*) anstelle einer Zahl wird im ShapeSheet-Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0fc59-108">The value of a custom color is its RGB color, and RGB(*r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="0fc59-109">Bei numerischen Vorgängen haben benutzerdefinierte Farben Werte von 24 und höher.</span><span class="sxs-lookup"><span data-stu-id="0fc59-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="0fc59-110">Die Fülltransparenz für den Hintergrund können Sie in der Zelle FillBkgndTrans festlegen.</span><span class="sxs-lookup"><span data-stu-id="0fc59-110">You can set the transparency of the background fill in the FillBkgndTrans cell.</span></span> 
  
<span data-ttu-id="0fc59-111">Wenn Sie einen Verweis auf die Zelle Zelle FillBkgnd aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="0fc59-111">To get a reference to the FillBkgnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0fc59-112">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="0fc59-112">Cell name:</span></span>  <br/> | <span data-ttu-id="0fc59-113">Zelle FillBkgnd</span><span class="sxs-lookup"><span data-stu-id="0fc59-113">FillBkgnd</span></span>  <br/> |
   
<span data-ttu-id="0fc59-114">Wenn Sie einen Verweis auf die Zelle Zelle FillBkgnd aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="0fc59-114">To get a reference to the FillBkgnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0fc59-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="0fc59-115">Section index:</span></span>  <br/> |<span data-ttu-id="0fc59-116">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0fc59-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0fc59-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="0fc59-117">Row index:</span></span>  <br/> |<span data-ttu-id="0fc59-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="0fc59-118">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="0fc59-119">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="0fc59-119">Cell index:</span></span>  <br/> |<span data-ttu-id="0fc59-120">**visFillBkgnd**</span><span class="sxs-lookup"><span data-stu-id="0fc59-120">**visFillBkgnd**</span></span> <br/> |
   

