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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280983"
---
# <a name="transparency-cell-character-section"></a><span data-ttu-id="d5b36-103">Zelle "Transparency" (Abschnitt "Character")</span><span class="sxs-lookup"><span data-stu-id="d5b36-103">Transparency Cell (Character Section)</span></span>

<span data-ttu-id="d5b36-104">Definiert die Transparenzstufe für einen Bereich der Textfarbe eines Shapes.</span><span class="sxs-lookup"><span data-stu-id="d5b36-104">Determines the transparency level for a range of a shape's text color.</span></span>
  
|<span data-ttu-id="d5b36-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d5b36-105">**Value**</span></span>|<span data-ttu-id="d5b36-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d5b36-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d5b36-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="d5b36-107">0 - 100</span></span>  <br/> |<span data-ttu-id="d5b36-p101">Stellt die Transparenz in Prozent dar. Der Standardwert ist 0% (vollständig undurchsichtig).</span><span class="sxs-lookup"><span data-stu-id="d5b36-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d5b36-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5b36-110">Remarks</span></span>

<span data-ttu-id="d5b36-p102">Die Werte werden auf ein halbes Prozent gerundet. Ein Wert von 100 % bezeichnet völlige Transparenz. Ein Shape, dem ein völlig transparenter Text zugewiesen wurde, verhält sich auf dem Zeichenblatt zwar genauso wie ein Shape ohne Text, die Interaktion mit anderen Objekten auf dem Zeichenblatt erfolgt aber genauso wie bei einer Transparenz von 0 %.</span><span class="sxs-lookup"><span data-stu-id="d5b36-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a shape that has completely transparent text appears the same on the drawing page as a shape that has no text, it interacts with other objects on the page in the same way as if its transparency were 0%.</span></span>
  
<span data-ttu-id="d5b36-114">Sie können diesen Wert auch festlegen, indem Sie das Schieberegler-Steuerelement auf der Registerkarte **Schriftart** im Dialogfeld **Text** verwenden (Klicken Sie auf der Registerkarte **Start** auf den Pfeil **Schriftart** ).</span><span class="sxs-lookup"><span data-stu-id="d5b36-114">You can also set this value by using the slider control on the **Font** tab in the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="d5b36-p103">Wenn der Abschnitt Character über mehrere Zeilen verfügt, enthält die Zelle Transparency Formatierungsinformationen für einen Unterbereich des Texts eines Shapes. Andernfalls enthält diese Zelle Formatierungsinformationen für den gesamten Text des Shapes.</span><span class="sxs-lookup"><span data-stu-id="d5b36-p103">If the Characters section contains multiple rows, the Transparency cell contains formatting information applied to a sub-range of a shape's text. Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="d5b36-117">Wenn Sie einen Verweis auf die Zelle Transparency aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d5b36-117">To get a reference to the Transparency cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d5b36-118">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="d5b36-118">Cell name:</span></span>  <br/> |<span data-ttu-id="d5b36-119">Char. ColorTrans [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d5b36-119">Char.ColorTrans[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d5b36-120">Wenn Sie einen Verweis auf die Zelle "Transparency" aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="d5b36-120">To get a reference to the Transparency cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d5b36-121">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="d5b36-121">Section index:</span></span>  <br/> |<span data-ttu-id="d5b36-122">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="d5b36-122">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="d5b36-123">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d5b36-123">Row index:</span></span>  <br/> |<span data-ttu-id="d5b36-124">**visRowCharacter** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d5b36-124">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="d5b36-125">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="d5b36-125">Cell index:</span></span>  <br/> |<span data-ttu-id="d5b36-126">**visCharacterColorTrans**</span><span class="sxs-lookup"><span data-stu-id="d5b36-126">**visCharacterColorTrans**</span></span> <br/> |
   

