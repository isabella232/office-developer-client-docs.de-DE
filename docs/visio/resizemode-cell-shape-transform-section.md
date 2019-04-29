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
# <a name="resizemode-cell-shape-transform-section"></a><span data-ttu-id="ff08a-103">Zelle "ResizeMode" (Abschnitt "Shape Transform")</span><span class="sxs-lookup"><span data-stu-id="ff08a-103">ResizeMode Cell (Shape Transform Section)</span></span>

<span data-ttu-id="ff08a-104">Zeigt die aktuelle Einstellung für das Größenänderungsverhalten in Bezug auf das Shape an.</span><span class="sxs-lookup"><span data-stu-id="ff08a-104">Shows the current resize behavior setting for the shape.</span></span>
  
|<span data-ttu-id="ff08a-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ff08a-105">**Value**</span></span>|<span data-ttu-id="ff08a-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ff08a-106">**Description**</span></span>|<span data-ttu-id="ff08a-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="ff08a-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ff08a-108">0</span><span class="sxs-lookup"><span data-stu-id="ff08a-108">0</span></span>  <br/> |<span data-ttu-id="ff08a-109">Einstellung der Gruppe verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff08a-109">Use group's setting.</span></span>  <br/> |<span data-ttu-id="ff08a-110">**visXFormResizeDontCare**</span><span class="sxs-lookup"><span data-stu-id="ff08a-110">**visXFormResizeDontCare**</span></span> <br/> |
|<span data-ttu-id="ff08a-111">1</span><span class="sxs-lookup"><span data-stu-id="ff08a-111">1</span></span>  <br/> |<span data-ttu-id="ff08a-112">Nur neu positionieren.</span><span class="sxs-lookup"><span data-stu-id="ff08a-112">Reposition only.</span></span>  <br/> |<span data-ttu-id="ff08a-113">**visXFormResizeSpread**</span><span class="sxs-lookup"><span data-stu-id="ff08a-113">**visXFormResizeSpread**</span></span> <br/> |
|<span data-ttu-id="ff08a-114">2</span><span class="sxs-lookup"><span data-stu-id="ff08a-114">2</span></span>  <br/> |<span data-ttu-id="ff08a-115">Mit Gruppe skalieren.</span><span class="sxs-lookup"><span data-stu-id="ff08a-115">Scale with group.</span></span>  <br/> |<span data-ttu-id="ff08a-116">**visXFormResizeScale**</span><span class="sxs-lookup"><span data-stu-id="ff08a-116">**visXFormResizeScale**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff08a-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff08a-117">Remarks</span></span>

<span data-ttu-id="ff08a-118">Sie können diesen Wert auch im Dialogfeld **Verhalten** auf der Registerkarte **Verhalten** festlegen (Klicken Sie auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md)in der Gruppe **Shape-Design** auf **Verhalten**).</span><span class="sxs-lookup"><span data-stu-id="ff08a-118">You can also set this value on the **Behavior** tab in the **Behavior** dialog box (on the [Developer](run-in-developer-mode-display-the-developer-tab.md)tab, in the **Shape Design** group, click **Behavior**).</span></span> <span data-ttu-id="ff08a-119">Wenn Sie einen Verweis auf die Zelle Zelle ResizeMode aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ff08a-119">To get a reference to the ResizeMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff08a-120">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ff08a-120">Cell name:</span></span>  <br/> |<span data-ttu-id="ff08a-121">Zelle ResizeMode</span><span class="sxs-lookup"><span data-stu-id="ff08a-121">ResizeMode</span></span>  <br/> |
   
<span data-ttu-id="ff08a-122">Wenn Sie einen Verweis auf die Zelle Zelle ResizeMode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="ff08a-122">To get a reference to the ResizeMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff08a-123">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ff08a-123">Section index:</span></span>  <br/> |<span data-ttu-id="ff08a-124">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ff08a-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ff08a-125">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ff08a-125">Row index:</span></span>  <br/> |<span data-ttu-id="ff08a-126">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="ff08a-126">**visRowXFormOut**</span></span> <br/> |
|<span data-ttu-id="ff08a-127">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="ff08a-127">Cell index:</span></span>  <br/> |<span data-ttu-id="ff08a-128">**visXFormResizeMode**</span><span class="sxs-lookup"><span data-stu-id="ff08a-128">**visXFormResizeMode**</span></span> <br/> |
   

