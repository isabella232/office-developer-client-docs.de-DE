---
title: RotationType Cell (3-D Rotation Properties section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: Bestimmt, ob die Form einer parallelen Drehung, einer perspektivischen Drehung oder einer schrägen Drehung als ganze Zahl zwischen 0 und 6 folgt.
ms.openlocfilehash: 676f8a15185242aacc1affb9f1bd200ff3df454d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315673"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a><span data-ttu-id="42caf-103">RotationType Cell (3-D Rotation Properties section)</span><span class="sxs-lookup"><span data-stu-id="42caf-103">RotationType Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="42caf-104">Bestimmt, ob die Form einer parallelen Drehung, einer perspektivischen Drehung oder einer schrägen Drehung als ganze Zahl zwischen 0 und 6 folgt.</span><span class="sxs-lookup"><span data-stu-id="42caf-104">Determines whether the shape follows a parallel rotation, a perspective rotation, or an oblique rotation, as an integer from 0 to 6.</span></span> 
  
|<span data-ttu-id="42caf-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="42caf-105">**Value**</span></span>|<span data-ttu-id="42caf-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="42caf-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="42caf-107">0</span><span class="sxs-lookup"><span data-stu-id="42caf-107">0</span></span>  <br/> |<span data-ttu-id="42caf-108">Die Form hat keine Rotation.</span><span class="sxs-lookup"><span data-stu-id="42caf-108">The shape does not have any rotation.</span></span>  <br/> |
|<span data-ttu-id="42caf-109">1</span><span class="sxs-lookup"><span data-stu-id="42caf-109">1</span></span>  <br/> |<span data-ttu-id="42caf-110">Die Form hat eine parallele Drehung.</span><span class="sxs-lookup"><span data-stu-id="42caf-110">The shape has a parallel rotation.</span></span>  <br/> |
|<span data-ttu-id="42caf-111">2</span><span class="sxs-lookup"><span data-stu-id="42caf-111">2</span></span>  <br/> |<span data-ttu-id="42caf-112">Die Form hat eine perspektivische Drehung.</span><span class="sxs-lookup"><span data-stu-id="42caf-112">The shape has a perspective rotation.</span></span>  <br/> |
|<span data-ttu-id="42caf-113">3</span><span class="sxs-lookup"><span data-stu-id="42caf-113">3</span></span>  <br/> |<span data-ttu-id="42caf-114">Die Form weist eine schräge Drehung oben links auf.</span><span class="sxs-lookup"><span data-stu-id="42caf-114">The shape has a top left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="42caf-115">4</span><span class="sxs-lookup"><span data-stu-id="42caf-115">4</span></span>  <br/> |<span data-ttu-id="42caf-116">Die Form ist oben rechts schräg gedreht.</span><span class="sxs-lookup"><span data-stu-id="42caf-116">The shape has a top right oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="42caf-117">5</span><span class="sxs-lookup"><span data-stu-id="42caf-117">5</span></span>  <br/> |<span data-ttu-id="42caf-118">Die Form hat eine schräge linke untere Drehung.</span><span class="sxs-lookup"><span data-stu-id="42caf-118">The shape has a bottom left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="42caf-119">6</span><span class="sxs-lookup"><span data-stu-id="42caf-119">6</span></span>  <br/> |<span data-ttu-id="42caf-120">Die Form hat eine schräge unten rechts.</span><span class="sxs-lookup"><span data-stu-id="42caf-120">The shape has a bottom right oblique rotation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="42caf-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42caf-121">Remarks</span></span>

<span data-ttu-id="42caf-122">Wenn Sie einen Verweis auf die \*\*\*\* Zelle RotationType aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="42caf-122">To get a reference to the **RotationType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="42caf-123">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="42caf-123">Cell name:</span></span>  <br/> |<span data-ttu-id="42caf-124">RotationType</span><span class="sxs-lookup"><span data-stu-id="42caf-124">RotationType</span></span>  <br/> |
   
<span data-ttu-id="42caf-125">Wenn Sie einen Verweis auf die \*\*\*\* Zelle RotationType nach Index aus einem Programm abrufen möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="42caf-125">To get a reference to the **RotationType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="42caf-126">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="42caf-126">Section index:</span></span>  <br/> |<span data-ttu-id="42caf-127">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="42caf-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="42caf-128">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="42caf-128">Row index:</span></span>  <br/> |<span data-ttu-id="42caf-129">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="42caf-129">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="42caf-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="42caf-130">Cell index:</span></span>  <br/> |<span data-ttu-id="42caf-131">**visRotationType**</span><span class="sxs-lookup"><span data-stu-id="42caf-131">**visRotationType**</span></span> <br/> |
   

