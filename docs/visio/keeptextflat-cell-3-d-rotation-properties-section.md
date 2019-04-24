---
title: KeepTextFlat Cell (3-D Rotation Properties section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: Gibt an, ob der Text der Form die Drehung in 3D ignoriert. Gilt nicht für 2D-Rotation.
ms.openlocfilehash: fc8cf2fac431645876c7f81ed9864cb6c2036169
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360438"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a><span data-ttu-id="bffd8-104">KeepTextFlat Cell (3-D Rotation Properties section)</span><span class="sxs-lookup"><span data-stu-id="bffd8-104">KeepTextFlat Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="bffd8-105">Gibt an, ob der Text der Form die Drehung in 3D ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bffd8-105">Indicates whether a shape's text will ignore the shape's rotation in 3-D.</span></span> <span data-ttu-id="bffd8-106">Gilt nicht für 2D-Rotation.</span><span class="sxs-lookup"><span data-stu-id="bffd8-106">Does not apply to 2-D rotation.</span></span> 
  
****

|<span data-ttu-id="bffd8-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="bffd8-107">**Value**</span></span>|<span data-ttu-id="bffd8-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bffd8-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bffd8-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="bffd8-109">TRUE</span></span>  <br/> |<span data-ttu-id="bffd8-110">Der Shape-Text wird nicht mit der Geometrie des Shapes gedreht.</span><span class="sxs-lookup"><span data-stu-id="bffd8-110">Shape text does not rotate with the shape's geometry.</span></span>  <br/> |
|<span data-ttu-id="bffd8-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="bffd8-111">FALSE</span></span>  <br/> |<span data-ttu-id="bffd8-112">Der Shape-Text wird so transformiert, dass er mit der Geometrie des Shapes rotiert.</span><span class="sxs-lookup"><span data-stu-id="bffd8-112">Shape text is transformed to rotate with the shape's geometry.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bffd8-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bffd8-113">Remarks</span></span>

<span data-ttu-id="bffd8-114">Wenn Sie einen Verweis auf die Zelle **KeepTextFlat** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="bffd8-114">To get a reference to the **KeepTextFlat** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bffd8-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="bffd8-115">Cell name:</span></span>  <br/> |<span data-ttu-id="bffd8-116">KeepTextFlat</span><span class="sxs-lookup"><span data-stu-id="bffd8-116">KeepTextFlat</span></span>  <br/> |
   
<span data-ttu-id="bffd8-117">Wenn Sie einen Verweis auf die Zelle **KeepTextFlat** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="bffd8-117">To get a reference to the **KeepTextFlat** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bffd8-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="bffd8-118">Section index:</span></span>  <br/> |<span data-ttu-id="bffd8-119">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bffd8-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="bffd8-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="bffd8-120">Row index:</span></span>  <br/> |<span data-ttu-id="bffd8-121">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="bffd8-121">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="bffd8-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="bffd8-122">Cell index:</span></span>  <br/> |<span data-ttu-id="bffd8-123">**visKeepTextFlat**</span><span class="sxs-lookup"><span data-stu-id="bffd8-123">**visKeepTextFlat**</span></span> <br/> |
   

