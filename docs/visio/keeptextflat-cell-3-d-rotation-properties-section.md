---
title: Zelle "KeepTextFlat" (Abschnitt "3D Rotation Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: Gibt an, ob der Text eines Shapes die Drehung des Shapes in 3D ignoriert. Gilt nicht für 2D-Drehung.
ms.openlocfilehash: fc8cf2fac431645876c7f81ed9864cb6c2036169
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422040"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a><span data-ttu-id="4f67b-104">Zelle "KeepTextFlat" (Abschnitt "3D Rotation Properties")</span><span class="sxs-lookup"><span data-stu-id="4f67b-104">KeepTextFlat Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="4f67b-105">Gibt an, ob der Text eines Shapes die Drehung des Shapes in 3D ignoriert.</span><span class="sxs-lookup"><span data-stu-id="4f67b-105">Indicates whether a shape's text will ignore the shape's rotation in 3-D.</span></span> <span data-ttu-id="4f67b-106">Gilt nicht für 2D-Drehung.</span><span class="sxs-lookup"><span data-stu-id="4f67b-106">Does not apply to 2-D rotation.</span></span> 
  
****

|<span data-ttu-id="4f67b-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="4f67b-107">**Value**</span></span>|<span data-ttu-id="4f67b-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f67b-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4f67b-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="4f67b-109">TRUE</span></span>  <br/> |<span data-ttu-id="4f67b-110">Der Formtext wird nicht mit der Geometrie des Shapes gedreht.</span><span class="sxs-lookup"><span data-stu-id="4f67b-110">Shape text does not rotate with the shape's geometry.</span></span>  <br/> |
|<span data-ttu-id="4f67b-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="4f67b-111">FALSE</span></span>  <br/> |<span data-ttu-id="4f67b-112">Der Formtext wird so transformiert, dass er mit der Geometrie des Shapes gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="4f67b-112">Shape text is transformed to rotate with the shape's geometry.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f67b-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4f67b-113">Remarks</span></span>

<span data-ttu-id="4f67b-114">Verwenden Sie zum Erhalten eines Verweises auf die **Zelle KeepTextFlat** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="4f67b-114">To get a reference to the **KeepTextFlat** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4f67b-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="4f67b-115">Cell name:</span></span>  <br/> |<span data-ttu-id="4f67b-116">KeepTextFlat</span><span class="sxs-lookup"><span data-stu-id="4f67b-116">KeepTextFlat</span></span>  <br/> |
   
<span data-ttu-id="4f67b-117">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **KeepTextFlat-Zelle** nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="4f67b-117">To get a reference to the **KeepTextFlat** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4f67b-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="4f67b-118">Section index:</span></span>  <br/> |<span data-ttu-id="4f67b-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4f67b-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="4f67b-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="4f67b-120">Row index:</span></span>  <br/> |<span data-ttu-id="4f67b-121">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="4f67b-121">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="4f67b-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="4f67b-122">Cell index:</span></span>  <br/> |<span data-ttu-id="4f67b-123">**visKeepTextFlat**</span><span class="sxs-lookup"><span data-stu-id="4f67b-123">**visKeepTextFlat**</span></span> <br/> |
   

