---
title: Zelle "CtrlAsInput" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1225
localization_priority: Normal
ms.assetid: c6fd0aba-7c33-b77f-207b-ba704b3e0756
description: Legt die übergeordneten Shapes bei Verwendung von Shapes mit Steuerpunkten fest. Mithilfe dieser Zelle wird das Verhalten aller Shapes auf dem Zeichenblatt festgelegt.
ms.openlocfilehash: a87ba7451d73af50de4a110ecdc12b3e23e14d5d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796764"
---
# <a name="ctrlasinput-cell-page-layout-section"></a><span data-ttu-id="8414f-104">Zelle "CtrlAsInput" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="8414f-104">CtrlAsInput Cell (Page Layout Section)</span></span>

<span data-ttu-id="8414f-p102">Legt die übergeordneten Shapes bei Verwendung von Shapes mit Steuerpunkten fest. Mithilfe dieser Zelle wird das Verhalten aller Shapes auf dem Zeichenblatt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8414f-p102">Determines which shape is the parent when using shapes with control handles. This cell sets the behavior for all the shapes on the drawing page.</span></span>
  
|<span data-ttu-id="8414f-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="8414f-107">**Value**</span></span>|<span data-ttu-id="8414f-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8414f-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="8414f-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="8414f-109">TRUE</span></span>  <br/> | <span data-ttu-id="8414f-110">Legt das mit dem Steuerpunkt verbundene Shape als das übergeordnete Element fest.</span><span class="sxs-lookup"><span data-stu-id="8414f-110">Set the shape that the control handle is connected to as the parent.</span></span>  <br/> |
| <span data-ttu-id="8414f-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="8414f-111">FALSE</span></span>  <br/> | <span data-ttu-id="8414f-p103">Standard. Legt das Shape, in dem der Steuerpunkt enthalten ist, als das übergeordnete Element fest.</span><span class="sxs-lookup"><span data-stu-id="8414f-p103">The default. Set shape that contains the control handle as the parent.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8414f-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8414f-114">Remarks</span></span>

<span data-ttu-id="8414f-115">Wenn Sie einen Verweis auf die Zelle CtrlAsInput nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="8414f-115">To get a reference to the CtrlAsInput cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8414f-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="8414f-116">Cell name:</span></span>  <br/> | <span data-ttu-id="8414f-117">CtrlAsInput</span><span class="sxs-lookup"><span data-stu-id="8414f-117">CtrlAsInput</span></span>  <br/> |
   
<span data-ttu-id="8414f-118">Wenn Sie einen Verweis auf die Zelle CtrlAsInput aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="8414f-118">To get a reference to the CtrlAsInput cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8414f-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="8414f-119">Section index:</span></span>  <br/> |<span data-ttu-id="8414f-120">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8414f-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8414f-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="8414f-121">Row index:</span></span>  <br/> |<span data-ttu-id="8414f-122">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="8414f-122">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="8414f-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="8414f-123">Cell index:</span></span>  <br/> |<span data-ttu-id="8414f-124">**visPLOCtrlAsInput**</span><span class="sxs-lookup"><span data-stu-id="8414f-124">**visPLOCtrlAsInput**</span></span> <br/> |
   

