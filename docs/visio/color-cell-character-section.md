---
title: Zelle "Color" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm160
localization_priority: Normal
ms.assetid: 1c9aab2e-6c2f-0684-4e66-c35ac71883d6
description: Bestimmt die für den Text des Shapes verwendete Farbe.
ms.openlocfilehash: ef07f4165882e08a2292e4ee549f8807fe8403e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796630"
---
# <a name="color-cell-character-section"></a><span data-ttu-id="ad637-103">Color Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="ad637-103">Color Cell (Character Section)</span></span>

<span data-ttu-id="ad637-104">Bestimmt die für den Text des Shapes verwendete Farbe.</span><span class="sxs-lookup"><span data-stu-id="ad637-104">Determines the color used for the shape's text.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ad637-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad637-105">Remarks</span></span>

<span data-ttu-id="ad637-106">Wenn Sie die Farbe festlegen möchten, geben Sie eine Zahl von 0 bis 23 ein.</span><span class="sxs-lookup"><span data-stu-id="ad637-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="ad637-107">Um eine benutzerdefinierte Farbe eingeben möchten, verwenden Sie die RGB oder HSL-Funktion.</span><span class="sxs-lookup"><span data-stu-id="ad637-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="ad637-108">Der Wert einer benutzerdefinierten Farbe ist ihre RGB-Farbe und RGB ( *R, g, b*), anstatt eine Zahl in das ShapeSheet-Fenster angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ad637-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="ad637-109">Bei Verwendung in numerischen Operationen haben benutzerdefinierte Farben Werte von 24 und höher.</span><span class="sxs-lookup"><span data-stu-id="ad637-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="ad637-110">Die Transparenz der Textfarbe können Sie in der Zelle Transparenz festlegen.</span><span class="sxs-lookup"><span data-stu-id="ad637-110">You can set the transparency of the text color in the Transparency cell.</span></span>
  
<span data-ttu-id="ad637-111">Wenn Sie einen Verweis auf die Zelle Color aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ad637-111">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ad637-112">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ad637-112">Cell name:</span></span>  <br/> |<span data-ttu-id="ad637-113">Char.Color [ *i* ] wobei *i* = < 1 >, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="ad637-113">Char.Color[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="ad637-114">Wenn Sie einen Verweis auf die Zelle Color aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="ad637-114">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ad637-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ad637-115">Section index:</span></span>  <br/> |<span data-ttu-id="ad637-116">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="ad637-116">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="ad637-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ad637-117">Row index:</span></span>  <br/> |<span data-ttu-id="ad637-118">**VisRowCharacter** +  *i* wobei *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="ad637-118">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="ad637-119">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="ad637-119">Cell index:</span></span>  <br/> |<span data-ttu-id="ad637-120">**visCharacterColor**</span><span class="sxs-lookup"><span data-stu-id="ad637-120">**visCharacterColor**</span></span> <br/> |
   

