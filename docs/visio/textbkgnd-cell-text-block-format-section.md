---
title: Zelle "TextBkgnd" (Abschnitt "Text Block Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251267
localization_priority: Normal
ms.assetid: a238bf1c-1acd-eacd-22f3-a48acaaa4549
description: Legt die Farbe des Texthintergrunds für ein Shape fest.
ms.openlocfilehash: 2450bf0cb0e013c0f9310eacfca0f5a20e7e6063
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332328"
---
# <a name="textbkgnd-cell-text-block-format-section"></a><span data-ttu-id="92d1e-103">Zelle "TextBkgnd" (Abschnitt "Text Block Format")</span><span class="sxs-lookup"><span data-stu-id="92d1e-103">TextBkgnd Cell (Text Block Format Section)</span></span>

<span data-ttu-id="92d1e-104">Legt die Farbe des Texthintergrunds für ein Shape fest.</span><span class="sxs-lookup"><span data-stu-id="92d1e-104">Determines the text background color for a shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="92d1e-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92d1e-105">Remarks</span></span>

<span data-ttu-id="92d1e-106">Die Zelle TextBkgnd-Zelle kann einen beliebigen Wert von 0 bis 24 oder 255 haben.</span><span class="sxs-lookup"><span data-stu-id="92d1e-106">The TextBkgnd cell can have any value from 0 through 24, or 255.</span></span> <span data-ttu-id="92d1e-107">Die Werte 0 und 255 ( *visTxtBlklOpaque*) deuten auf einen transparenten Texthintergrund hin.</span><span class="sxs-lookup"><span data-stu-id="92d1e-107">The values 0 and 255 ( *visTxtBlklOpaque*) both indicate a transparent text background.</span></span> 
  
<span data-ttu-id="92d1e-108">Wenn Sie eine benutzerdefinierte Farbe eingeben möchten, verwenden Sie die RGB-oder die GSL-Funktion plus eine, beispielsweise RGB (255127255) + 1.</span><span class="sxs-lookup"><span data-stu-id="92d1e-108">To enter a custom color, use the RGB or HSL function plus one—for example, RGB(255,127,255)+1.</span></span> <span data-ttu-id="92d1e-109">Der Wert einer benutzerdefinierten Farbe ist die RGB-Farbe, und RGB ( *r, g, b*) + 1 anstelle einer Zahl wird im ShapeSheet-Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="92d1e-109">The value of a custom color is its RGB color, and RGB( *r, g, b*)+1, rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="92d1e-110">Bei numerischen Vorgängen haben benutzerdefinierte Farben Werte von 25 und höher.</span><span class="sxs-lookup"><span data-stu-id="92d1e-110">When used in numeric operations, custom colors have values of 25 and above.</span></span> 
  
<span data-ttu-id="92d1e-111">Die Transparenz der Texthintergrundfarbe können Sie in der Zelle TextBkgnd Trans festlegen.</span><span class="sxs-lookup"><span data-stu-id="92d1e-111">You can set the transparency of the text background color in the TextBkgndTrans cell.</span></span>
  
<span data-ttu-id="92d1e-112">Wenn Sie einen Verweis auf die Zelle Zelle TextBkgnd aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="92d1e-112">To get a reference to the TextBkgnd cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="92d1e-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="92d1e-113">Cell name:</span></span>  <br/> |<span data-ttu-id="92d1e-114">Zelle TextBkgnd</span><span class="sxs-lookup"><span data-stu-id="92d1e-114">TextBkgnd</span></span>  <br/> |
   
<span data-ttu-id="92d1e-115">Wenn Sie einen Verweis auf die Zelle Zelle TextBkgnd aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="92d1e-115">To get a reference to the TextBkgnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="92d1e-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="92d1e-116">Section index:</span></span>  <br/> |<span data-ttu-id="92d1e-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="92d1e-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="92d1e-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="92d1e-118">Row index:</span></span>  <br/> |<span data-ttu-id="92d1e-119">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="92d1e-119">**visRowText**</span></span> <br/> |
|<span data-ttu-id="92d1e-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="92d1e-120">Cell index:</span></span>  <br/> |<span data-ttu-id="92d1e-121">**visTxtBlkBkgnd**</span><span class="sxs-lookup"><span data-stu-id="92d1e-121">**visTxtBlkBkgnd**</span></span> <br/> |
   

