---
title: Zelle "NoLiveDynamics" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm720
localization_priority: Normal
ms.assetid: d1c4b9d9-6d64-8ed1-9fc6-2dbf829a75b5
description: Bestimmt, ob ein Shape auf dynamische Art und Weise größenmäßig angepasst oder gedreht wird, während Sie es bearbeiten.
ms.openlocfilehash: e332546c1fc5dfc71dfa3b72ea5a58bfef59dc7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421480"
---
# <a name="nolivedynamics-cell-miscellaneous-section"></a><span data-ttu-id="5a075-103">Zelle "NoLiveDynamics" (Abschnitt "Miscellaneous")</span><span class="sxs-lookup"><span data-stu-id="5a075-103">NoLiveDynamics Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="5a075-104">Bestimmt, ob ein Shape auf dynamische Art und Weise größenmäßig angepasst oder gedreht wird, während Sie es bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="5a075-104">Determines whether a shape dynamically resizes or rotates as you are manipulating it.</span></span>
  
|<span data-ttu-id="5a075-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="5a075-105">**Value**</span></span>|<span data-ttu-id="5a075-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5a075-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5a075-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="5a075-107">TRUE</span></span>  <br/> | <span data-ttu-id="5a075-108">Shape beim Bearbeiten nicht dynamisch aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5a075-108">Do not dynamically update the shape while you are manipulating it.</span></span>  <br/> |
| <span data-ttu-id="5a075-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="5a075-109">FALSE</span></span>  <br/> | <span data-ttu-id="5a075-110">Shape beim Bearbeiten dynamisch aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5a075-110">Dynamically update the shape while you are manipulating it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a075-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5a075-111">Remarks</span></span>

<span data-ttu-id="5a075-p101">Während Sie ein zweidimensionales Shape (2D-Shape) bei deaktivierter Dynamik größenmäßig ändern oder drehen, wird ein Auswahlfeld angezeigt. Wenn das Shape eindimensional (1D-Shape) ist, hängt das visuelle Feedback vom Wert in der Zelle DynFeedback ab.</span><span class="sxs-lookup"><span data-stu-id="5a075-p101">As you resize or rotate a two-dimensional (2-D) shape without live dynamics, you see a selection box. If the shape is one-dimensional (1-D), the visual feedback is based on the value of the DynFeedback cell.</span></span>
  
<span data-ttu-id="5a075-114">Um einen Verweis auf die Zelle NoLiveDynamics anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="5a075-114">To get a reference to the NoLiveDynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5a075-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="5a075-115">Cell name:</span></span>  <br/> | <span data-ttu-id="5a075-116">NoLiveDynamics</span><span class="sxs-lookup"><span data-stu-id="5a075-116">NoLiveDynamics</span></span>  <br/> |
   
<span data-ttu-id="5a075-117">Um einen Verweis auf die Zelle NoLiveDynamics nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="5a075-117">To get a reference to the NoLiveDynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5a075-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="5a075-118">Section index:</span></span>  <br/> |<span data-ttu-id="5a075-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5a075-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5a075-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="5a075-120">Row index:</span></span>  <br/> |<span data-ttu-id="5a075-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="5a075-121">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="5a075-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="5a075-122">Cell index:</span></span>  <br/> |<span data-ttu-id="5a075-123">**visNoLiveDynamics**</span><span class="sxs-lookup"><span data-stu-id="5a075-123">**visNoLiveDynamics**</span></span> <br/> |
   

