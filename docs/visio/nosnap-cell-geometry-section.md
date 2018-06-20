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
# <a name="nosnap-cell-geometry-section"></a><span data-ttu-id="c6cea-103">NoSnap Cell (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="c6cea-103">NoSnap Cell (Geometry Section)</span></span>

<span data-ttu-id="c6cea-104">Definiert, ob andere Shapes an einem Pfad einrasten.</span><span class="sxs-lookup"><span data-stu-id="c6cea-104">Determines whether other shapes snap to a path.</span></span>
  
|<span data-ttu-id="c6cea-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="c6cea-105">**Value**</span></span>|<span data-ttu-id="c6cea-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c6cea-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c6cea-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c6cea-107">TRUE</span></span>  <br/> | <span data-ttu-id="c6cea-108">Andere Shapes können nicht an diesem Pfad einrasten.</span><span class="sxs-lookup"><span data-stu-id="c6cea-108">Do not allow other shapes to snap to this path.</span></span>  <br/> |
| <span data-ttu-id="c6cea-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="c6cea-109">FALSE</span></span>  <br/> | <span data-ttu-id="c6cea-110">Andere Shapes können an diesem Pfad einrasten.</span><span class="sxs-lookup"><span data-stu-id="c6cea-110">Allow other shapes to snap to this path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6cea-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c6cea-111">Remarks</span></span>

<span data-ttu-id="c6cea-112">Wenn Sie einen Verweis auf die Zelle NoSnap nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c6cea-112">To get a reference to the NoSnap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c6cea-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="c6cea-113">Cell name:</span></span>  <br/> | <span data-ttu-id="c6cea-114">Geometrie *i* . NoSnap wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="c6cea-114">Geometry  *i*  .NoSnap            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c6cea-115">Wenn Sie einen Verweis auf die Zelle NoSnap aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="c6cea-115">To get a reference to the NoSnap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c6cea-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="c6cea-116">Section index:</span></span>  <br/> |<span data-ttu-id="c6cea-117">**VisSectionFirstComponent** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c6cea-117">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c6cea-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="c6cea-118">Row index:</span></span>  <br/> |<span data-ttu-id="c6cea-119">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="c6cea-119">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="c6cea-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="c6cea-120">Cell index:</span></span>  <br/> |<span data-ttu-id="c6cea-121">**visCompNoSnap**</span><span class="sxs-lookup"><span data-stu-id="c6cea-121">**visCompNoSnap**</span></span> <br/> |
   

