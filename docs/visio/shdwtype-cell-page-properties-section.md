---
title: Zelle "ShdwType" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60084
localization_priority: Normal
ms.assetid: 551166d0-3aaa-0fd7-e742-cf3450ba90ed
description: Gibt den Standardschattentyp eines Zeichenblatts an.
ms.openlocfilehash: f1fc72484d94788ca2798760ca935c89c3e841ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424098"
---
# <a name="shdwtype-cell-page-properties-section"></a><span data-ttu-id="2853b-103">Zelle "ShdwType" (Abschnitt "Page Properties")</span><span class="sxs-lookup"><span data-stu-id="2853b-103">ShdwType Cell (Page Properties Section)</span></span>

<span data-ttu-id="2853b-104">Gibt den Standardschattentyp eines Zeichenblatts an.</span><span class="sxs-lookup"><span data-stu-id="2853b-104">Indicates the default shadow type for a page.</span></span>
  
|<span data-ttu-id="2853b-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2853b-105">**Value**</span></span>|<span data-ttu-id="2853b-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2853b-106">**Description**</span></span>|<span data-ttu-id="2853b-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="2853b-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="2853b-108">1</span><span class="sxs-lookup"><span data-stu-id="2853b-108">1</span></span>  <br/> | <span data-ttu-id="2853b-109">Simple</span><span class="sxs-lookup"><span data-stu-id="2853b-109">Simple</span></span>  <br/> |<span data-ttu-id="2853b-110">**visFSTSimple**</span><span class="sxs-lookup"><span data-stu-id="2853b-110">**visFSTSimple**</span></span> <br/> |
| <span data-ttu-id="2853b-111">2</span><span class="sxs-lookup"><span data-stu-id="2853b-111">2</span></span>  <br/> | <span data-ttu-id="2853b-112">Oblique</span><span class="sxs-lookup"><span data-stu-id="2853b-112">Oblique</span></span>  <br/> |<span data-ttu-id="2853b-113">**visFSTOblique**</span><span class="sxs-lookup"><span data-stu-id="2853b-113">**visFSTOblique**</span></span> <br/> |
|<span data-ttu-id="2853b-114">3</span><span class="sxs-lookup"><span data-stu-id="2853b-114">3</span></span>  <br/> |<span data-ttu-id="2853b-115">Inneren</span><span class="sxs-lookup"><span data-stu-id="2853b-115">Inner</span></span>  <br/> |<span data-ttu-id="2853b-116">**visFSTInner**</span><span class="sxs-lookup"><span data-stu-id="2853b-116">**visFSTInner**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2853b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2853b-117">Remarks</span></span>

 <span data-ttu-id="2853b-118">Der in dieser Zelle beschriebene Schattentyp wird verwendet, wenn die Zelle-Zelle (der Schattentyp für ein einzelnes Shape auf dem Zeichenblatt) auf Seiten Standard (**visFSTPageDefault** ) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2853b-118">The shadow type described in this cell is used whenever the ShapeShdwType Cell (the shadow type for an individual shape on the page) is set to Page Default (**visFSTPageDefault** ).</span></span> 
  
<span data-ttu-id="2853b-119">Einfache Schattentypen werden als Abstandsschatten auf der Benutzeroberfläche beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2853b-119">Simple shadow types are described as offset shadows in the user interface (UI).</span></span> <span data-ttu-id="2853b-120">Ein einfacher Schatten gibt an, wie sich die Form auf eine parallele Ebene befindet, die sich dahinter befindet.</span><span class="sxs-lookup"><span data-stu-id="2853b-120">A simple shadow gives the effect of the shape being shadowed onto a parallel plane located some distance behind it.</span></span> <span data-ttu-id="2853b-121">Schräge Schatten werden als schräge Schatten auf der Benutzeroberfläche beschrieben und haben den Effekt, dass der Schatten auf einer zum Shape rechtwinkligen Ebene zu liegen scheint.</span><span class="sxs-lookup"><span data-stu-id="2853b-121">Oblique shadows are described as oblique shadows in the UI and give the effect of a shadow being cast onto a plane perpendicular to the shape.</span></span> 
  
<span data-ttu-id="2853b-122">Eine Liste vordefinierter einfacher und schräger Schattentypen finden Sie im Dialogfeld **Seite einrichten** auf der Registerkarte **Schatten** in der Liste **Formatvorlage** (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**).</span><span class="sxs-lookup"><span data-stu-id="2853b-122">For a list of predefined simple and oblique shadow types, see the **Style** list on the **Shadows** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="2853b-123">Wenn Sie einen Verweis auf die Zelle "ShdwType aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2853b-123">To get a reference to the ShdwType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2853b-124">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2853b-124">Cell name:</span></span>  <br/> | <span data-ttu-id="2853b-125">"ShdwType</span><span class="sxs-lookup"><span data-stu-id="2853b-125">ShdwType</span></span>  <br/> |
   
<span data-ttu-id="2853b-126">Wenn Sie einen Verweis auf die Zelle Zelle ShapeShdwOffsetX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="2853b-126">To get a reference to the ShapeShdwOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2853b-127">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2853b-127">Section index:</span></span>  <br/> |<span data-ttu-id="2853b-128">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2853b-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2853b-129">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2853b-129">Row index:</span></span>  <br/> |<span data-ttu-id="2853b-130">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="2853b-130">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="2853b-131">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="2853b-131">Cell index:</span></span>  <br/> |<span data-ttu-id="2853b-132">**visPageShdwType**</span><span class="sxs-lookup"><span data-stu-id="2853b-132">**visPageShdwType**</span></span> <br/> |
   

