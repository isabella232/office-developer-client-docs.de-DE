---
title: Zelle "LineColorTrans" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50120
localization_priority: Normal
ms.assetid: b68054b5-7efd-1156-9dc1-5ec94e18d227
description: Definiert die Transparenzstufe der Linienfarbe eines Shapes.
ms.openlocfilehash: 555ea15de0279a37bcf67de7374d922b8692ce02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414438"
---
# <a name="linecolortrans-cell-line-format-section"></a><span data-ttu-id="caf48-103">Zelle "LineColorTrans" (Abschnitt "Line Format")</span><span class="sxs-lookup"><span data-stu-id="caf48-103">LineColorTrans Cell (Line Format Section)</span></span>

<span data-ttu-id="caf48-104">Definiert die Transparenzstufe der Linienfarbe eines Shapes.</span><span class="sxs-lookup"><span data-stu-id="caf48-104">Determines the transparency level of a shape's line color.</span></span>
  
|<span data-ttu-id="caf48-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="caf48-105">**Value**</span></span>|<span data-ttu-id="caf48-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="caf48-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="caf48-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="caf48-107">0 - 100</span></span>  <br/> |<span data-ttu-id="caf48-p101">Stellt die Transparenz in Prozent dar. Der Standardwert ist 0% (vollständig undurchsichtig).</span><span class="sxs-lookup"><span data-stu-id="caf48-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="caf48-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="caf48-110">Remarks</span></span>

<span data-ttu-id="caf48-p102">Werte werden auf ein halbes Prozent gerundet. Ein Wert von 100% bezeichnet völlige Transparenz. Ein Shape, dem eine völlig transparente Linienfarbe zugewiesen wurde, verhält sich auf dem Zeichenblatt zwar genauso wie ein Shape ohne Linien, die Interaktion mit anderen Objekten auf dem Zeichenblatt verläuft aber genauso wie bei Festlegen der Transparenz auf 0%.</span><span class="sxs-lookup"><span data-stu-id="caf48-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a shape with a completely transparent line color appears the same as a shape with no lines on the drawing page, it will interact with other objects on the page in the same ways as if its transparency is 0%.</span></span> 
  
<span data-ttu-id="caf48-114">Sie können diesen Wert auch festlegen, indem Sie das Schieberegler-Steuerelement im Dialogfeld **Linie** verwenden (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Shape** auf **Linie**, zeigen Sie auf **Linienbreite**, und klicken Sie dann auf **Weitere Linien**).</span><span class="sxs-lookup"><span data-stu-id="caf48-114">You can also set this value by using the slider control in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="caf48-115">Wenn Sie einen Verweis auf die Zelle Zelle linecolortrans aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="caf48-115">To get a reference to the LineColorTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="caf48-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="caf48-116">Cell name:</span></span>  <br/> |<span data-ttu-id="caf48-117">Zelle linecolortrans</span><span class="sxs-lookup"><span data-stu-id="caf48-117">LineColorTrans</span></span>  <br/> |
   
<span data-ttu-id="caf48-118">Wenn Sie einen Verweis auf die Zelle Zelle linecolortrans aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="caf48-118">To get a reference to the LineColorTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="caf48-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="caf48-119">Section index:</span></span>  <br/> |<span data-ttu-id="caf48-120">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="caf48-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="caf48-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="caf48-121">Row index:</span></span>  <br/> |<span data-ttu-id="caf48-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="caf48-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="caf48-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="caf48-123">Cell index:</span></span>  <br/> |<span data-ttu-id="caf48-124">**visLineColorTrans**</span><span class="sxs-lookup"><span data-stu-id="caf48-124">**visLineColorTrans**</span></span> <br/> |
   

