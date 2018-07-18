---
title: RotationType Cell (3-D Rotation Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: Bestimmt, ob das Shape eine parallele Drehung, eine Perspektive Drehung oder eine oblique Rotation, als eine ganze Zahl zwischen 0 und 6 folgt.
ms.openlocfilehash: 85effcef3969d7b7c57551ec88710ba84b3fc163
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797909"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a><span data-ttu-id="7b87d-103">RotationType Cell (3-D Rotation Properties Section)</span><span class="sxs-lookup"><span data-stu-id="7b87d-103">RotationType Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="7b87d-104">Bestimmt, ob das Shape eine parallele Drehung, eine Perspektive Drehung oder eine oblique Rotation, als eine ganze Zahl zwischen 0 und 6 folgt.</span><span class="sxs-lookup"><span data-stu-id="7b87d-104">Determines whether the shape follows a parallel rotation, a perspective rotation, or an oblique rotation, as an integer from 0 to 6.</span></span> 
  
|<span data-ttu-id="7b87d-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="7b87d-105">**Value**</span></span>|<span data-ttu-id="7b87d-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7b87d-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7b87d-107">0</span><span class="sxs-lookup"><span data-stu-id="7b87d-107">0</span></span>  <br/> |<span data-ttu-id="7b87d-108">Das Shape hat keine Drehung.</span><span class="sxs-lookup"><span data-stu-id="7b87d-108">The shape does not have any rotation.</span></span>  <br/> |
|<span data-ttu-id="7b87d-109">1</span><span class="sxs-lookup"><span data-stu-id="7b87d-109">1</span></span>  <br/> |<span data-ttu-id="7b87d-110">Die Form ist eine parallele Drehung.</span><span class="sxs-lookup"><span data-stu-id="7b87d-110">The shape has a parallel rotation.</span></span>  <br/> |
|<span data-ttu-id="7b87d-111">2</span><span class="sxs-lookup"><span data-stu-id="7b87d-111">2</span></span>  <br/> |<span data-ttu-id="7b87d-112">Die Form ist eine Perspektive Drehung.</span><span class="sxs-lookup"><span data-stu-id="7b87d-112">The shape has a perspective rotation.</span></span>  <br/> |
|<span data-ttu-id="7b87d-113">3</span><span class="sxs-lookup"><span data-stu-id="7b87d-113">3</span></span>  <br/> |<span data-ttu-id="7b87d-114">Die Form ist eine obere linke oblique Drehung.</span><span class="sxs-lookup"><span data-stu-id="7b87d-114">The shape has a top left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="7b87d-115">4</span><span class="sxs-lookup"><span data-stu-id="7b87d-115">4</span></span>  <br/> |<span data-ttu-id="7b87d-116">Die Form ist eine rechts oblique Top Drehung.</span><span class="sxs-lookup"><span data-stu-id="7b87d-116">The shape has a top right oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="7b87d-117">5</span><span class="sxs-lookup"><span data-stu-id="7b87d-117">5</span></span>  <br/> |<span data-ttu-id="7b87d-118">Die Form ist eine unteren linken oblique Drehung.</span><span class="sxs-lookup"><span data-stu-id="7b87d-118">The shape has a bottom left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="7b87d-119">6</span><span class="sxs-lookup"><span data-stu-id="7b87d-119">6</span></span>  <br/> |<span data-ttu-id="7b87d-120">Die Form ist eine unten rechts oblique Drehung.</span><span class="sxs-lookup"><span data-stu-id="7b87d-120">The shape has a bottom right oblique rotation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b87d-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b87d-121">Remarks</span></span>

<span data-ttu-id="7b87d-122">Wenn Sie einen Verweis auf die Zelle **RotationType** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7b87d-122">To get a reference to the **RotationType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b87d-123">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="7b87d-123">Cell name:</span></span>  <br/> |<span data-ttu-id="7b87d-124">RotationType</span><span class="sxs-lookup"><span data-stu-id="7b87d-124">RotationType</span></span>  <br/> |
   
<span data-ttu-id="7b87d-125">Wenn Sie einen Verweis auf die Zelle **RotationType** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="7b87d-125">To get a reference to the **RotationType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b87d-126">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="7b87d-126">Section index:</span></span>  <br/> |<span data-ttu-id="7b87d-127">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7b87d-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="7b87d-128">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="7b87d-128">Row index:</span></span>  <br/> |<span data-ttu-id="7b87d-129">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="7b87d-129">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="7b87d-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="7b87d-130">Cell index:</span></span>  <br/> |<span data-ttu-id="7b87d-131">**visRotationType**</span><span class="sxs-lookup"><span data-stu-id="7b87d-131">**visRotationType**</span></span> <br/> |
   

