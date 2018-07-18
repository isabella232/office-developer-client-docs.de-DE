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
ms.openlocfilehash: 043571243fe3698561bee8632e7fd18db04c9330
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797543"
---
# <a name="nolivedynamics-cell-miscellaneous-section"></a><span data-ttu-id="184de-103">NoLiveDynamics Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="184de-103">NoLiveDynamics Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="184de-104">Bestimmt, ob ein Shape auf dynamische Art und Weise größenmäßig angepasst oder gedreht wird, während Sie es bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="184de-104">Determines whether a shape dynamically resizes or rotates as you are manipulating it.</span></span>
  
|<span data-ttu-id="184de-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="184de-105">**Value**</span></span>|<span data-ttu-id="184de-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="184de-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="184de-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="184de-107">TRUE</span></span>  <br/> | <span data-ttu-id="184de-108">Shape beim Bearbeiten nicht dynamisch aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="184de-108">Do not dynamically update the shape while you are manipulating it.</span></span>  <br/> |
| <span data-ttu-id="184de-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="184de-109">FALSE</span></span>  <br/> | <span data-ttu-id="184de-110">Shape beim Bearbeiten dynamisch aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="184de-110">Dynamically update the shape while you are manipulating it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="184de-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="184de-111">Remarks</span></span>

<span data-ttu-id="184de-p101">Während Sie ein zweidimensionales Shape (2D-Shape) bei deaktivierter Dynamik größenmäßig ändern oder drehen, wird ein Auswahlfeld angezeigt. Wenn das Shape eindimensional (1D-Shape) ist, hängt das visuelle Feedback vom Wert in der Zelle DynFeedback ab.</span><span class="sxs-lookup"><span data-stu-id="184de-p101">As you resize or rotate a two-dimensional (2-D) shape without live dynamics, you see a selection box. If the shape is one-dimensional (1-D), the visual feedback is based on the value of the DynFeedback cell.</span></span>
  
<span data-ttu-id="184de-114">Wenn Sie einen Verweis auf die Zelle NoLiveDynamics aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="184de-114">To get a reference to the NoLiveDynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="184de-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="184de-115">Cell name:</span></span>  <br/> | <span data-ttu-id="184de-116">NoLiveDynamics</span><span class="sxs-lookup"><span data-stu-id="184de-116">NoLiveDynamics</span></span>  <br/> |
   
<span data-ttu-id="184de-117">Wenn Sie einen Verweis auf die Zelle NoLiveDynamics aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="184de-117">To get a reference to the NoLiveDynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="184de-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="184de-118">Section index:</span></span>  <br/> |<span data-ttu-id="184de-119">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="184de-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="184de-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="184de-120">Row index:</span></span>  <br/> |<span data-ttu-id="184de-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="184de-121">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="184de-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="184de-122">Cell index:</span></span>  <br/> |<span data-ttu-id="184de-123">**visNoLiveDynamics**</span><span class="sxs-lookup"><span data-stu-id="184de-123">**visNoLiveDynamics**</span></span> <br/> |
   

