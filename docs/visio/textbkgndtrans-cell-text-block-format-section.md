---
title: Zelle "TextBkgndTrans" (Abschnitt "Text Block Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253240
localization_priority: Normal
ms.assetid: b2f9d317-cc42-bec5-66f9-f988bcbdcc24
description: Legt die Transparenzstufe für die Hintergrundfarbe des Textblocks des Shapes fest.
ms.openlocfilehash: f4c4dc7700c553bd4c9bee337220e357c4c5538a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332324"
---
# <a name="textbkgndtrans-cell-text-block-format-section"></a><span data-ttu-id="a7f97-103">Zelle "TextBkgndTrans" (Abschnitt "Text Block Format")</span><span class="sxs-lookup"><span data-stu-id="a7f97-103">TextBkgndTrans Cell (Text Block Format Section)</span></span>

<span data-ttu-id="a7f97-104">Legt die Transparenzstufe für die Hintergrundfarbe des Textblocks des Shapes fest.</span><span class="sxs-lookup"><span data-stu-id="a7f97-104">Determines the transparency level for the background color of the shape's text block.</span></span>
  
|<span data-ttu-id="a7f97-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a7f97-105">**Value**</span></span>|<span data-ttu-id="a7f97-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a7f97-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a7f97-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="a7f97-107">0 - 100</span></span>  <br/> |<span data-ttu-id="a7f97-p101">Stellt die Transparenz in Prozent dar. Der Standardwert ist 0% (vollständig undurchsichtig).</span><span class="sxs-lookup"><span data-stu-id="a7f97-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7f97-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7f97-110">Remarks</span></span>

<span data-ttu-id="a7f97-p102">Die Werte werden auf ein halbes Prozent gerundet. Ein Wert von 100 % bezeichnet völlige Transparenz. Ein Shape, dem ein völlig transparenter Texthintergrund zugewiesen wurde, verhält sich auf dem Zeichenblatt zwar genauso wie ein Shape ohne Texthintergrund, die Interaktion mit anderen Objekten auf dem Zeichenblatt erfolgt aber genauso wie bei einer Transparenz von 0 %.</span><span class="sxs-lookup"><span data-stu-id="a7f97-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a shape that has a completely transparent text background appears the same on the drawing page as a shape that has no text background, it interacts with other objects on the page in the same way as if its transparency were 0%.</span></span>
  
<span data-ttu-id="a7f97-114">Sie können diesen Wert auch festlegen, indem Sie den Schieberegler auf der Registerkarte **Schriftart** des Dialogfelds **Text** verwenden (klicken Sie dazu auf der Registerkarte **Start** auf den Pfeil neben **Schriftart**).</span><span class="sxs-lookup"><span data-stu-id="a7f97-114">You can also set this value using the slider control on the **Font** tab of the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="a7f97-115">Wenn Sie einen Verweis auf die Zelle Zelle TextBkgndTrans aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a7f97-115">To get a reference to the TextBkgndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a7f97-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a7f97-116">Cell name:</span></span>  <br/> |<span data-ttu-id="a7f97-117">Zelle TextBkgndTrans</span><span class="sxs-lookup"><span data-stu-id="a7f97-117">TextBkgndTrans</span></span>  <br/> |
   
<span data-ttu-id="a7f97-118">Wenn Sie einen Verweis auf die Zelle Zelle TextBkgndTrans aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a7f97-118">To get a reference to the TextBkgndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a7f97-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a7f97-119">Section index:</span></span>  <br/> |<span data-ttu-id="a7f97-120">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a7f97-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a7f97-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a7f97-121">Row index:</span></span>  <br/> |<span data-ttu-id="a7f97-122">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="a7f97-122">**visRowText**</span></span> <br/> |
|<span data-ttu-id="a7f97-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a7f97-123">Cell index:</span></span>  <br/> |<span data-ttu-id="a7f97-124">**visTxtBlkBkgndTrans**</span><span class="sxs-lookup"><span data-stu-id="a7f97-124">**visTxtBlkBkgndTrans**</span></span> <br/> |
   

