---
title: Zelle "FillForegndTrans" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253231
localization_priority: Normal
ms.assetid: 8b1b3904-6635-3fd1-31a9-ff32c19394af
description: Legt die Transparenzstufe fest, die für die Vordergrundfarbe (Füllbereich) des Füllmusters des Shapes verwendet wird.
ms.openlocfilehash: f9b09d67bc8d9ae851e86eaaa2ce1d36a92b2da2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797002"
---
# <a name="fillforegndtrans-cell-fill-format-section"></a><span data-ttu-id="e7242-103">FillForegndTrans Cell (Fill Format Section)</span><span class="sxs-lookup"><span data-stu-id="e7242-103">FillForegndTrans Cell (Fill Format Section)</span></span>

<span data-ttu-id="e7242-104">Legt die Transparenzstufe fest, die für die Vordergrundfarbe (Füllbereich) des Füllmusters des Shapes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e7242-104">Determines the transparency level for the foreground (fill) color of the shape's fill pattern.</span></span>
  
|<span data-ttu-id="e7242-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e7242-105">**Value**</span></span>|<span data-ttu-id="e7242-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e7242-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e7242-107">
          0 - 100
</span><span class="sxs-lookup"><span data-stu-id="e7242-107">0 - 100</span></span>  <br/> |<span data-ttu-id="e7242-p101">Stellt die Transparenz in Prozent dar. Der Standardwert ist 0% (vollständig undurchsichtig).</span><span class="sxs-lookup"><span data-stu-id="e7242-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7242-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7242-110">Remarks</span></span>

<span data-ttu-id="e7242-p102">Werte werden auf ein halbes Prozent gerundet. Ein Wert von 100% bezeichnet völlige Transparenz. Ein Shape, dem ein völlig transparenter Füllbereich zugewiesen wurde, verhält sich auf dem Zeichenblatt zwar genauso wie ein Shape ohne Füllbereichzuweisung, die Interaktion mit anderen Objekten auf dem Zeichenblatt verläuft aber genauso wie bei Festlegen der Transparenz auf 0%.</span><span class="sxs-lookup"><span data-stu-id="e7242-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a shape with a completely transparent fill appears the same as a shape with no fill on the drawing page, it will interact with other objects on the page in the same ways as if its transparency is 0%.</span></span>
  
<span data-ttu-id="e7242-p103">Sie können diesen Wert auch festlegen, indem Sie den Schieberegler im Dialogfeld **Füllbereich** verwenden (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Shape** auf **Füllbereich**, und klicken Sie dann auf **Füllbereichsoptionen**). Dieser Wert bestimmt sowohl den Wert der Fülltransparenz für den Hintergrund als auch den Wert für den Vordergrund. Wenn Sie diese Werte unabhängig voneinander festlegen möchten, müssen Sie sie im ShapeSheet-Fenster eingeben.</span><span class="sxs-lookup"><span data-stu-id="e7242-p103">You can also set this value using the slider control in the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill**, and then click **Fill Options**). This value controls the value of both the background and foreground fill transparencies. To set these values independently, you must enter them in the ShapeSheet window.</span></span>
  
<span data-ttu-id="e7242-117">Wenn Sie einen Verweis auf die Zelle FillForegndTrans aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e7242-117">To get a reference to the FillForegndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e7242-118">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="e7242-118">Cell name:</span></span>  <br/> |<span data-ttu-id="e7242-119">FillForegndTrans</span><span class="sxs-lookup"><span data-stu-id="e7242-119">FillForegndTrans</span></span>  <br/> |
   
<span data-ttu-id="e7242-120">Wenn Sie einen Verweis auf die Zelle FillForegndTrans aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="e7242-120">To get a reference to the FillForegndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e7242-121">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="e7242-121">Section index:</span></span>  <br/> |<span data-ttu-id="e7242-122">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e7242-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e7242-123">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="e7242-123">Row index:</span></span>  <br/> |<span data-ttu-id="e7242-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="e7242-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="e7242-125">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="e7242-125">Cell index:</span></span>  <br/> |<span data-ttu-id="e7242-126">**visFillForegndTrans**</span><span class="sxs-lookup"><span data-stu-id="e7242-126">**visFillForegndTrans**</span></span> <br/> |
   

