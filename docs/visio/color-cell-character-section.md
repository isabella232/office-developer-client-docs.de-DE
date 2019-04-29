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
ms.openlocfilehash: a27d957781ca9a784e7ab9d5c1ce4f533b9a55ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439989"
---
# <a name="color-cell-character-section"></a><span data-ttu-id="c5df3-103">Zelle "Color" (Abschnitt "Character")</span><span class="sxs-lookup"><span data-stu-id="c5df3-103">Color Cell (Character Section)</span></span>

<span data-ttu-id="c5df3-104">Bestimmt die für den Text des Shapes verwendete Farbe.</span><span class="sxs-lookup"><span data-stu-id="c5df3-104">Determines the color used for the shape's text.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c5df3-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5df3-105">Remarks</span></span>

<span data-ttu-id="c5df3-106">Wenn Sie die Farbe festlegen möchten, geben Sie eine Zahl von 0 bis 23 ein.</span><span class="sxs-lookup"><span data-stu-id="c5df3-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="c5df3-107">Verwenden Sie die RGB-oder die GSL-Funktion, um eine benutzerdefinierte Farbe einzugeben.</span><span class="sxs-lookup"><span data-stu-id="c5df3-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="c5df3-108">Der Wert einer benutzerdefinierten Farbe ist ihre RGB-Farbe, und RGB ( *r, g, b*) anstelle einer Zahl wird im ShapeSheet-Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c5df3-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="c5df3-109">Bei numerischen Vorgängen haben benutzerdefinierte Farben Werte von 24 und höher.</span><span class="sxs-lookup"><span data-stu-id="c5df3-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="c5df3-110">Die Transparenz der Textfarbe können Sie in der Zelle Transparenz festlegen.</span><span class="sxs-lookup"><span data-stu-id="c5df3-110">You can set the transparency of the text color in the Transparency cell.</span></span>
  
<span data-ttu-id="c5df3-111">Wenn Sie einen Verweis auf die Zelle Farbe aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c5df3-111">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c5df3-112">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="c5df3-112">Cell name:</span></span>  <br/> |<span data-ttu-id="c5df3-113">Char. Color [ *i* ] wobei *i* = <1>, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="c5df3-113">Char.Color[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="c5df3-114">Wenn Sie einen Verweis auf die Zelle Color nach Index aus einem Programm erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="c5df3-114">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c5df3-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="c5df3-115">Section index:</span></span>  <br/> |<span data-ttu-id="c5df3-116">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="c5df3-116">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="c5df3-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="c5df3-117">Row index:</span></span>  <br/> |<span data-ttu-id="c5df3-118">**visRowCharacter** +  *i* , wobei *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="c5df3-118">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="c5df3-119">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="c5df3-119">Cell index:</span></span>  <br/> |<span data-ttu-id="c5df3-120">**visCharacterColor**</span><span class="sxs-lookup"><span data-stu-id="c5df3-120">**visCharacterColor**</span></span> <br/> |
   

