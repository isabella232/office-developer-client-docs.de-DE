---
title: Zelle "FillBkgndTrans" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253230
localization_priority: Normal
ms.assetid: 87065350-ba9a-aae8-47f6-f263f6700d08
description: Legt die Transparenzstufe fest, die für die Hintergrundfarbe (Füllbereich) des Füllmusters des Shapes verwendet wird.
ms.openlocfilehash: 64c5d09fb18f089769e025893b9fac8b1878fca1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423209"
---
# <a name="fillbkgndtrans-cell-fill-format-section"></a><span data-ttu-id="08f20-103">Zelle "FillBkgndTrans" (Abschnitt "Fill Format")</span><span class="sxs-lookup"><span data-stu-id="08f20-103">FillBkgndTrans Cell (Fill Format Section)</span></span>

<span data-ttu-id="08f20-104">Legt die Transparenzstufe fest, die für die Hintergrundfarbe (Füllbereich) des Füllmusters des Shapes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="08f20-104">Determines the transparency level for the background (fill) color of the shape's fill pattern.</span></span>
  
|<span data-ttu-id="08f20-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="08f20-105">**Value**</span></span>|<span data-ttu-id="08f20-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="08f20-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="08f20-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="08f20-107">0 - 100</span></span>  <br/> |<span data-ttu-id="08f20-p101">Stellt die Transparenz in Prozent dar. Der Standardwert ist 0% (vollständig undurchsichtig).</span><span class="sxs-lookup"><span data-stu-id="08f20-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08f20-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08f20-110">Remarks</span></span>

<span data-ttu-id="08f20-p102">Werte werden auf ein halbes Prozent gerundet. Ein Wert von 100% bezeichnet völlige Transparenz. Ein Shape, dem ein völlig transparenter Füllbereich zugewiesen wurde, verhält sich auf dem Zeichenblatt zwar genauso wie ein Shape ohne Füllbereichzuweisung, die Interaktion mit anderen Objekten auf dem Zeichenblatt verläuft aber genauso wie bei Festlegen der Transparenz auf 0%.</span><span class="sxs-lookup"><span data-stu-id="08f20-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a shape with a completely transparent fill appears the same as a shape with no fill on the drawing page, it will interact with other objects on the page in the same ways as if its transparency is 0%.</span></span>
  
<span data-ttu-id="08f20-p103">Sie können diesen Wert auch festlegen, indem Sie den Schieberegler im Dialogfeld **Füllbereich** verwenden (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Shape** auf **Füllbereich**, und klicken Sie dann auf **Füllbereichsoptionen**). Dieser Wert bestimmt sowohl den Wert der Fülltransparenz für den Hintergrund als auch den Wert für den Vordergrund. Wenn Sie diese Werte unabhängig voneinander festlegen möchten, müssen Sie sie im ShapeSheet-Fenster eingeben.</span><span class="sxs-lookup"><span data-stu-id="08f20-p103">You can also set this value using the slider control in the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill**, and then click **Fill Options**). This value controls the value of both the background and foreground fill transparencies. To set these values independently, you must enter them in the ShapeSheet window.</span></span>
  
<span data-ttu-id="08f20-117">Wenn Sie einen Verweis auf die Zelle Zelle FillBkgndTrans aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="08f20-117">To get a reference to the FillBkgndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="08f20-118">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="08f20-118">Cell name:</span></span>  <br/> |<span data-ttu-id="08f20-119">Zelle FillBkgndTrans</span><span class="sxs-lookup"><span data-stu-id="08f20-119">FillBkgndTrans</span></span>  <br/> |
   
<span data-ttu-id="08f20-120">Wenn Sie einen Verweis auf die Zelle Zelle FillBkgndTrans aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="08f20-120">To get a reference to the FillBkgndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="08f20-121">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="08f20-121">Section index:</span></span>  <br/> |<span data-ttu-id="08f20-122">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="08f20-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="08f20-123">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="08f20-123">Row index:</span></span>  <br/> |<span data-ttu-id="08f20-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="08f20-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="08f20-125">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="08f20-125">Cell index:</span></span>  <br/> |<span data-ttu-id="08f20-126">**visFillBkgndTrans**</span><span class="sxs-lookup"><span data-stu-id="08f20-126">**visFillBkgndTrans**</span></span> <br/> |
   

