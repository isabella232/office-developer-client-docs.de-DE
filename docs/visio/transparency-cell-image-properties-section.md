---
title: Zelle "Transparency" (Abschnitt "Image Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51095
localization_priority: Normal
ms.assetid: 5b265356-1602-4241-fbe1-4d5a55392a52
description: Legt die Transparenzstufe für eine Layerfarbe fest.
ms.openlocfilehash: 5537cbdcd49c66f3bc28a58051f6e2888a290cd3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798299"
---
# <a name="transparency-cell-image-properties-section"></a><span data-ttu-id="bff18-103">Transparency Cell (Image Properties Section)</span><span class="sxs-lookup"><span data-stu-id="bff18-103">Transparency Cell (Image Properties Section)</span></span>

<span data-ttu-id="bff18-104">Legt die Transparenzstufe für eine Layerfarbe fest.</span><span class="sxs-lookup"><span data-stu-id="bff18-104">Determines the transparency level for a layer color.</span></span>
  
|<span data-ttu-id="bff18-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="bff18-105">**Value**</span></span>|<span data-ttu-id="bff18-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bff18-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bff18-107">
          0 - 100
</span><span class="sxs-lookup"><span data-stu-id="bff18-107">0 - 100</span></span>  <br/> |<span data-ttu-id="bff18-p101">Stellt die Transparenz in Prozent dar. Der Standardwert ist 0% (vollständig undurchsichtig).</span><span class="sxs-lookup"><span data-stu-id="bff18-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bff18-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bff18-110">Remarks</span></span>

<span data-ttu-id="bff18-p102">Die Werte werden auf ein halbes Prozent gerundet. Ein Wert von 100 % bezeichnet völlige Transparenz. Ein Layer mit einer völlig transparenten Farbe verhält sich auf dem Zeichenblatt zwar genauso wie ein Layer ohne Farbzuweisung, die Interaktion mit anderen Objekten auf dem Zeichenblatt erfolgt aber genauso wie bei einer Transparenz von 0 %. Sie können diesen Wert auch festlegen, indem Sie den Schieberegler im Dialogfeld **Layereigenschaften** verwenden (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Bearbeiten** auf **Layer**, und klicken Sie dann auf **Layereigenschaften**).</span><span class="sxs-lookup"><span data-stu-id="bff18-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a layer that has completely transparent color appears the same on the drawing page as a layer that has no color, it interacts with other objects on the page in the same way as if its transparency were 0%. You can also set this value by using the slider control in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="bff18-115">Wenn Sie einen Verweis auf die Zelle Transparency aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="bff18-115">To get a reference to the Transparency cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bff18-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="bff18-116">Cell name:</span></span>  <br/> |<span data-ttu-id="bff18-117">Transparency</span><span class="sxs-lookup"><span data-stu-id="bff18-117">Transparency</span></span>  <br/> |
   
<span data-ttu-id="bff18-118">Wenn Sie einen Verweis auf die Zelle Transparency aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="bff18-118">To get a reference to the Transparency cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bff18-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="bff18-119">Section index:</span></span>  <br/> |<span data-ttu-id="bff18-120">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bff18-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="bff18-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="bff18-121">Row index:</span></span>  <br/> |<span data-ttu-id="bff18-122">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="bff18-122">**visRowImage**</span></span> <br/> |
|<span data-ttu-id="bff18-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="bff18-123">Cell index:</span></span>  <br/> |<span data-ttu-id="bff18-124">**visImageTransparency**</span><span class="sxs-lookup"><span data-stu-id="bff18-124">**visImageTransparency**</span></span> <br/> |
   

