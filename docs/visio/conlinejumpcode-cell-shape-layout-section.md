---
title: Zelle "ConLineJumpCode" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251652
localization_priority: Normal
ms.assetid: af85588e-8e83-5168-7a8c-d7e8b4af5c27
description: Bestimmt die Bedingungen für einen Verbindersprung.
ms.openlocfilehash: 28bf506b8d3729fefec438d259746661fd28586e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284088"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a><span data-ttu-id="9d1bf-103">Zelle "ConLineJumpCode" (Abschnitt "Shape Layout")</span><span class="sxs-lookup"><span data-stu-id="9d1bf-103">ConLineJumpCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="9d1bf-104">Bestimmt die Bedingungen für einen Verbindersprung.</span><span class="sxs-lookup"><span data-stu-id="9d1bf-104">Determines when a connector jumps.</span></span>
  
|<span data-ttu-id="9d1bf-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9d1bf-105">**Value**</span></span>|<span data-ttu-id="9d1bf-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9d1bf-106">**Description**</span></span>|<span data-ttu-id="9d1bf-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="9d1bf-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9d1bf-108">0</span><span class="sxs-lookup"><span data-stu-id="9d1bf-108">0</span></span>  <br/> |<span data-ttu-id="9d1bf-109">Klicken Sie gemäß den Angaben auf dem Zeichenblatt auf der Registerkarte **Entwurf** in der Gruppe **Seite einrichten** auf den Pfeil, und klicken Sie anschließend auf die Registerkarte **Layout und Routing**, um die Zeichenblattspezifikationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9d1bf-109">As page specifies; on the **Design** tab, click the arrow in the **Page Setup** group, and then click the **Layout and Routing** tab to see the page specifications</span></span>  <br/> |<span data-ttu-id="9d1bf-110">**visSLOJumpDefault**</span><span class="sxs-lookup"><span data-stu-id="9d1bf-110">**visSLOJumpDefault**</span></span> <br/> |
|<span data-ttu-id="9d1bf-111">1</span><span class="sxs-lookup"><span data-stu-id="9d1bf-111">1</span></span>  <br/> |<span data-ttu-id="9d1bf-112">Never</span><span class="sxs-lookup"><span data-stu-id="9d1bf-112">Never</span></span>  <br/> |<span data-ttu-id="9d1bf-113">**visSLOJumpNever**</span><span class="sxs-lookup"><span data-stu-id="9d1bf-113">**visSLOJumpNever**</span></span> <br/> |
|<span data-ttu-id="9d1bf-114">2</span><span class="sxs-lookup"><span data-stu-id="9d1bf-114">2</span></span>  <br/> |<span data-ttu-id="9d1bf-115">Always</span><span class="sxs-lookup"><span data-stu-id="9d1bf-115">Always</span></span>  <br/> |<span data-ttu-id="9d1bf-116">**visSLOJumpAlways**</span><span class="sxs-lookup"><span data-stu-id="9d1bf-116">**visSLOJumpAlways**</span></span> <br/> |
|<span data-ttu-id="9d1bf-117">3</span><span class="sxs-lookup"><span data-stu-id="9d1bf-117">3</span></span>  <br/> |<span data-ttu-id="9d1bf-118">Andere Verbindersprünge</span><span class="sxs-lookup"><span data-stu-id="9d1bf-118">Other connector jumps</span></span>  <br/> |<span data-ttu-id="9d1bf-119">**visSLOJumpOther**</span><span class="sxs-lookup"><span data-stu-id="9d1bf-119">**visSLOJumpOther**</span></span> <br/> |
|<span data-ttu-id="9d1bf-120">4</span><span class="sxs-lookup"><span data-stu-id="9d1bf-120">4</span></span>  <br/> |<span data-ttu-id="9d1bf-121">Keine Verbindersprünge</span><span class="sxs-lookup"><span data-stu-id="9d1bf-121">Neither connector jumps</span></span>  <br/> |<span data-ttu-id="9d1bf-122">**visSLOJumpNeither**</span><span class="sxs-lookup"><span data-stu-id="9d1bf-122">**visSLOJumpNeither**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d1bf-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d1bf-123">Remarks</span></span>

<span data-ttu-id="9d1bf-124">Sie können den Wert dieser Zelle auch festlegen, indem Sie einen dynamischen Verbinder auswählen, auf der Registerkarte [Entwickler](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **Shape-Design** auf **Verhalten** klicken und dann auf die Registerkarte **Verbinder** klicken.</span><span class="sxs-lookup"><span data-stu-id="9d1bf-124">You can also set the value of this cell by selecting a dynamic connector, clicking **Behavior** in the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then clicking the **Connector** tab.</span></span> 
  
<span data-ttu-id="9d1bf-125">Wenn Sie einen Verweis auf die Zelle Zelle ConLineJumpCode aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9d1bf-125">To get a reference to the ConLineJumpCode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9d1bf-126">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9d1bf-126">Cell name:</span></span>  <br/> |<span data-ttu-id="9d1bf-127">Zelle ConLineJumpCode</span><span class="sxs-lookup"><span data-stu-id="9d1bf-127">ConLineJumpCode</span></span>  <br/> |
   
<span data-ttu-id="9d1bf-128">Wenn Sie einen Verweis auf die Zelle Zelle ConLineJumpCode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="9d1bf-128">To get a reference to the ConLineJumpCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9d1bf-129">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9d1bf-129">Section index:</span></span>  <br/> |<span data-ttu-id="9d1bf-130">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9d1bf-130">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9d1bf-131">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9d1bf-131">Row index:</span></span>  <br/> |<span data-ttu-id="9d1bf-132">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="9d1bf-132">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="9d1bf-133">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9d1bf-133">Cell index:</span></span>  <br/> |<span data-ttu-id="9d1bf-134">**visSLOJumpCode**</span><span class="sxs-lookup"><span data-stu-id="9d1bf-134">**visSLOJumpCode**</span></span> <br/> |
   

