---
title: Zelle "LineColor" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm535
localization_priority: Normal
ms.assetid: d857b48b-9a3d-a1e1-5ad2-6816a492c8ab
description: Definiert die Linienfarbe eines Shapes.
ms.openlocfilehash: d0b4ebee6d96bc67c9ca45e8a6194cb91ed6c7f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359304"
---
# <a name="linecolor-cell-line-format-section"></a><span data-ttu-id="504b4-103">Zelle "LineColor" (Abschnitt "Line Format")</span><span class="sxs-lookup"><span data-stu-id="504b4-103">LineColor Cell (Line Format Section)</span></span>

<span data-ttu-id="504b4-104">Definiert die Linienfarbe eines Shapes.</span><span class="sxs-lookup"><span data-stu-id="504b4-104">Determines the line color of the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="504b4-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="504b4-105">Remarks</span></span>

<span data-ttu-id="504b4-106">Um die Linienfarbe festzulegen, geben Sie eine Zahl zwischen 0 und 23 ein, bei der es sich um einen Index in einer Auflistung von Linien Farben handelt.</span><span class="sxs-lookup"><span data-stu-id="504b4-106">To set the line color, enter a number from 0 to 23, which is an index into a collection of line colors.</span></span> <span data-ttu-id="504b4-107">Sie können die Linien Farbsammlung im Dialogfeld **Linie** anzeigen (Klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** auf **Linie**, zeigen Sie auf **Gewicht**, und klicken Sie dann auf **Weitere Linien**).</span><span class="sxs-lookup"><span data-stu-id="504b4-107">You can view the line color collection in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span> <span data-ttu-id="504b4-108">Sie können den Wert von Zelle LineColor auch im Dialogfeld **Leitung** festlegen.</span><span class="sxs-lookup"><span data-stu-id="504b4-108">You can also set the value of LineColor in the **Line** dialog box.</span></span> 
  
<span data-ttu-id="504b4-109">Verwenden Sie die RGB-oder die GSL-Funktion, um eine benutzerdefinierte Farbe einzugeben.</span><span class="sxs-lookup"><span data-stu-id="504b4-109">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="504b4-110">Der Wert einer benutzerdefinierten Farbe ist ihre RGB-Farbe, und RGB ( *r, g, b*) anstelle einer Zahl wird im ShapeSheet-Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="504b4-110">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="504b4-111">Bei numerischen Vorgängen haben benutzerdefinierte Farben Werte von 24 und höher.</span><span class="sxs-lookup"><span data-stu-id="504b4-111">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="504b4-112">Die Transparenz der Linienfarbe können Sie in der Zelle LineColorTrans festlegen.</span><span class="sxs-lookup"><span data-stu-id="504b4-112">You can set the transparency of the line color in the LineColorTrans cell.</span></span>
  
<span data-ttu-id="504b4-113">Wenn Sie einen Verweis auf die Zelle Zelle LineColor aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="504b4-113">To get a reference to the LineColor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="504b4-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="504b4-114">Cell name:</span></span>  <br/> |<span data-ttu-id="504b4-115">Zelle LineColor</span><span class="sxs-lookup"><span data-stu-id="504b4-115">LineColor</span></span>  <br/> |
   
<span data-ttu-id="504b4-116">Wenn Sie einen Verweis auf die Zelle Zelle LineColor aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="504b4-116">To get a reference to the LineColor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="504b4-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="504b4-117">Section index:</span></span>  <br/> |<span data-ttu-id="504b4-118">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="504b4-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="504b4-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="504b4-119">Row index:</span></span>  <br/> |<span data-ttu-id="504b4-120">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="504b4-120">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="504b4-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="504b4-121">Cell index:</span></span>  <br/> |<span data-ttu-id="504b4-122">**visLineColor**</span><span class="sxs-lookup"><span data-stu-id="504b4-122">**visLineColor**</span></span> <br/> |
   

