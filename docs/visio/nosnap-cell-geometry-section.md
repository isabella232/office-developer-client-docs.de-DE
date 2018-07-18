---
title: Zelle "NoSnap" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm740
localization_priority: Normal
ms.assetid: 0e6c8621-868c-9eac-926b-3049f18023b0
description: Definiert, ob andere Shapes an einem Pfad einrasten.
ms.openlocfilehash: 111f3773cb1df9033ed5a7b0b146d40ce6b26df0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797556"
---
# <a name="nosnap-cell-geometry-section"></a><span data-ttu-id="f2b1c-103">NoSnap Cell (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="f2b1c-103">NoSnap Cell (Geometry Section)</span></span>

<span data-ttu-id="f2b1c-104">Definiert, ob andere Shapes an einem Pfad einrasten.</span><span class="sxs-lookup"><span data-stu-id="f2b1c-104">Determines whether other shapes snap to a path.</span></span>
  
|<span data-ttu-id="f2b1c-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="f2b1c-105">**Value**</span></span>|<span data-ttu-id="f2b1c-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f2b1c-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f2b1c-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="f2b1c-107">TRUE</span></span>  <br/> | <span data-ttu-id="f2b1c-108">Andere Shapes können nicht an diesem Pfad einrasten.</span><span class="sxs-lookup"><span data-stu-id="f2b1c-108">Do not allow other shapes to snap to this path.</span></span>  <br/> |
| <span data-ttu-id="f2b1c-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="f2b1c-109">FALSE</span></span>  <br/> | <span data-ttu-id="f2b1c-110">Andere Shapes können an diesem Pfad einrasten.</span><span class="sxs-lookup"><span data-stu-id="f2b1c-110">Allow other shapes to snap to this path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2b1c-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f2b1c-111">Remarks</span></span>

<span data-ttu-id="f2b1c-112">Wenn Sie einen Verweis auf die Zelle NoSnap aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f2b1c-112">To get a reference to the NoSnap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f2b1c-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="f2b1c-113">Cell name:</span></span>  <br/> | <span data-ttu-id="f2b1c-114">Geometrie *i* . NoSnap wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="f2b1c-114">Geometry  *i*  .NoSnap            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="f2b1c-115">Wenn Sie einen Verweis auf die Zelle NoSnap aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="f2b1c-115">To get a reference to the NoSnap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f2b1c-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="f2b1c-116">Section index:</span></span>  <br/> |<span data-ttu-id="f2b1c-117">**VisSectionFirstComponent** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f2b1c-117">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f2b1c-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="f2b1c-118">Row index:</span></span>  <br/> |<span data-ttu-id="f2b1c-119">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="f2b1c-119">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="f2b1c-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="f2b1c-120">Cell index:</span></span>  <br/> |<span data-ttu-id="f2b1c-121">**visCompNoSnap**</span><span class="sxs-lookup"><span data-stu-id="f2b1c-121">**visCompNoSnap**</span></span> <br/> |
   

