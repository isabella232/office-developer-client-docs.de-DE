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
ms.openlocfilehash: 81c23b77c4663158819f9d5fe53765860183e039
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797325"
---
# <a name="linecolortrans-cell-line-format-section"></a><span data-ttu-id="24c40-103">Zelle "LineColorTrans" (Abschnitt "Line Format")</span><span class="sxs-lookup"><span data-stu-id="24c40-103">LineColorTrans Cell (Line Format Section)</span></span>

<span data-ttu-id="24c40-104">Definiert die Transparenzstufe der Linienfarbe eines Shapes.</span><span class="sxs-lookup"><span data-stu-id="24c40-104">Determines the transparency level of a shape's line color.</span></span>
  
|<span data-ttu-id="24c40-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="24c40-105">**Value**</span></span>|<span data-ttu-id="24c40-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="24c40-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="24c40-107">0 – 100</span><span class="sxs-lookup"><span data-stu-id="24c40-107">0 - 100</span></span>  <br/> |<span data-ttu-id="24c40-p101">Stellt die Transparenz in Prozent dar. Der Standardwert ist 0% (vollständig undurchsichtig).</span><span class="sxs-lookup"><span data-stu-id="24c40-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24c40-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24c40-110">Remarks</span></span>

<span data-ttu-id="24c40-p102">Werte werden auf ein halbes Prozent gerundet. Ein Wert von 100% bezeichnet völlige Transparenz. Ein Shape, dem eine völlig transparente Linienfarbe zugewiesen wurde, verhält sich auf dem Zeichenblatt zwar genauso wie ein Shape ohne Linien, die Interaktion mit anderen Objekten auf dem Zeichenblatt verläuft aber genauso wie bei Festlegen der Transparenz auf 0%.</span><span class="sxs-lookup"><span data-stu-id="24c40-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a shape with a completely transparent line color appears the same as a shape with no lines on the drawing page, it will interact with other objects on the page in the same ways as if its transparency is 0%.</span></span> 
  
<span data-ttu-id="24c40-114">Sie können diesen Wert auch mit den Schieberegler im Dialogfeld **Linie** festlegen (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** klicken Sie auf **Zeile**, **Weight**, und klicken Sie dann auf **Weitere Linien**).</span><span class="sxs-lookup"><span data-stu-id="24c40-114">You can also set this value by using the slider control in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="24c40-115">Wenn Sie einen Verweis auf die Zelle LineColorTrans nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="24c40-115">To get a reference to the LineColorTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="24c40-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="24c40-116">Cell name:</span></span>  <br/> |<span data-ttu-id="24c40-117">LineColorTrans</span><span class="sxs-lookup"><span data-stu-id="24c40-117">LineColorTrans</span></span>  <br/> |
   
<span data-ttu-id="24c40-118">Wenn Sie einen Verweis auf die Zelle LineColorTrans aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="24c40-118">To get a reference to the LineColorTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="24c40-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="24c40-119">Section index:</span></span>  <br/> |<span data-ttu-id="24c40-120">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="24c40-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="24c40-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="24c40-121">Row index:</span></span>  <br/> |<span data-ttu-id="24c40-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="24c40-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="24c40-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="24c40-123">Cell index:</span></span>  <br/> |<span data-ttu-id="24c40-124">**visLineColorTrans**</span><span class="sxs-lookup"><span data-stu-id="24c40-124">**visLineColorTrans**</span></span> <br/> |
   

