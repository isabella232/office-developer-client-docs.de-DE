---
title: Zelle "ResizeMode" (Abschnitt "Shape Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251203
localization_priority: Normal
ms.assetid: 49816e46-fa83-3ee4-1451-9c85fbd0f519
description: Zeigt die aktuelle Einstellung für das Größenänderungsverhalten in Bezug auf das Shape an.
ms.openlocfilehash: 7e9080fcd4604e2dbdc1dae31992f05e5b512213
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421963"
---
# <a name="resizemode-cell-shape-transform-section"></a><span data-ttu-id="24c1d-103">Zelle "ResizeMode" (Abschnitt "Shape Transform")</span><span class="sxs-lookup"><span data-stu-id="24c1d-103">ResizeMode Cell (Shape Transform Section)</span></span>

<span data-ttu-id="24c1d-104">Zeigt die aktuelle Einstellung für das Größenänderungsverhalten in Bezug auf das Shape an.</span><span class="sxs-lookup"><span data-stu-id="24c1d-104">Shows the current resize behavior setting for the shape.</span></span>
  
|<span data-ttu-id="24c1d-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="24c1d-105">**Value**</span></span>|<span data-ttu-id="24c1d-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="24c1d-106">**Description**</span></span>|<span data-ttu-id="24c1d-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="24c1d-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="24c1d-108">0</span><span class="sxs-lookup"><span data-stu-id="24c1d-108">0</span></span>  <br/> |<span data-ttu-id="24c1d-109">Einstellung der Gruppe verwenden.</span><span class="sxs-lookup"><span data-stu-id="24c1d-109">Use group's setting.</span></span>  <br/> |<span data-ttu-id="24c1d-110">**visXFormResizeDontCare**</span><span class="sxs-lookup"><span data-stu-id="24c1d-110">**visXFormResizeDontCare**</span></span> <br/> |
|<span data-ttu-id="24c1d-111">1</span><span class="sxs-lookup"><span data-stu-id="24c1d-111">1</span></span>  <br/> |<span data-ttu-id="24c1d-112">Nur neu positionieren.</span><span class="sxs-lookup"><span data-stu-id="24c1d-112">Reposition only.</span></span>  <br/> |<span data-ttu-id="24c1d-113">**visXFormResizeSpread**</span><span class="sxs-lookup"><span data-stu-id="24c1d-113">**visXFormResizeSpread**</span></span> <br/> |
|<span data-ttu-id="24c1d-114">2</span><span class="sxs-lookup"><span data-stu-id="24c1d-114">2</span></span>  <br/> |<span data-ttu-id="24c1d-115">Mit Gruppe skalieren.</span><span class="sxs-lookup"><span data-stu-id="24c1d-115">Scale with group.</span></span>  <br/> |<span data-ttu-id="24c1d-116">**visXFormResizeScale**</span><span class="sxs-lookup"><span data-stu-id="24c1d-116">**visXFormResizeScale**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24c1d-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="24c1d-117">Remarks</span></span>

<span data-ttu-id="24c1d-118">Sie können diesen Wert  auch auf der Registerkarte Verhalten [](run-in-developer-mode-display-the-developer-tab.md)im Dialogfeld Verhalten festlegen (klicken Sie auf der Registerkarte Entwickler in der **Gruppe Shape-Entwurf** auf  **Verhalten**).</span><span class="sxs-lookup"><span data-stu-id="24c1d-118">You can also set this value on the **Behavior** tab in the **Behavior** dialog box (on the [Developer](run-in-developer-mode-display-the-developer-tab.md)tab, in the **Shape Design** group, click **Behavior**).</span></span> <span data-ttu-id="24c1d-119">Um einen Verweis auf die Zelle ResizeMode anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="24c1d-119">To get a reference to the ResizeMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="24c1d-120">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="24c1d-120">Cell name:</span></span>  <br/> |<span data-ttu-id="24c1d-121">ResizeMode</span><span class="sxs-lookup"><span data-stu-id="24c1d-121">ResizeMode</span></span>  <br/> |
   
<span data-ttu-id="24c1d-122">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ResizeMode nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="24c1d-122">To get a reference to the ResizeMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="24c1d-123">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="24c1d-123">Section index:</span></span>  <br/> |<span data-ttu-id="24c1d-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="24c1d-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="24c1d-125">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="24c1d-125">Row index:</span></span>  <br/> |<span data-ttu-id="24c1d-126">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="24c1d-126">**visRowXFormOut**</span></span> <br/> |
|<span data-ttu-id="24c1d-127">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="24c1d-127">Cell index:</span></span>  <br/> |<span data-ttu-id="24c1d-128">**visXFormResizeMode**</span><span class="sxs-lookup"><span data-stu-id="24c1d-128">**visXFormResizeMode**</span></span> <br/> |
   

