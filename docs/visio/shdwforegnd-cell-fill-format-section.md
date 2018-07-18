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
ms.openlocfilehash: f39109a296949d23142017661bb55f0708402d8f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798085"
---
# <a name="shdwforegnd-cell-fill-format-section"></a><span data-ttu-id="5d6d3-103">ShdwForegnd Cell (Fill Format Section)</span><span class="sxs-lookup"><span data-stu-id="5d6d3-103">ShdwForegnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="5d6d3-104">Legt die Farbe fest, die für den Vordergrund (Pinselstrich) des Schattenfüllmusters des Shapes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5d6d3-104">Determines the color used for the foreground (stroke) of the shape's drop shadow fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5d6d3-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d6d3-105">Remarks</span></span>

<span data-ttu-id="5d6d3-106">Wenn Sie die Farbe festlegen möchten, geben Sie eine Zahl von 0 bis 23 ein.</span><span class="sxs-lookup"><span data-stu-id="5d6d3-106">To set the color, enter a number from 0 to 23, which is an index into a collection of colors.</span></span>
  
<span data-ttu-id="5d6d3-107">Um eine benutzerdefinierte Farbe eingeben möchten, verwenden Sie die RGB oder HSL-Funktion.</span><span class="sxs-lookup"><span data-stu-id="5d6d3-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="5d6d3-108">Der Wert einer benutzerdefinierten Farbe ist ihre RGB-Farbe und RGB ( *R, g, b*), anstatt eine Zahl in das ShapeSheet-Fenster angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5d6d3-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="5d6d3-109">Bei Verwendung in numerischen Operationen haben benutzerdefinierte Farben Werte von 24 und höher.</span><span class="sxs-lookup"><span data-stu-id="5d6d3-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="5d6d3-110">Sie können die Transparenz der Farbe für den Vordergrund des Schattenfüllmusters des Shapes in der Zelle ShdwForegndTrans festlegen.</span><span class="sxs-lookup"><span data-stu-id="5d6d3-110">You can set the transparency of the foreground color of the shape's drop shadow fill pattern in the ShdwForegndTrans cell.</span></span>
  
<span data-ttu-id="5d6d3-111">Wenn Sie einen Verweis auf die Zelle ShdwForegnd aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="5d6d3-111">To get a reference to the ShdwForegnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5d6d3-112">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="5d6d3-112">Cell name:</span></span>  <br/> | <span data-ttu-id="5d6d3-113">ShdwForegnd</span><span class="sxs-lookup"><span data-stu-id="5d6d3-113">ShdwForegnd</span></span>  <br/> |
   
<span data-ttu-id="5d6d3-114">Wenn Sie einen Verweis auf die Zelle ShdwForegnd aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="5d6d3-114">To get a reference to the ShdwForegnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5d6d3-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="5d6d3-115">Section index:</span></span>  <br/> |<span data-ttu-id="5d6d3-116">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5d6d3-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5d6d3-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="5d6d3-117">Row index:</span></span>  <br/> |<span data-ttu-id="5d6d3-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="5d6d3-118">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="5d6d3-119">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="5d6d3-119">Cell index:</span></span>  <br/> |<span data-ttu-id="5d6d3-120">**visFillShdwForegnd**</span><span class="sxs-lookup"><span data-stu-id="5d6d3-120">**visFillShdwForegnd**</span></span> <br/> |
   

