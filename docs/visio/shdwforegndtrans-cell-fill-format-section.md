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
ms.openlocfilehash: 5fd385fc2f46f1ff8eedc961833813ec16ba7b73
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798071"
---
# <a name="shdwforegndtrans-cell-fill-format-section"></a><span data-ttu-id="c0f40-103">Zelle "ShdwForegndTrans" (Abschnitt "Fill Format")</span><span class="sxs-lookup"><span data-stu-id="c0f40-103">ShdwForegndTrans Cell (Fill Format Section)</span></span>

<span data-ttu-id="c0f40-104">Legt die Transparenzstufe für die Farbe fest, die für den Vordergrund (Pinselstrich) des Schattenfüllmusters des Shapes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c0f40-104">Determines the transparency level for the color used for the foreground (stroke) of the shape's drop shadow fill pattern.</span></span>
  
|<span data-ttu-id="c0f40-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="c0f40-105">**Value**</span></span>|<span data-ttu-id="c0f40-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c0f40-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c0f40-107">0 – 100</span><span class="sxs-lookup"><span data-stu-id="c0f40-107">0 - 100</span></span>  <br/> |<span data-ttu-id="c0f40-p101">Stellt die Transparenz in Prozent dar. Der Standardwert ist 0% (vollständig undurchsichtig).</span><span class="sxs-lookup"><span data-stu-id="c0f40-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0f40-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0f40-110">Remarks</span></span>

<span data-ttu-id="c0f40-111">Werte werden auf die nächste halbe % gerundet.</span><span class="sxs-lookup"><span data-stu-id="c0f40-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="c0f40-112">Es wird ein Wert von 100 % vollständig transparent.</span><span class="sxs-lookup"><span data-stu-id="c0f40-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="c0f40-113">Obwohl Sie ein Schatten, der eine vollständig transparente Füllung hat die gleiche auf dem Zeichenblatt als einen Schatten angezeigt wird, die keine Füllung aufweist, die Interaktion mit anderen Objekten auf der Seite auf die gleiche Weise als wäre die Transparenz 0 %.</span><span class="sxs-lookup"><span data-stu-id="c0f40-113">Although a shadow that has a completely transparent fill appears the same on the drawing page as a shadow that has no fill, it interacts with other objects on the page in the same ways as if its transparency were 0%.</span></span>
  
<span data-ttu-id="c0f40-114">Sie können diesen Wert auch festlegen, mit den Schieberegler im Dialogfeld **Schatten** (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** klicken Sie auf **Schatten**, und klicken Sie dann auf **Schattenoptionen**).</span><span class="sxs-lookup"><span data-stu-id="c0f40-114">You can also set this value by using the slider control in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span> <span data-ttu-id="c0f40-115">Dieser Wert steuert den Wert der sowohl die Hintergrund- und Vordergrundfarben Schatten Folien.</span><span class="sxs-lookup"><span data-stu-id="c0f40-115">This value controls the value of both the background and foreground shadow transparencies.</span></span> <span data-ttu-id="c0f40-116">Um diese Werte unabhängig voneinander festzulegen, müssen Sie diese im ShapeSheet-Fenster eingeben.</span><span class="sxs-lookup"><span data-stu-id="c0f40-116">To set these values independently, you must enter them in the ShapeSheet window.</span></span>
  
<span data-ttu-id="c0f40-117">Wenn Sie einen Verweis auf die Zelle ShdwForegndTrans nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c0f40-117">To get a reference to the ShdwForegndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c0f40-118">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="c0f40-118">Cell name:</span></span>  <br/> |<span data-ttu-id="c0f40-119">ShdwForegndTrans</span><span class="sxs-lookup"><span data-stu-id="c0f40-119">ShdwForegndTrans</span></span>  <br/> |
   
<span data-ttu-id="c0f40-120">Wenn Sie einen Verweis auf die Zelle ShdwForegndTrans aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="c0f40-120">To get a reference to the ShdwForegndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c0f40-121">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="c0f40-121">Section index:</span></span>  <br/> |<span data-ttu-id="c0f40-122">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c0f40-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c0f40-123">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="c0f40-123">Row index:</span></span>  <br/> |<span data-ttu-id="c0f40-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="c0f40-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="c0f40-125">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="c0f40-125">Cell index:</span></span>  <br/> |<span data-ttu-id="c0f40-126">**visFillShdwForegndTrans**</span><span class="sxs-lookup"><span data-stu-id="c0f40-126">**visFillShdwForegndTrans**</span></span> <br/> |
   

