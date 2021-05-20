---
title: Zelle "Transparency" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50135
localization_priority: Normal
ms.assetid: ab835a1a-9e90-126e-279f-463882c48e93
description: Definiert die Transparenzstufe für einen Bereich der Textfarbe eines Shapes.
ms.openlocfilehash: 8619ec25372ae163fff1759aca36ff6693820e39
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427836"
---
# <a name="transparency-cell-character-section"></a><span data-ttu-id="db6de-103">Zelle "Transparency" (Abschnitt "Character")</span><span class="sxs-lookup"><span data-stu-id="db6de-103">Transparency Cell (Character Section)</span></span>

<span data-ttu-id="db6de-104">Definiert die Transparenzstufe für einen Bereich der Textfarbe eines Shapes.</span><span class="sxs-lookup"><span data-stu-id="db6de-104">Determines the transparency level for a range of a shape's text color.</span></span>
  
|<span data-ttu-id="db6de-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="db6de-105">**Value**</span></span>|<span data-ttu-id="db6de-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="db6de-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="db6de-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="db6de-107">0 - 100</span></span>  <br/> |<span data-ttu-id="db6de-p101">Stellt die Transparenz in Prozent dar. Der Standardwert ist 0% (vollständig undurchsichtig).</span><span class="sxs-lookup"><span data-stu-id="db6de-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db6de-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="db6de-110">Remarks</span></span>

<span data-ttu-id="db6de-p102">Die Werte werden auf ein halbes Prozent gerundet. Ein Wert von 100 % bezeichnet völlige Transparenz. Ein Shape, dem ein völlig transparenter Text zugewiesen wurde, verhält sich auf dem Zeichenblatt zwar genauso wie ein Shape ohne Text, die Interaktion mit anderen Objekten auf dem Zeichenblatt erfolgt aber genauso wie bei einer Transparenz von 0 %.</span><span class="sxs-lookup"><span data-stu-id="db6de-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a shape that has completely transparent text appears the same on the drawing page as a shape that has no text, it interacts with other objects on the page in the same way as if its transparency were 0%.</span></span>
  
<span data-ttu-id="db6de-114">Sie können diesen Wert auch festlegen, indem Sie das Schiebereglersteuerelement auf  der Registerkarte **Schriftart** im Dialogfeld **Text** verwenden (klicken Sie auf der Registerkarte Start auf den **Pfeil Schriftart).**</span><span class="sxs-lookup"><span data-stu-id="db6de-114">You can also set this value by using the slider control on the **Font** tab in the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="db6de-p103">Wenn der Abschnitt Character über mehrere Zeilen verfügt, enthält die Zelle Transparency Formatierungsinformationen für einen Unterbereich des Texts eines Shapes. Andernfalls enthält diese Zelle Formatierungsinformationen für den gesamten Text des Shapes.</span><span class="sxs-lookup"><span data-stu-id="db6de-p103">If the Characters section contains multiple rows, the Transparency cell contains formatting information applied to a sub-range of a shape's text. Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="db6de-117">Verwenden Sie zum Erhalten eines Verweises auf die Zelle Transparency anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="db6de-117">To get a reference to the Transparency cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="db6de-118">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="db6de-118">Cell name:</span></span>  <br/> |<span data-ttu-id="db6de-119">Char.ColorTrans[ *i*  ] wobei  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="db6de-119">Char.ColorTrans[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="db6de-120">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Transparency nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="db6de-120">To get a reference to the Transparency cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="db6de-121">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="db6de-121">Section index:</span></span>  <br/> |<span data-ttu-id="db6de-122">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="db6de-122">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="db6de-123">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="db6de-123">Row index:</span></span>  <br/> |<span data-ttu-id="db6de-124">**visRowCharacter**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="db6de-124">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="db6de-125">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="db6de-125">Cell index:</span></span>  <br/> |<span data-ttu-id="db6de-126">**visCharacterColorTrans**</span><span class="sxs-lookup"><span data-stu-id="db6de-126">**visCharacterColorTrans**</span></span> <br/> |
   

