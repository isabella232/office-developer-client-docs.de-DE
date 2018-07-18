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
ms.openlocfilehash: 2256a4c89812924af820c020c225f4b82b1d4856
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798264"
---
# <a name="textbkgnd-cell-text-block-format-section"></a><span data-ttu-id="bf881-103">TextBkgnd Cell (Text Block Format Section)</span><span class="sxs-lookup"><span data-stu-id="bf881-103">TextBkgnd Cell (Text Block Format Section)</span></span>

<span data-ttu-id="bf881-104">Legt die Farbe des Texthintergrunds für ein Shape fest.</span><span class="sxs-lookup"><span data-stu-id="bf881-104">Determines the text background color for a shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bf881-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf881-105">Remarks</span></span>

<span data-ttu-id="bf881-106">Die Zelle TextBkgnd kann einen beliebigen Wert von 0 bis 24 oder 255 haben.</span><span class="sxs-lookup"><span data-stu-id="bf881-106">The TextBkgnd cell can have any value from 0 through 24, or 255.</span></span> <span data-ttu-id="bf881-107">Die Werte 0 und 255 ( *VisTxtBlklOpaque*) Geben Sie einen transparenten Texthintergrund an.</span><span class="sxs-lookup"><span data-stu-id="bf881-107">The values 0 and 255 ( *visTxtBlklOpaque*) both indicate a transparent text background.</span></span> 
  
<span data-ttu-id="bf881-108">Um eine benutzerdefinierte Farbe eingeben möchten, verwenden Sie die Funktionen RGB oder HSL plus 1 – beispielsweise RGB (255,127,255) + 1.</span><span class="sxs-lookup"><span data-stu-id="bf881-108">To enter a custom color, use the RGB or HSL function plus one—for example, RGB(255,127,255)+1.</span></span> <span data-ttu-id="bf881-109">Der Wert einer benutzerdefinierten Farbe ist ihre RGB-Farbe und RGB ( *R, g, b*) + 1, statt eine Zahl in das ShapeSheet-Fenster angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bf881-109">The value of a custom color is its RGB color, and RGB( *r, g, b*)+1, rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="bf881-110">Bei Verwendung in numerischen Operationen haben benutzerdefinierte Farben Werte von 25 und höher.</span><span class="sxs-lookup"><span data-stu-id="bf881-110">When used in numeric operations, custom colors have values of 25 and above.</span></span> 
  
<span data-ttu-id="bf881-111">Die Transparenz der Texthintergrundfarbe können Sie in der Zelle TextBkgnd Trans festlegen.</span><span class="sxs-lookup"><span data-stu-id="bf881-111">You can set the transparency of the text background color in the TextBkgndTrans cell.</span></span>
  
<span data-ttu-id="bf881-112">Wenn Sie einen Verweis auf die Zelle TextBkgnd aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="bf881-112">To get a reference to the TextBkgnd cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bf881-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="bf881-113">Cell name:</span></span>  <br/> |<span data-ttu-id="bf881-114">TextBkgnd</span><span class="sxs-lookup"><span data-stu-id="bf881-114">TextBkgnd</span></span>  <br/> |
   
<span data-ttu-id="bf881-115">Wenn Sie einen Verweis auf die Zelle TextBkgnd aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="bf881-115">To get a reference to the TextBkgnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bf881-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="bf881-116">Section index:</span></span>  <br/> |<span data-ttu-id="bf881-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bf881-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="bf881-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="bf881-118">Row index:</span></span>  <br/> |<span data-ttu-id="bf881-119">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="bf881-119">**visRowText**</span></span> <br/> |
|<span data-ttu-id="bf881-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="bf881-120">Cell index:</span></span>  <br/> |<span data-ttu-id="bf881-121">**visTxtBlkBkgnd**</span><span class="sxs-lookup"><span data-stu-id="bf881-121">**visTxtBlkBkgnd**</span></span> <br/> |
   

