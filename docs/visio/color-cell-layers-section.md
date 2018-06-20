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
ms.openlocfilehash: b6728d44c71f6403e772a6a7e730ba3c18d9eb48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796647"
---
# <a name="color-cell-layers-section"></a><span data-ttu-id="ba1e7-103">Zelle "Color" (Abschnitt "Layers")</span><span class="sxs-lookup"><span data-stu-id="ba1e7-103">Color Cell (Layers Section)</span></span>

<span data-ttu-id="ba1e7-104">Gibt die zur Darstellung des Layers verwendete Farbe an.</span><span class="sxs-lookup"><span data-stu-id="ba1e7-104">Specifies the color used to display the layer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ba1e7-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba1e7-105">Remarks</span></span>

<span data-ttu-id="ba1e7-106">Wenn Sie die Farbe festlegen möchten, geben Sie eine Zahl von 0 bis 23 ein.</span><span class="sxs-lookup"><span data-stu-id="ba1e7-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="ba1e7-107">Dieser Zellwert entspricht der Einstellung für **Layerfarbe** im Dialogfeld **Layereigenschaften** (in der Gruppe **Bearbeiten** auf der Registerkarte **Start** , klicken Sie auf **Ebenen** und klicken Sie dann auf **Layereigenschaften**).</span><span class="sxs-lookup"><span data-stu-id="ba1e7-107">This cell value corresponds to the **Layer color** setting in the **Layer Properties** dialog box (in the **Editing** group on the **Home** tab, click **Layers** and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="ba1e7-108">Um eine benutzerdefinierte Farbe eingeben möchten, verwenden Sie die RGB oder HSL-Funktion.</span><span class="sxs-lookup"><span data-stu-id="ba1e7-108">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="ba1e7-109">Der Wert einer benutzerdefinierten Farbe ist ihre RGB-Farbe und RGB ( *R, g, b*), anstatt eine Zahl in das ShapeSheet-Fenster angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ba1e7-109">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="ba1e7-110">Bei Verwendung in numerischen Operationen haben benutzerdefinierte Farben Werte von 24 und höher.</span><span class="sxs-lookup"><span data-stu-id="ba1e7-110">When used in numeric operations, custom colors have values of 24 and above.</span></span> <span data-ttu-id="ba1e7-111">Der Wert 255 gibt an, dass der Layer keine Farbe aufweist.</span><span class="sxs-lookup"><span data-stu-id="ba1e7-111">A value of 255 indicates that the layer has no color.</span></span> 
  
<span data-ttu-id="ba1e7-112">Die Transparenz der Layer-Farbe können Sie in der Zelle Transparenz festlegen.</span><span class="sxs-lookup"><span data-stu-id="ba1e7-112">You can set the transparency of the layer color in the Transparency cell.</span></span>
  
<span data-ttu-id="ba1e7-113">Wenn Sie einen Verweis auf die Zelle Color nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ba1e7-113">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ba1e7-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ba1e7-114">Cell name:</span></span>  <br/> |<span data-ttu-id="ba1e7-115">Layers.Color [ *i* ] wobei *i* = < 1 >, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="ba1e7-115">Layers.Color[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="ba1e7-116">Wenn Sie einen Verweis auf die Zelle Color aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="ba1e7-116">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ba1e7-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ba1e7-117">Section index:</span></span>  <br/> |<span data-ttu-id="ba1e7-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="ba1e7-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="ba1e7-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ba1e7-119">Row index:</span></span>  <br/> |<span data-ttu-id="ba1e7-120">**VisRowLayer** +  *i* wobei *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="ba1e7-120">**visRowLayer** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="ba1e7-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="ba1e7-121">Cell index:</span></span>  <br/> |<span data-ttu-id="ba1e7-122">**visLayerColor**</span><span class="sxs-lookup"><span data-stu-id="ba1e7-122">**visLayerColor**</span></span> <br/> |
   

