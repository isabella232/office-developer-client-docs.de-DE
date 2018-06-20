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
ms.openlocfilehash: a32f5dbc935e85a49ab585073ca6a31215fd102a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797884"
---
# <a name="resizemode-cell-shape-transform-section"></a><span data-ttu-id="39236-103">ResizeMode Cell (Shape Transform Section)</span><span class="sxs-lookup"><span data-stu-id="39236-103">ResizeMode Cell (Shape Transform Section)</span></span>

<span data-ttu-id="39236-104">Zeigt die aktuelle Einstellung für das Größenänderungsverhalten in Bezug auf das Shape an.</span><span class="sxs-lookup"><span data-stu-id="39236-104">Shows the current resize behavior setting for the shape.</span></span>
  
|<span data-ttu-id="39236-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="39236-105">**Value**</span></span>|<span data-ttu-id="39236-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="39236-106">**Description**</span></span>|<span data-ttu-id="39236-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="39236-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="39236-108">0</span><span class="sxs-lookup"><span data-stu-id="39236-108">0</span></span>  <br/> |<span data-ttu-id="39236-109">Einstellung der Gruppe verwenden.</span><span class="sxs-lookup"><span data-stu-id="39236-109">Use group's setting.</span></span>  <br/> |<span data-ttu-id="39236-110">**visXFormResizeDontCare**</span><span class="sxs-lookup"><span data-stu-id="39236-110">**visXFormResizeDontCare**</span></span> <br/> |
|<span data-ttu-id="39236-111">1</span><span class="sxs-lookup"><span data-stu-id="39236-111">1</span></span>  <br/> |<span data-ttu-id="39236-112">Nur neu positionieren.</span><span class="sxs-lookup"><span data-stu-id="39236-112">Reposition only.</span></span>  <br/> |<span data-ttu-id="39236-113">**visXFormResizeSpread**</span><span class="sxs-lookup"><span data-stu-id="39236-113">**visXFormResizeSpread**</span></span> <br/> |
|<span data-ttu-id="39236-114">2</span><span class="sxs-lookup"><span data-stu-id="39236-114">2</span></span>  <br/> |<span data-ttu-id="39236-115">Mit Gruppe skalieren.</span><span class="sxs-lookup"><span data-stu-id="39236-115">Scale with group.</span></span>  <br/> |<span data-ttu-id="39236-116">**visXFormResizeScale**</span><span class="sxs-lookup"><span data-stu-id="39236-116">**visXFormResizeScale**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39236-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="39236-117">Remarks</span></span>

<span data-ttu-id="39236-118">Sie können diesen Wert auch auf der Registerkarte **Verhalten** im Dialogfeld **Verhalten** festlegen (klicken Sie auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md)in der Gruppe **Shape-Design** auf **Verhalten**).</span><span class="sxs-lookup"><span data-stu-id="39236-118">You can also set this value on the **Behavior** tab in the **Behavior** dialog box (on the [Developer](run-in-developer-mode-display-the-developer-tab.md)tab, in the **Shape Design** group, click **Behavior**).</span></span> <span data-ttu-id="39236-119">Wenn Sie einen Verweis auf die Zelle ResizeMode nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="39236-119">To get a reference to the ResizeMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="39236-120">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="39236-120">Cell name:</span></span>  <br/> |<span data-ttu-id="39236-121">ResizeMode</span><span class="sxs-lookup"><span data-stu-id="39236-121">ResizeMode</span></span>  <br/> |
   
<span data-ttu-id="39236-122">Wenn Sie einen Verweis auf die Zelle ResizeMode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="39236-122">To get a reference to the ResizeMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="39236-123">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="39236-123">Section index:</span></span>  <br/> |<span data-ttu-id="39236-124">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="39236-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="39236-125">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="39236-125">Row index:</span></span>  <br/> |<span data-ttu-id="39236-126">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="39236-126">**visRowXFormOut**</span></span> <br/> |
|<span data-ttu-id="39236-127">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="39236-127">Cell index:</span></span>  <br/> |<span data-ttu-id="39236-128">**visXFormResizeMode**</span><span class="sxs-lookup"><span data-stu-id="39236-128">**visXFormResizeMode**</span></span> <br/> |
   

