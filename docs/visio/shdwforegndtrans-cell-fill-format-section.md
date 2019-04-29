---
title: Zelle "ShdwForegndTrans" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253253
localization_priority: Normal
ms.assetid: c42d4d2e-f8f0-bc5b-6018-4bb4ffa81b64
description: Legt die Transparenzstufe für die Farbe fest, die für den Vordergrund (Pinselstrich) des Schattenfüllmusters des Shapes verwendet wird.
ms.openlocfilehash: 0ef3ce525edcce4ccd61f36649ead512545eef58
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435040"
---
# <a name="shdwforegndtrans-cell-fill-format-section"></a><span data-ttu-id="f6576-103">Zelle "ShdwForegndTrans" (Abschnitt "Fill Format")</span><span class="sxs-lookup"><span data-stu-id="f6576-103">ShdwForegndTrans Cell (Fill Format Section)</span></span>

<span data-ttu-id="f6576-104">Legt die Transparenzstufe für die Farbe fest, die für den Vordergrund (Pinselstrich) des Schattenfüllmusters des Shapes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f6576-104">Determines the transparency level for the color used for the foreground (stroke) of the shape's drop shadow fill pattern.</span></span>
  
|<span data-ttu-id="f6576-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="f6576-105">**Value**</span></span>|<span data-ttu-id="f6576-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f6576-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f6576-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="f6576-107">0 - 100</span></span>  <br/> |<span data-ttu-id="f6576-p101">Stellt die Transparenz in Prozent dar. Der Standardwert ist 0% (vollständig undurchsichtig).</span><span class="sxs-lookup"><span data-stu-id="f6576-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6576-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6576-110">Remarks</span></span>

<span data-ttu-id="f6576-111">Werte werden auf ein halbes Prozent gerundet.</span><span class="sxs-lookup"><span data-stu-id="f6576-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="f6576-112">Ein Wert von 100% bezeichnet völlige Transparenz.</span><span class="sxs-lookup"><span data-stu-id="f6576-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="f6576-113">Obwohl ein Schatten mit einer vollständig transparenten Füllung auf dem Zeichenblatt als Schatten angezeigt wird, der keine Füllung aufweist, interagiert er mit anderen Objekten auf der Seite auf die gleiche Weise wie bei der Transparenz von 0%.</span><span class="sxs-lookup"><span data-stu-id="f6576-113">Although a shadow that has a completely transparent fill appears the same on the drawing page as a shadow that has no fill, it interacts with other objects on the page in the same ways as if its transparency were 0%.</span></span>
  
<span data-ttu-id="f6576-p103">Sie können diesen Wert auch festlegen, indem Sie den Schieberegler im Dialogfeld **Schatten** verwenden (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** auf **Schatten**, und klicken Sie dann auf **Schattenoptionen**). Dieser Wert bestimmt den Wert der Schattentransparenz sowohl für den Hintergrund als auch für den Vordergrund. Wenn Sie diese Werte unabhängig voneinander festlegen möchten, müssen Sie sie im ShapeSheet-Fenster eingeben.</span><span class="sxs-lookup"><span data-stu-id="f6576-p103">You can also set this value by using the slider control in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**). This value controls the value of both the background and foreground shadow transparencies. To set these values independently, you must enter them in the ShapeSheet window.</span></span>
  
<span data-ttu-id="f6576-117">Wenn Sie einen Verweis auf die Zelle Zelle ShdwForegndTrans aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f6576-117">To get a reference to the ShdwForegndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f6576-118">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="f6576-118">Cell name:</span></span>  <br/> |<span data-ttu-id="f6576-119">Zelle ShdwForegndTrans</span><span class="sxs-lookup"><span data-stu-id="f6576-119">ShdwForegndTrans</span></span>  <br/> |
   
<span data-ttu-id="f6576-120">Wenn Sie einen Verweis auf die Zelle Zelle ShdwForegndTrans aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="f6576-120">To get a reference to the ShdwForegndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f6576-121">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="f6576-121">Section index:</span></span>  <br/> |<span data-ttu-id="f6576-122">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f6576-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f6576-123">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="f6576-123">Row index:</span></span>  <br/> |<span data-ttu-id="f6576-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="f6576-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="f6576-125">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="f6576-125">Cell index:</span></span>  <br/> |<span data-ttu-id="f6576-126">**visFillShdwForegndTrans**</span><span class="sxs-lookup"><span data-stu-id="f6576-126">**visFillShdwForegndTrans**</span></span> <br/> |
   

