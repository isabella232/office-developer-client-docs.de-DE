---
title: Zelle "RotationType" (Abschnitt "3D Rotation Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: Bestimmt, ob die Form einer parallelen Drehung, einer Perspektivdrehung oder einer schrägen Drehung als ganze Zahl von 0 bis 6 folgt.
ms.openlocfilehash: 676f8a15185242aacc1affb9f1bd200ff3df454d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422943"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a><span data-ttu-id="f7f4e-103">Zelle "RotationType" (Abschnitt "3D Rotation Properties")</span><span class="sxs-lookup"><span data-stu-id="f7f4e-103">RotationType Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="f7f4e-104">Bestimmt, ob die Form einer parallelen Drehung, einer Perspektivdrehung oder einer schrägen Drehung als ganze Zahl von 0 bis 6 folgt.</span><span class="sxs-lookup"><span data-stu-id="f7f4e-104">Determines whether the shape follows a parallel rotation, a perspective rotation, or an oblique rotation, as an integer from 0 to 6.</span></span> 
  
|<span data-ttu-id="f7f4e-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="f7f4e-105">**Value**</span></span>|<span data-ttu-id="f7f4e-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f7f4e-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f7f4e-107">0</span><span class="sxs-lookup"><span data-stu-id="f7f4e-107">0</span></span>  <br/> |<span data-ttu-id="f7f4e-108">Die Form hat keine Drehung.</span><span class="sxs-lookup"><span data-stu-id="f7f4e-108">The shape does not have any rotation.</span></span>  <br/> |
|<span data-ttu-id="f7f4e-109">1</span><span class="sxs-lookup"><span data-stu-id="f7f4e-109">1</span></span>  <br/> |<span data-ttu-id="f7f4e-110">Die Form hat eine parallele Drehung.</span><span class="sxs-lookup"><span data-stu-id="f7f4e-110">The shape has a parallel rotation.</span></span>  <br/> |
|<span data-ttu-id="f7f4e-111">2</span><span class="sxs-lookup"><span data-stu-id="f7f4e-111">2</span></span>  <br/> |<span data-ttu-id="f7f4e-112">Die Form hat eine Perspektivdrehung.</span><span class="sxs-lookup"><span data-stu-id="f7f4e-112">The shape has a perspective rotation.</span></span>  <br/> |
|<span data-ttu-id="f7f4e-113">3</span><span class="sxs-lookup"><span data-stu-id="f7f4e-113">3</span></span>  <br/> |<span data-ttu-id="f7f4e-114">Die Form hat eine schräge Drehung nach links oben.</span><span class="sxs-lookup"><span data-stu-id="f7f4e-114">The shape has a top left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="f7f4e-115">4 </span><span class="sxs-lookup"><span data-stu-id="f7f4e-115">4</span></span>  <br/> |<span data-ttu-id="f7f4e-116">Die Form hat eine oben rechts schräge Drehung.</span><span class="sxs-lookup"><span data-stu-id="f7f4e-116">The shape has a top right oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="f7f4e-117">5 </span><span class="sxs-lookup"><span data-stu-id="f7f4e-117">5</span></span>  <br/> |<span data-ttu-id="f7f4e-118">Die Form hat eine schräge Drehung nach links unten.</span><span class="sxs-lookup"><span data-stu-id="f7f4e-118">The shape has a bottom left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="f7f4e-119">6 </span><span class="sxs-lookup"><span data-stu-id="f7f4e-119">6</span></span>  <br/> |<span data-ttu-id="f7f4e-120">Die Form hat eine schräge Drehung nach rechts unten.</span><span class="sxs-lookup"><span data-stu-id="f7f4e-120">The shape has a bottom right oblique rotation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7f4e-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f7f4e-121">Remarks</span></span>

<span data-ttu-id="f7f4e-122">Verwenden Sie zum Erhalten eines Verweises auf die **Zelle RotationType** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="f7f4e-122">To get a reference to the **RotationType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f7f4e-123">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="f7f4e-123">Cell name:</span></span>  <br/> |<span data-ttu-id="f7f4e-124">RotationType</span><span class="sxs-lookup"><span data-stu-id="f7f4e-124">RotationType</span></span>  <br/> |
   
<span data-ttu-id="f7f4e-125">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **RotationType-Zelle** nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="f7f4e-125">To get a reference to the **RotationType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f7f4e-126">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="f7f4e-126">Section index:</span></span>  <br/> |<span data-ttu-id="f7f4e-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f7f4e-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f7f4e-128">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="f7f4e-128">Row index:</span></span>  <br/> |<span data-ttu-id="f7f4e-129">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="f7f4e-129">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="f7f4e-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="f7f4e-130">Cell index:</span></span>  <br/> |<span data-ttu-id="f7f4e-131">**visRotationType**</span><span class="sxs-lookup"><span data-stu-id="f7f4e-131">**visRotationType**</span></span> <br/> |
   

