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
ms.openlocfilehash: 607881e4a520f1376562394c6e40ab5d2508906d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342861"
---
# <a name="shapeshdwtype-cell-fill-format-section"></a><span data-ttu-id="8f900-103">Zelle "ShapeShdwType" (Abschnitt "Fill Format")</span><span class="sxs-lookup"><span data-stu-id="8f900-103">ShapeShdwType Cell (Fill Format Section)</span></span>

<span data-ttu-id="8f900-104">Gibt den Schattentyp für ein Shape an.</span><span class="sxs-lookup"><span data-stu-id="8f900-104">Specifies the type of shadow for a shape.</span></span> 
  
|<span data-ttu-id="8f900-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="8f900-105">**Value**</span></span>|<span data-ttu-id="8f900-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8f900-106">**Description**</span></span>|<span data-ttu-id="8f900-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="8f900-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8f900-108">0</span><span class="sxs-lookup"><span data-stu-id="8f900-108">0</span></span>  <br/> |<span data-ttu-id="8f900-109">Zeichenblattstandard verwenden (Standard)</span><span class="sxs-lookup"><span data-stu-id="8f900-109">Use page default (the default)</span></span>  <br/> |<span data-ttu-id="8f900-110">**visFSTPageDefault**</span><span class="sxs-lookup"><span data-stu-id="8f900-110">**visFSTPageDefault**</span></span> <br/> |
|<span data-ttu-id="8f900-111">1</span><span class="sxs-lookup"><span data-stu-id="8f900-111">1</span></span>  <br/> |<span data-ttu-id="8f900-112">Simple</span><span class="sxs-lookup"><span data-stu-id="8f900-112">Simple</span></span>  <br/> |<span data-ttu-id="8f900-113">**visFSTSimple**</span><span class="sxs-lookup"><span data-stu-id="8f900-113">**visFSTSimple**</span></span> <br/> |
|<span data-ttu-id="8f900-114">2</span><span class="sxs-lookup"><span data-stu-id="8f900-114">2</span></span>  <br/> |<span data-ttu-id="8f900-115">Oblique</span><span class="sxs-lookup"><span data-stu-id="8f900-115">Oblique</span></span>  <br/> |<span data-ttu-id="8f900-116">**visFSTOblique**</span><span class="sxs-lookup"><span data-stu-id="8f900-116">**visFSTOblique**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8f900-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8f900-117">Remarks</span></span>

<span data-ttu-id="8f900-118">Verwenden Sie diese Zelle, um einen anderen Shape-Schatten als den Seiten Standard anzuwenden (der Standard Schattentyp der Seite ist in der Zelle "ShdwType im Abschnitt Page Properties definiert).</span><span class="sxs-lookup"><span data-stu-id="8f900-118">Use this cell to apply a shape shadow that is different from the page default (the page default shadow type is defined in the ShdwType cell in the Page Properties Section).</span></span>
  
<span data-ttu-id="8f900-119">Einfache Schattentypen werden als Abstandsschatten auf der Benutzeroberfläche beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8f900-119">Simple shadow types are described as offset shadows in the user interface (UI).</span></span> <span data-ttu-id="8f900-120">Ein einfacher Schatten hat den Effekt, dass das Shape auf einer zum Shape parallelen Ebene einen Schatten zu werfen scheint.</span><span class="sxs-lookup"><span data-stu-id="8f900-120">A simple shadow gives the effect of the shape being shadowed onto a parallel plane located behind the shape.</span></span> <span data-ttu-id="8f900-121">Schräge Schatten werden als schräge Schatten auf der Benutzeroberfläche beschrieben und haben den Effekt, dass der Schatten auf einer zum Shape rechtwinkligen Ebene zu liegen scheint.</span><span class="sxs-lookup"><span data-stu-id="8f900-121">Oblique shadows are described as oblique shadows in the UI and give the effect of a shadow being cast onto a plane perpendicular to the shape.</span></span> 
  
<span data-ttu-id="8f900-122">Eine Liste vordefinierter einfacher und schräger Schatten finden Sie im Dialogfeld **Schatten** im Feld **Formatvorlage** (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** auf **Schatten**, und klicken Sie dann auf **Schattenoptionen**).</span><span class="sxs-lookup"><span data-stu-id="8f900-122">For a list of predefined simple and oblique shadow types, see the **Style** box in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="8f900-123">Wenn Sie einen Verweis auf die Zelle Zelle aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="8f900-123">To get a reference to the ShapeShdwType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8f900-124">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="8f900-124">Cell name:</span></span>  <br/> |<span data-ttu-id="8f900-125">Zelle</span><span class="sxs-lookup"><span data-stu-id="8f900-125">ShapeShdwType</span></span>  <br/> |
   
<span data-ttu-id="8f900-126">Wenn Sie einen Verweis auf die Zelle Zelle aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="8f900-126">To get a reference to the ShapeShdwType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8f900-127">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="8f900-127">Section index:</span></span>  <br/> |<span data-ttu-id="8f900-128">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8f900-128">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8f900-129">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="8f900-129">Row index:</span></span>  <br/> |<span data-ttu-id="8f900-130">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="8f900-130">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="8f900-131">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="8f900-131">Cell index:</span></span>  <br/> |<span data-ttu-id="8f900-132">**visFillShdwType**</span><span class="sxs-lookup"><span data-stu-id="8f900-132">**visFillShdwType**</span></span> <br/> |
   

