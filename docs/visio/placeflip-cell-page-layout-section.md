---
title: Zelle "PlaceFlip" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253251
localization_priority: Normal
ms.assetid: df014b98-cfd5-b6d3-4b8a-b0acb3b94412
description: Legt fest, wie platzierbare Shapes auf einem Zeichenblatt gekippt und/oder gedreht werden, wenn Sie das Dialogfeld Layout konfigurieren verwenden (klicken Sie dazu auf der Registerkarte Entwurf in der Gruppe Layout auf Seite neu anordnen, und klicken Sie dann auf Weitere Layoutoptionen).
ms.openlocfilehash: d1c31654782012b3536d35f3a12a923c2cc7a8f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434298"
---
# <a name="placeflip-cell-page-layout-section"></a><span data-ttu-id="88d90-103">Zelle "PlaceFlip" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="88d90-103">PlaceFlip Cell (Page Layout Section)</span></span>

<span data-ttu-id="88d90-104">Legt fest, wie platzierbare Shapes auf einem Zeichenblatt gekippt und/oder gedreht werden, wenn Sie das Dialogfeld **Layout konfigurieren** verwenden (klicken Sie dazu auf der Registerkarte **Entwurf** in der Gruppe **Layout** auf **Seite neu anordnen**, und klicken Sie dann auf **Weitere Layoutoptionen**).</span><span class="sxs-lookup"><span data-stu-id="88d90-104">Determines how placeable shapes flip and/or rotate on a page when you use the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="88d90-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="88d90-105">**Value**</span></span>|<span data-ttu-id="88d90-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="88d90-106">**Description**</span></span>|<span data-ttu-id="88d90-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="88d90-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="88d90-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="88d90-108">&amp;H0</span></span>  <br/> |<span data-ttu-id="88d90-109">Standardwert.</span><span class="sxs-lookup"><span data-stu-id="88d90-109">Default.</span></span> <span data-ttu-id="88d90-110">Nicht kippen.</span><span class="sxs-lookup"><span data-stu-id="88d90-110">Do not flip.</span></span>  <br/> |<span data-ttu-id="88d90-111">**visLOFlipDefault**</span><span class="sxs-lookup"><span data-stu-id="88d90-111">**visLOFlipDefault**</span></span> <br/> |
|<span data-ttu-id="88d90-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="88d90-112">&amp;H1</span></span>  <br/> |<span data-ttu-id="88d90-113">Horizontal kippen.</span><span class="sxs-lookup"><span data-stu-id="88d90-113">Flip horizontal.</span></span>  <br/> |<span data-ttu-id="88d90-114">**visLOFlipX**</span><span class="sxs-lookup"><span data-stu-id="88d90-114">**visLOFlipX**</span></span> <br/> |
|<span data-ttu-id="88d90-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="88d90-115">&amp;H2</span></span>  <br/> |<span data-ttu-id="88d90-116">Vertikal kippen.</span><span class="sxs-lookup"><span data-stu-id="88d90-116">Flip vertical.</span></span>  <br/> |<span data-ttu-id="88d90-117">**visLOFlipY**</span><span class="sxs-lookup"><span data-stu-id="88d90-117">**visLOFlipY**</span></span> <br/> |
|<span data-ttu-id="88d90-118">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="88d90-118">&amp;H4</span></span>  <br/> |<span data-ttu-id="88d90-119">In 90-Grad-Schritten kippen.</span><span class="sxs-lookup"><span data-stu-id="88d90-119">Flip in 90 degree increments.</span></span>  <br/> |<span data-ttu-id="88d90-120">**visLOFlipRotate**</span><span class="sxs-lookup"><span data-stu-id="88d90-120">**visLOFlipRotate**</span></span> <br/> |
|<span data-ttu-id="88d90-121">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="88d90-121">&amp;H8</span></span>  <br/> |<span data-ttu-id="88d90-122">Nicht kippen.</span><span class="sxs-lookup"><span data-stu-id="88d90-122">Do not flip.</span></span>  <br/> |<span data-ttu-id="88d90-123">**visLOFlipNone**</span><span class="sxs-lookup"><span data-stu-id="88d90-123">**visLOFlipNone**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="88d90-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88d90-124">Remarks</span></span>

<span data-ttu-id="88d90-p102">Der Wert in der Zelle PlaceFlip hilft bei der Ausrichtung eines platzierbaren Shapes in Richtung des nächsten platzierbaren Shapes, mit dem es verbunden ist. Dieser Wert wird normalerweise verwendet, wenn Sie Zeichnungen ausrichten, die statischen Kleber verwenden.</span><span class="sxs-lookup"><span data-stu-id="88d90-p102">The value in the PlaceFlip cell helps orient a placeable shape toward the next placeable shape it is connected to. It is typically used when laying out drawings that use static glue.</span></span>
  
<span data-ttu-id="88d90-127">Wenn Sie dieses Verhalten für ein bestimmtes Shape festlegen möchten, verwenden Sie die Zelle ShapePlaceFlip im Abschnitt Shape Layout.</span><span class="sxs-lookup"><span data-stu-id="88d90-127">To set this behavior for a particular shape, use the ShapePlaceFlip cell in the Shape Layout section.</span></span>
  
<span data-ttu-id="88d90-128">Wenn Sie einen Verweis auf die Zelle Zelle placeflip aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="88d90-128">To get a reference to the PlaceFlip cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="88d90-129">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="88d90-129">Cell name:</span></span>  <br/> |<span data-ttu-id="88d90-130">Zelle placeflip</span><span class="sxs-lookup"><span data-stu-id="88d90-130">PlaceFlip</span></span>  <br/> |
   
<span data-ttu-id="88d90-131">Wenn Sie einen Verweis auf die Zelle Zelle placeflip aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="88d90-131">To get a reference to the PlaceFlip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="88d90-132">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="88d90-132">Section index:</span></span>  <br/> |<span data-ttu-id="88d90-133">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="88d90-133">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="88d90-134">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="88d90-134">Row index:</span></span>  <br/> |<span data-ttu-id="88d90-135">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="88d90-135">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="88d90-136">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="88d90-136">Cell index:</span></span>  <br/> |<span data-ttu-id="88d90-137">**visPLOPlaceFlip**</span><span class="sxs-lookup"><span data-stu-id="88d90-137">**visPLOPlaceFlip**</span></span> <br/> |
   

