---
title: Zelle "Transparency" (Abschnitt "Layers")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50130
localization_priority: Normal
ms.assetid: 7382e2aa-5e18-19d2-88d8-c4a19a385106
description: Legt die Transparenzstufe für eine Layerfarbe fest.
ms.openlocfilehash: 7c205612436e7731f268e17c851616beebf809dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798305"
---
# <a name="transparency-cell-layers-section"></a><span data-ttu-id="8fe6e-103">Transparency Cell (Layers Section)</span><span class="sxs-lookup"><span data-stu-id="8fe6e-103">Transparency Cell (Layers Section)</span></span>

<span data-ttu-id="8fe6e-104">Legt die Transparenzstufe für eine Layerfarbe fest.</span><span class="sxs-lookup"><span data-stu-id="8fe6e-104">Determines the transparency level for a layer color.</span></span>
  
|<span data-ttu-id="8fe6e-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="8fe6e-105">**Value**</span></span>|<span data-ttu-id="8fe6e-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8fe6e-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8fe6e-107">0 – 100</span><span class="sxs-lookup"><span data-stu-id="8fe6e-107">0 - 100</span></span>  <br/> |<span data-ttu-id="8fe6e-p101">Stellt die Transparenz in Prozent dar. Der Standardwert ist 0% (vollständig undurchsichtig).</span><span class="sxs-lookup"><span data-stu-id="8fe6e-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8fe6e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8fe6e-110">Remarks</span></span>

<span data-ttu-id="8fe6e-111">Werte werden auf die nächste halbe % gerundet.</span><span class="sxs-lookup"><span data-stu-id="8fe6e-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="8fe6e-112">Es wird ein Wert von 100 % vollständig transparent.</span><span class="sxs-lookup"><span data-stu-id="8fe6e-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="8fe6e-113">Obwohl einem Layer, vollständig transparente Farbe ist, die gleiche auf dem Zeichenblatt als einer Ebene angezeigt, die keine Farbe aufweist wird, die Interaktion mit anderen Objekten auf der Seite auf die gleiche Weise als wäre die Transparenz 0 %.</span><span class="sxs-lookup"><span data-stu-id="8fe6e-113">Although a layer that has completely transparent color appears the same on the drawing page as a layer that has no color, it interacts with other objects on the page in the same way as if its transparency were 0%.</span></span> <span data-ttu-id="8fe6e-114">Sie können diesen Wert auch festlegen, mit den Schieberegler im Dialogfeld **Layereigenschaften** (klicken Sie auf der Registerkarte **Start** in der Gruppe **Bearbeiten** , klicken Sie auf **Ebenen**, und klicken Sie dann auf **Layereigenschaften**).</span><span class="sxs-lookup"><span data-stu-id="8fe6e-114">You can also set this value by using the slider control in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="8fe6e-115">Zum Abrufen eines Verweises auf die Zelle Transparency nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="8fe6e-115">To get a reference to the Transparency cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8fe6e-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="8fe6e-116">Cell name:</span></span>  <br/> |<span data-ttu-id="8fe6e-117">Layers.ColorTrans [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="8fe6e-117">Layers.ColorTrans[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="8fe6e-118">Wenn Sie einen Verweis auf die Zelle Transparency aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="8fe6e-118">To get a reference to the Transparency cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8fe6e-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="8fe6e-119">Section index:</span></span>  <br/> |<span data-ttu-id="8fe6e-120">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="8fe6e-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="8fe6e-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="8fe6e-121">Row index:</span></span>  <br/> |<span data-ttu-id="8fe6e-122">**VisRowLayer** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="8fe6e-122">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="8fe6e-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="8fe6e-123">Cell index:</span></span>  <br/> |<span data-ttu-id="8fe6e-124">**visLayerColorTrans**</span><span class="sxs-lookup"><span data-stu-id="8fe6e-124">**visLayerColorTrans**</span></span> <br/> |
   

