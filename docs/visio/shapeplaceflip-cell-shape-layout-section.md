---
title: Zelle "ShapePlaceFlip" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253247
localization_priority: Normal
ms.assetid: 40008507-d9e4-9c0e-603f-d5e6da73a94b
description: Legt fest, wie ein platzierbares Shape auf dem Zeichenblatt gekippt und/oder gedreht wird, wenn Sie Shapes unter Verwendung des Dialogfelds Layout konfigurieren ausrichten. (Klicken Sie dazu auf der Registerkarte Entwurf in der Gruppe Layout auf Seite neu anordnen, und klicken Sie dann auf Weitere Layoutoptionen.)
ms.openlocfilehash: 76941b9c50e6f2c68ea9abf54e81dcd18be13a70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798025"
---
# <a name="shapeplaceflip-cell-shape-layout-section"></a><span data-ttu-id="27463-103">ShapePlaceFlip Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="27463-103">ShapePlaceFlip Cell (Shape Layout Section)</span></span>

<span data-ttu-id="27463-104">Legt fest, wie ein platzierbares Shape auf dem Zeichenblatt gekippt und/oder gedreht wird, wenn Sie Shapes unter Verwendung des Dialogfelds **Layout konfigurieren** ausrichten. (Klicken Sie dazu auf der Registerkarte **Entwurf** in der Gruppe **Layout** auf **Seite neu anordnen**, und klicken Sie dann auf **Weitere Layoutoptionen**.)</span><span class="sxs-lookup"><span data-stu-id="27463-104">Determines how a placeable shape flips, rotates, or both on the page when you are laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="27463-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="27463-105">**Value**</span></span>|<span data-ttu-id="27463-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="27463-106">**Description**</span></span>|<span data-ttu-id="27463-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="27463-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="27463-108">0</span><span class="sxs-lookup"><span data-stu-id="27463-108">0</span></span>  <br/> |<span data-ttu-id="27463-109">Zeichenblattstandard verwenden:</span><span class="sxs-lookup"><span data-stu-id="27463-109">Use page default.</span></span>  <br/> |<span data-ttu-id="27463-110">**visLOFlipDefault**</span><span class="sxs-lookup"><span data-stu-id="27463-110">**visLOFlipDefault**</span></span> <br/> |
|<span data-ttu-id="27463-111">1</span><span class="sxs-lookup"><span data-stu-id="27463-111">1</span></span>  <br/> |<span data-ttu-id="27463-112">Horizontal kippen.</span><span class="sxs-lookup"><span data-stu-id="27463-112">Flip horizontal.</span></span>  <br/> |<span data-ttu-id="27463-113">**visLOFlipX**</span><span class="sxs-lookup"><span data-stu-id="27463-113">**visLOFlipX**</span></span> <br/> |
|<span data-ttu-id="27463-114">2</span><span class="sxs-lookup"><span data-stu-id="27463-114">2</span></span>  <br/> |<span data-ttu-id="27463-115">Vertikal kippen.</span><span class="sxs-lookup"><span data-stu-id="27463-115">Flip vertical.</span></span>  <br/> |<span data-ttu-id="27463-116">**visLOFlipY**</span><span class="sxs-lookup"><span data-stu-id="27463-116">**visLOFlipY**</span></span> <br/> |
|<span data-ttu-id="27463-117">4</span><span class="sxs-lookup"><span data-stu-id="27463-117">4</span></span>  <br/> |<span data-ttu-id="27463-118">In 90-Grad-Schritten zwischen 0 und 270 kippen.</span><span class="sxs-lookup"><span data-stu-id="27463-118">Flip in 90 degree increments between 0 and 270.</span></span>  <br/> |<span data-ttu-id="27463-119">**visLOFlipRotate**</span><span class="sxs-lookup"><span data-stu-id="27463-119">**visLOFlipRotate**</span></span> <br/> |
|<span data-ttu-id="27463-120">8</span><span class="sxs-lookup"><span data-stu-id="27463-120">8</span></span>  <br/> |<span data-ttu-id="27463-121">Nicht kippen.</span><span class="sxs-lookup"><span data-stu-id="27463-121">Do not flip.</span></span>  <br/> |<span data-ttu-id="27463-122">**visLOFlipNone**</span><span class="sxs-lookup"><span data-stu-id="27463-122">**visLOFlipNone**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27463-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27463-123">Remarks</span></span>

<span data-ttu-id="27463-124">Der Wert in der Zelle ShapePlaceFlip hilft bei der Ausrichtung eines platzierbaren Shapes in Richtung des nächsten platzierbaren Shapes, mit dem es verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="27463-124">The value in the ShapePlaceFlip cell helps orient a placeable shape toward the next placeable shape it is connected to.</span></span>
  
<span data-ttu-id="27463-125">Wenn Sie dieses Verhalten für *sämtliche* Shapes auf dem Zeichenblatt festlegen möchten, verwenden Sie die Zelle PlaceFlip im Abschnitt Page Layout.</span><span class="sxs-lookup"><span data-stu-id="27463-125">To set this behavior for  *all*  the shapes on the drawing page, use the PlaceFlip cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="27463-126">Wenn Sie einen Verweis auf die Zelle ShapePlaceFlip aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="27463-126">To get a reference to the ShapePlaceFlip cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="27463-127">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="27463-127">Cell name:</span></span>  <br/> |<span data-ttu-id="27463-128">ShapePlaceFlip</span><span class="sxs-lookup"><span data-stu-id="27463-128">ShapePlaceFlip</span></span>  <br/> |
   
<span data-ttu-id="27463-129">Wenn Sie einen Verweis auf die Zelle ShapePlaceFlip aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="27463-129">To get a reference to the ShapePlaceFlip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="27463-130">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="27463-130">Section index:</span></span>  <br/> |<span data-ttu-id="27463-131">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="27463-131">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="27463-132">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="27463-132">Row index:</span></span>  <br/> |<span data-ttu-id="27463-133">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="27463-133">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="27463-134">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="27463-134">Cell index:</span></span>  <br/> |<span data-ttu-id="27463-135">**visSLOPlaceFlip**</span><span class="sxs-lookup"><span data-stu-id="27463-135">**visSLOPlaceFlip**</span></span> <br/> |
   

