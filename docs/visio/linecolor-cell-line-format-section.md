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
ms.openlocfilehash: 6086a45108b88475e250c4d833ab4b740f33b8e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797328"
---
# <a name="linecolor-cell-line-format-section"></a><span data-ttu-id="94d57-103">Zelle "LineColor" (Abschnitt "Line Format")</span><span class="sxs-lookup"><span data-stu-id="94d57-103">LineColor Cell (Line Format Section)</span></span>

<span data-ttu-id="94d57-104">Definiert die Linienfarbe eines Shapes.</span><span class="sxs-lookup"><span data-stu-id="94d57-104">Determines the line color of the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="94d57-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94d57-105">Remarks</span></span>

<span data-ttu-id="94d57-106">Um die Linienfarbe festzulegen, geben Sie eine Zahl von 0 bis 23, also einen Index in einer Auflistung von Linienfarben.</span><span class="sxs-lookup"><span data-stu-id="94d57-106">To set the line color, enter a number from 0 to 23, which is an index into a collection of line colors.</span></span> <span data-ttu-id="94d57-107">Sie können die Auflistung der Zeile Farbe im Dialogfeld **Linie** anzeigen (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** klicken Sie auf **Zeile**, **Weight**, und klicken Sie dann auf **Weitere Linien**).</span><span class="sxs-lookup"><span data-stu-id="94d57-107">You can view the line color collection in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span> <span data-ttu-id="94d57-108">Sie können den Wert der LineColor auch im Dialogfeld **Linie** festlegen.</span><span class="sxs-lookup"><span data-stu-id="94d57-108">You can also set the value of LineColor in the **Line** dialog box.</span></span> 
  
<span data-ttu-id="94d57-109">Um eine benutzerdefinierte Farbe eingeben möchten, verwenden Sie die RGB oder HSL-Funktion.</span><span class="sxs-lookup"><span data-stu-id="94d57-109">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="94d57-110">Der Wert einer benutzerdefinierten Farbe ist ihre RGB-Farbe und RGB ( *R, g, b*), anstatt eine Zahl in das ShapeSheet-Fenster angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="94d57-110">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="94d57-111">Bei Verwendung in numerischen Operationen haben benutzerdefinierte Farben Werte von 24 und höher.</span><span class="sxs-lookup"><span data-stu-id="94d57-111">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="94d57-112">Die Transparenz der Linienfarbe können Sie in der Zelle LineColorTrans festlegen.</span><span class="sxs-lookup"><span data-stu-id="94d57-112">You can set the transparency of the line color in the LineColorTrans cell.</span></span>
  
<span data-ttu-id="94d57-113">Wenn Sie einen Verweis auf die Zelle LineColor nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="94d57-113">To get a reference to the LineColor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="94d57-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="94d57-114">Cell name:</span></span>  <br/> |<span data-ttu-id="94d57-115">LineColor</span><span class="sxs-lookup"><span data-stu-id="94d57-115">LineColor</span></span>  <br/> |
   
<span data-ttu-id="94d57-116">Wenn Sie einen Verweis auf die Zelle LineColor aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="94d57-116">To get a reference to the LineColor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="94d57-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="94d57-117">Section index:</span></span>  <br/> |<span data-ttu-id="94d57-118">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="94d57-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="94d57-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="94d57-119">Row index:</span></span>  <br/> |<span data-ttu-id="94d57-120">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="94d57-120">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="94d57-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="94d57-121">Cell index:</span></span>  <br/> |<span data-ttu-id="94d57-122">**visLineColor**</span><span class="sxs-lookup"><span data-stu-id="94d57-122">**visLineColor**</span></span> <br/> |
   

