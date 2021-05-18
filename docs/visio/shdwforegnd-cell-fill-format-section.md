---
title: Zelle "ShdwForegnd" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251244
localization_priority: Normal
ms.assetid: ea153390-631d-79fd-c1ba-4c281239a24e
description: Legt die Farbe fest, die für den Vordergrund (Pinselstrich) des Schattenfüllmusters des Shapes verwendet wird.
ms.openlocfilehash: 602df83dcb88d4137b0609f9a8b1084a40148a10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422250"
---
# <a name="shdwforegnd-cell-fill-format-section"></a><span data-ttu-id="bcd9a-103">Zelle "ShdwForegnd" (Abschnitt "Fill Format")</span><span class="sxs-lookup"><span data-stu-id="bcd9a-103">ShdwForegnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="bcd9a-104">Legt die Farbe fest, die für den Vordergrund (Pinselstrich) des Schattenfüllmusters des Shapes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bcd9a-104">Determines the color used for the foreground (stroke) of the shape's drop shadow fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bcd9a-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bcd9a-105">Remarks</span></span>

<span data-ttu-id="bcd9a-106">Wenn Sie die Farbe festlegen möchten, geben Sie eine Zahl von 0 bis 23 ein.</span><span class="sxs-lookup"><span data-stu-id="bcd9a-106">To set the color, enter a number from 0 to 23, which is an index into a collection of colors.</span></span>
  
<span data-ttu-id="bcd9a-107">Verwenden Sie zum Eingeben einer benutzerdefinierten Farbe die RGB- oder HSL-Funktion.</span><span class="sxs-lookup"><span data-stu-id="bcd9a-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="bcd9a-108">Der Wert einer benutzerdefinierten Farbe ist die RGB-Farbe, und RGB( *r, g, b*), anstatt eine Zahl, wird im ShapeSheet-Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bcd9a-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="bcd9a-109">Bei Verwendung in numerischen Vorgängen haben benutzerdefinierte Farben Werte von 24 und höher.</span><span class="sxs-lookup"><span data-stu-id="bcd9a-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="bcd9a-110">Sie können die Transparenz der Farbe für den Vordergrund des Schattenfüllmusters des Shapes in der Zelle ShdwForegndTrans festlegen.</span><span class="sxs-lookup"><span data-stu-id="bcd9a-110">You can set the transparency of the foreground color of the shape's drop shadow fill pattern in the ShdwForegndTrans cell.</span></span>
  
<span data-ttu-id="bcd9a-111">Um einen Verweis auf die Zelle ShdwForegnd anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="bcd9a-111">To get a reference to the ShdwForegnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bcd9a-112">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="bcd9a-112">Cell name:</span></span>  <br/> | <span data-ttu-id="bcd9a-113">ShdwForegnd</span><span class="sxs-lookup"><span data-stu-id="bcd9a-113">ShdwForegnd</span></span>  <br/> |
   
<span data-ttu-id="bcd9a-114">Um einen Verweis auf die ShdwForegnd-Zelle nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="bcd9a-114">To get a reference to the ShdwForegnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bcd9a-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="bcd9a-115">Section index:</span></span>  <br/> |<span data-ttu-id="bcd9a-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bcd9a-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bcd9a-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="bcd9a-117">Row index:</span></span>  <br/> |<span data-ttu-id="bcd9a-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="bcd9a-118">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="bcd9a-119">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="bcd9a-119">Cell index:</span></span>  <br/> |<span data-ttu-id="bcd9a-120">**visFillShdwForegnd**</span><span class="sxs-lookup"><span data-stu-id="bcd9a-120">**visFillShdwForegnd**</span></span> <br/> |
   

