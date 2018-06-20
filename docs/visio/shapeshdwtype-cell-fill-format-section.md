---
title: Zelle "ShapeShdwType" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033173
localization_priority: Normal
ms.assetid: 1461148d-90a9-6f7c-1b28-9310ffaf0e3b
description: Gibt den Schattentyp für ein Shape an.
ms.openlocfilehash: b96ad4a877d72bf4457ec3cf038a29a2b414e0f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798041"
---
# <a name="shapeshdwtype-cell-fill-format-section"></a><span data-ttu-id="cc098-103">ShapeShdwType Cell (Fill Format Section)</span><span class="sxs-lookup"><span data-stu-id="cc098-103">ShapeShdwType Cell (Fill Format Section)</span></span>

<span data-ttu-id="cc098-104">Gibt den Schattentyp für ein Shape an.</span><span class="sxs-lookup"><span data-stu-id="cc098-104">Specifies the type of shadow for a shape.</span></span> 
  
|<span data-ttu-id="cc098-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="cc098-105">**Value**</span></span>|<span data-ttu-id="cc098-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cc098-106">**Description**</span></span>|<span data-ttu-id="cc098-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="cc098-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cc098-108">0</span><span class="sxs-lookup"><span data-stu-id="cc098-108">0</span></span>  <br/> |<span data-ttu-id="cc098-109">Zeichenblattstandard verwenden (Standard)</span><span class="sxs-lookup"><span data-stu-id="cc098-109">Use page default (the default)</span></span>  <br/> |<span data-ttu-id="cc098-110">**visFSTPageDefault**</span><span class="sxs-lookup"><span data-stu-id="cc098-110">**visFSTPageDefault**</span></span> <br/> |
|<span data-ttu-id="cc098-111">1</span><span class="sxs-lookup"><span data-stu-id="cc098-111">1</span></span>  <br/> |<span data-ttu-id="cc098-112">Einfach</span><span class="sxs-lookup"><span data-stu-id="cc098-112">Simple</span></span>  <br/> |<span data-ttu-id="cc098-113">**visFSTSimple**</span><span class="sxs-lookup"><span data-stu-id="cc098-113">**visFSTSimple**</span></span> <br/> |
|<span data-ttu-id="cc098-114">2</span><span class="sxs-lookup"><span data-stu-id="cc098-114">2</span></span>  <br/> |<span data-ttu-id="cc098-115">Schräg</span><span class="sxs-lookup"><span data-stu-id="cc098-115">Oblique</span></span>  <br/> |<span data-ttu-id="cc098-116">**visFSTOblique**</span><span class="sxs-lookup"><span data-stu-id="cc098-116">**visFSTOblique**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc098-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cc098-117">Remarks</span></span>

<span data-ttu-id="cc098-118">Verwenden Sie diese Zelle für einen Shape Schatten, der sich vom Zeichenblattstandard unterscheidet (der Schattentyp Seite wird in der Zelle ShdwType in den Abschnitt "Page Properties" definiert).</span><span class="sxs-lookup"><span data-stu-id="cc098-118">Use this cell to apply a shape shadow that is different from the page default (the page default shadow type is defined in the ShdwType cell in the Page Properties Section).</span></span>
  
<span data-ttu-id="cc098-119">Einfacher Schatten werden als Offset Schatten auf der Benutzeroberfläche (UI) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cc098-119">Simple shadow types are described as offset shadows in the user interface (UI).</span></span> <span data-ttu-id="cc098-120">Ein einfacher Schatten hat den Effekt der Form wird auf eine parallele Ebene hinter dem Shape schattiert.</span><span class="sxs-lookup"><span data-stu-id="cc098-120">A simple shadow gives the effect of the shape being shadowed onto a parallel plane located behind the shape.</span></span> <span data-ttu-id="cc098-121">Schräge Schatten werden als schräge Schatten auf der Benutzeroberfläche beschrieben, und weisen Sie die Auswirkung des einen Schatten auf eine senkrecht zum Shape.</span><span class="sxs-lookup"><span data-stu-id="cc098-121">Oblique shadows are described as oblique shadows in the UI and give the effect of a shadow being cast onto a plane perpendicular to the shape.</span></span> 
  
<span data-ttu-id="cc098-122">Eine Liste vordefinierter einfacher und schräger Schatten finden Sie unter Feld **Formatvorlage** im Dialogfeld **Schatten** (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** klicken Sie auf **Schatten**, und klicken Sie dann auf **Schattenoptionen**).</span><span class="sxs-lookup"><span data-stu-id="cc098-122">For a list of predefined simple and oblique shadow types, see the **Style** box in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="cc098-123">Wenn Sie einen Verweis auf die Zelle ShapeShdwType nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="cc098-123">To get a reference to the ShapeShdwType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cc098-124">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="cc098-124">Cell name:</span></span>  <br/> |<span data-ttu-id="cc098-125">ShapeShdwType</span><span class="sxs-lookup"><span data-stu-id="cc098-125">ShapeShdwType</span></span>  <br/> |
   
<span data-ttu-id="cc098-126">Wenn Sie einen Verweis auf die Zelle ShapeShdwType aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="cc098-126">To get a reference to the ShapeShdwType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cc098-127">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="cc098-127">Section index:</span></span>  <br/> |<span data-ttu-id="cc098-128">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cc098-128">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="cc098-129">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="cc098-129">Row index:</span></span>  <br/> |<span data-ttu-id="cc098-130">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="cc098-130">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="cc098-131">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="cc098-131">Cell index:</span></span>  <br/> |<span data-ttu-id="cc098-132">**visFillShdwType**</span><span class="sxs-lookup"><span data-stu-id="cc098-132">**visFillShdwType**</span></span> <br/> |
   

