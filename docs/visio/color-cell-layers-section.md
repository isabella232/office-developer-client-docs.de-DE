---
title: Zelle "Color" (Abschnitt "Layers")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm165
localization_priority: Normal
ms.assetid: 61c19342-46fb-48d4-6375-c9ea8306286d
description: Gibt die zur Darstellung des Layers verwendete Farbe an.
ms.openlocfilehash: a2eef24187165cabfdfc8dee49747a2381562d3e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341825"
---
# <a name="color-cell-layers-section"></a><span data-ttu-id="7aacb-103">Zelle "Color" (Abschnitt "Layers")</span><span class="sxs-lookup"><span data-stu-id="7aacb-103">Color Cell (Layers Section)</span></span>

<span data-ttu-id="7aacb-104">Gibt die zur Darstellung des Layers verwendete Farbe an.</span><span class="sxs-lookup"><span data-stu-id="7aacb-104">Specifies the color used to display the layer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7aacb-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7aacb-105">Remarks</span></span>

<span data-ttu-id="7aacb-106">Wenn Sie die Farbe festlegen möchten, geben Sie eine Zahl von 0 bis 23 ein.</span><span class="sxs-lookup"><span data-stu-id="7aacb-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="7aacb-107">Dieser Zellenwert entspricht der Einstellung **Layer-Farbe** im Dialog **Feld Layereigenschaften** (Klicken Sie auf der Registerkarte **Start** in der Gruppe **Bearbeiten** auf \*\*\*\* Layer, und klicken Sie dann auf **Layereigenschaften**).</span><span class="sxs-lookup"><span data-stu-id="7aacb-107">This cell value corresponds to the **Layer color** setting in the **Layer Properties** dialog box (in the **Editing** group on the **Home** tab, click **Layers** and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="7aacb-108">Verwenden Sie die RGB-oder die GSL-Funktion, um eine benutzerdefinierte Farbe einzugeben.</span><span class="sxs-lookup"><span data-stu-id="7aacb-108">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="7aacb-109">Der Wert einer benutzerdefinierten Farbe ist ihre RGB-Farbe, und RGB ( *r, g, b*) anstelle einer Zahl wird im ShapeSheet-Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7aacb-109">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="7aacb-110">Bei numerischen Vorgängen haben benutzerdefinierte Farben Werte von 24 und höher.</span><span class="sxs-lookup"><span data-stu-id="7aacb-110">When used in numeric operations, custom colors have values of 24 and above.</span></span> <span data-ttu-id="7aacb-111">Der Wert 255 gibt an, dass die Ebene keine Farbe aufweist.</span><span class="sxs-lookup"><span data-stu-id="7aacb-111">A value of 255 indicates that the layer has no color.</span></span> 
  
<span data-ttu-id="7aacb-112">Die Transparenz der Layer-Farbe können Sie in der Zelle Transparenz festlegen.</span><span class="sxs-lookup"><span data-stu-id="7aacb-112">You can set the transparency of the layer color in the Transparency cell.</span></span>
  
<span data-ttu-id="7aacb-113">Wenn Sie einen Verweis auf die Zelle Farbe aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7aacb-113">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7aacb-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="7aacb-114">Cell name:</span></span>  <br/> |<span data-ttu-id="7aacb-115">Layers. Color [ *i* ] wobei *i* = <1>, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="7aacb-115">Layers.Color[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="7aacb-116">Wenn Sie einen Verweis auf die Zelle Color nach Index aus einem Programm erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="7aacb-116">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7aacb-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="7aacb-117">Section index:</span></span>  <br/> |<span data-ttu-id="7aacb-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="7aacb-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="7aacb-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="7aacb-119">Row index:</span></span>  <br/> |<span data-ttu-id="7aacb-120">**visRowLayer** +  *i* , wobei *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="7aacb-120">**visRowLayer** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="7aacb-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="7aacb-121">Cell index:</span></span>  <br/> |<span data-ttu-id="7aacb-122">**visLayerColor**</span><span class="sxs-lookup"><span data-stu-id="7aacb-122">**visLayerColor**</span></span> <br/> |
   

