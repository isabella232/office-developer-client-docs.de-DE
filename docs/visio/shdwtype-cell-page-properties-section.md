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
ms.openlocfilehash: 1fc5c31a723d5d409110d94ff543a45dadabf264
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798090"
---
# <a name="shdwtype-cell-page-properties-section"></a><span data-ttu-id="bed6b-103">ShdwType Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="bed6b-103">ShdwType Cell (Page Properties Section)</span></span>

<span data-ttu-id="bed6b-104">Gibt den Standardschattentyp eines Zeichenblatts an.</span><span class="sxs-lookup"><span data-stu-id="bed6b-104">Indicates the default shadow type for a page.</span></span>
  
|<span data-ttu-id="bed6b-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="bed6b-105">**Value**</span></span>|<span data-ttu-id="bed6b-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bed6b-106">**Description**</span></span>|<span data-ttu-id="bed6b-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="bed6b-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="bed6b-108">1</span><span class="sxs-lookup"><span data-stu-id="bed6b-108">1</span></span>  <br/> | <span data-ttu-id="bed6b-109">Einfach</span><span class="sxs-lookup"><span data-stu-id="bed6b-109">Simple</span></span>  <br/> |<span data-ttu-id="bed6b-110">**visFSTSimple**</span><span class="sxs-lookup"><span data-stu-id="bed6b-110">**visFSTSimple**</span></span> <br/> |
| <span data-ttu-id="bed6b-111">2</span><span class="sxs-lookup"><span data-stu-id="bed6b-111">2</span></span>  <br/> | <span data-ttu-id="bed6b-112">Schräg</span><span class="sxs-lookup"><span data-stu-id="bed6b-112">Oblique</span></span>  <br/> |<span data-ttu-id="bed6b-113">**visFSTOblique**</span><span class="sxs-lookup"><span data-stu-id="bed6b-113">**visFSTOblique**</span></span> <br/> |
|<span data-ttu-id="bed6b-114">3</span><span class="sxs-lookup"><span data-stu-id="bed6b-114">3</span></span>  <br/> |<span data-ttu-id="bed6b-115">Innere</span><span class="sxs-lookup"><span data-stu-id="bed6b-115">Inner</span></span>  <br/> |<span data-ttu-id="bed6b-116">**visFSTInner**</span><span class="sxs-lookup"><span data-stu-id="bed6b-116">**visFSTInner**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bed6b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bed6b-117">Remarks</span></span>

 <span data-ttu-id="bed6b-118">In dieser Zelle beschriebene Schattentyp wird verwendet, wenn die Zelle ShapeShdwType (der Schattentyp für ein einzelnes Shape auf der Seite) auf Seitenstandard (**VisFSTPageDefault** ) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bed6b-118">The shadow type described in this cell is used whenever the ShapeShdwType Cell (the shadow type for an individual shape on the page) is set to Page Default (**visFSTPageDefault** ).</span></span> 
  
<span data-ttu-id="bed6b-119">Einfacher Schatten werden als Offset Schatten auf der Benutzeroberfläche (UI) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bed6b-119">Simple shadow types are described as offset shadows in the user interface (UI).</span></span> <span data-ttu-id="bed6b-120">Ein einfacher Schatten hat den Effekt der Form wird auf eine parallele Ebene hinter werfen schattiert.</span><span class="sxs-lookup"><span data-stu-id="bed6b-120">A simple shadow gives the effect of the shape being shadowed onto a parallel plane located some distance behind it.</span></span> <span data-ttu-id="bed6b-121">Schräge Schatten werden als schräge Schatten auf der Benutzeroberfläche beschrieben, und weisen Sie die Auswirkung des einen Schatten auf eine senkrecht zum Shape.</span><span class="sxs-lookup"><span data-stu-id="bed6b-121">Oblique shadows are described as oblique shadows in the UI and give the effect of a shadow being cast onto a plane perpendicular to the shape.</span></span> 
  
<span data-ttu-id="bed6b-122">Eine Liste vordefinierter einfacher und schräger Schattentypen finden Sie im Dialogfeld **Seite einrichten** auf der Registerkarte **Schatten** in der Liste **Formatvorlage** (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**).</span><span class="sxs-lookup"><span data-stu-id="bed6b-122">For a list of predefined simple and oblique shadow types, see the **Style** list on the **Shadows** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="bed6b-123">Wenn Sie einen Verweis auf die Zelle ShdwType aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="bed6b-123">To get a reference to the ShdwType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bed6b-124">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="bed6b-124">Cell name:</span></span>  <br/> | <span data-ttu-id="bed6b-125">ShdwType</span><span class="sxs-lookup"><span data-stu-id="bed6b-125">ShdwType</span></span>  <br/> |
   
<span data-ttu-id="bed6b-126">Wenn Sie einen Verweis auf die Zelle ShdwType aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="bed6b-126">To get a reference to the ShapeShdwOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bed6b-127">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="bed6b-127">Section index:</span></span>  <br/> |<span data-ttu-id="bed6b-128">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bed6b-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bed6b-129">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="bed6b-129">Row index:</span></span>  <br/> |<span data-ttu-id="bed6b-130">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="bed6b-130">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="bed6b-131">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="bed6b-131">Cell index:</span></span>  <br/> |<span data-ttu-id="bed6b-132">**visPageShdwType**</span><span class="sxs-lookup"><span data-stu-id="bed6b-132">**visPageShdwType**</span></span> <br/> |
   

