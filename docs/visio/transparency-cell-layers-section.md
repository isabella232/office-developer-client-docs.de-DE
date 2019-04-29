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
ms.openlocfilehash: fe0aacf167b2400ca10e22a70c9086429f6059f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436377"
---
# <a name="transparency-cell-layers-section"></a><span data-ttu-id="ff880-103">Zelle "Transparency" (Abschnitt "Layers")</span><span class="sxs-lookup"><span data-stu-id="ff880-103">Transparency Cell (Layers Section)</span></span>

<span data-ttu-id="ff880-104">Legt die Transparenzstufe für eine Layerfarbe fest.</span><span class="sxs-lookup"><span data-stu-id="ff880-104">Determines the transparency level for a layer color.</span></span>
  
|<span data-ttu-id="ff880-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ff880-105">**Value**</span></span>|<span data-ttu-id="ff880-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ff880-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ff880-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="ff880-107">0 - 100</span></span>  <br/> |<span data-ttu-id="ff880-p101">Stellt die Transparenz in Prozent dar. Der Standardwert ist 0% (vollständig undurchsichtig).</span><span class="sxs-lookup"><span data-stu-id="ff880-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff880-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff880-110">Remarks</span></span>

<span data-ttu-id="ff880-p102">Die Werte werden auf ein halbes Prozent gerundet. Ein Wert von 100 % bezeichnet völlige Transparenz. Ein Layer mit einer völlig transparenten Farbe verhält sich auf dem Zeichenblatt zwar genauso wie ein Layer ohne Farbzuweisung, die Interaktion mit anderen Objekten auf dem Zeichenblatt erfolgt aber genauso wie bei einer Transparenz von 0 %. Sie können diesen Wert auch festlegen, indem Sie den Schieberegler im Dialogfeld **Layereigenschaften** verwenden (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Bearbeiten** auf **Layer**, und klicken Sie dann auf **Layereigenschaften**).</span><span class="sxs-lookup"><span data-stu-id="ff880-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a layer that has completely transparent color appears the same on the drawing page as a layer that has no color, it interacts with other objects on the page in the same way as if its transparency were 0%. You can also set this value by using the slider control in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="ff880-115">Wenn Sie einen Verweis auf die Zelle Transparency aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ff880-115">To get a reference to the Transparency cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff880-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ff880-116">Cell name:</span></span>  <br/> |<span data-ttu-id="ff880-117">Layers. ColorTrans [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="ff880-117">Layers.ColorTrans[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="ff880-118">Wenn Sie einen Verweis auf die Zelle "Transparency" aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="ff880-118">To get a reference to the Transparency cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff880-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ff880-119">Section index:</span></span>  <br/> |<span data-ttu-id="ff880-120">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="ff880-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="ff880-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ff880-121">Row index:</span></span>  <br/> |<span data-ttu-id="ff880-122">**visRowLayer** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ff880-122">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="ff880-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="ff880-123">Cell index:</span></span>  <br/> |<span data-ttu-id="ff880-124">**visLayerColorTrans**</span><span class="sxs-lookup"><span data-stu-id="ff880-124">**visLayerColorTrans**</span></span> <br/> |
   

