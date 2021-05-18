---
title: Zelle "CompoundType" (Abschnitt "Line Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: Bestimmt den zusammengesetzten Typ der Linie einer Form.
ms.openlocfilehash: 120975e419656234266cb8151b2fa37ef19602e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407172"
---
# <a name="compoundtype-cell-line-format-section"></a><span data-ttu-id="24c0e-103">Zelle "CompoundType" (Abschnitt "Line Format")</span><span class="sxs-lookup"><span data-stu-id="24c0e-103">CompoundType Cell (Line Format Section)</span></span>

<span data-ttu-id="24c0e-104">Bestimmt den zusammengesetzten Typ der Linie einer Form.</span><span class="sxs-lookup"><span data-stu-id="24c0e-104">Determines the compound type of the line of a shape.</span></span> 
  
|<span data-ttu-id="24c0e-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="24c0e-105">**Value**</span></span>|<span data-ttu-id="24c0e-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="24c0e-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="24c0e-107">0</span><span class="sxs-lookup"><span data-stu-id="24c0e-107">0</span></span>  <br/> |<span data-ttu-id="24c0e-108">Einfach</span><span class="sxs-lookup"><span data-stu-id="24c0e-108">Simple</span></span>  <br/> |
|<span data-ttu-id="24c0e-109">1</span><span class="sxs-lookup"><span data-stu-id="24c0e-109">1</span></span>  <br/> |<span data-ttu-id="24c0e-110">Gleitkommawert mit doppelter Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="24c0e-110">Double</span></span>  <br/> |
|<span data-ttu-id="24c0e-111">2</span><span class="sxs-lookup"><span data-stu-id="24c0e-111">2</span></span>  <br/> |<span data-ttu-id="24c0e-112">Dick dünn</span><span class="sxs-lookup"><span data-stu-id="24c0e-112">Thick thin</span></span>  <br/> |
|<span data-ttu-id="24c0e-113">3</span><span class="sxs-lookup"><span data-stu-id="24c0e-113">3</span></span>  <br/> |<span data-ttu-id="24c0e-114">Dünn dick</span><span class="sxs-lookup"><span data-stu-id="24c0e-114">Thin thick</span></span>  <br/> |
|<span data-ttu-id="24c0e-115">4 </span><span class="sxs-lookup"><span data-stu-id="24c0e-115">4</span></span>  <br/> |<span data-ttu-id="24c0e-116">Triple</span><span class="sxs-lookup"><span data-stu-id="24c0e-116">Triple</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24c0e-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="24c0e-117">Remarks</span></span>

<span data-ttu-id="24c0e-118">Verwenden Sie zum Erhalten eines Verweises auf die **Zelle CompoundType** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="24c0e-118">To get a reference to the **CompoundType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="24c0e-119">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="24c0e-119">Cell name:</span></span>  <br/> | <span data-ttu-id="24c0e-120">CompoundType</span><span class="sxs-lookup"><span data-stu-id="24c0e-120">CompoundType</span></span>  <br/> |
   
<span data-ttu-id="24c0e-121">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle CompoundType** nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="24c0e-121">To get a reference to the **CompoundType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="24c0e-122">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="24c0e-122">Section index:</span></span>  <br/> |<span data-ttu-id="24c0e-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="24c0e-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="24c0e-124">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="24c0e-124">Row index:</span></span>  <br/> |<span data-ttu-id="24c0e-125">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="24c0e-125">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="24c0e-126">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="24c0e-126">Cell index:</span></span>  <br/> |<span data-ttu-id="24c0e-127">**visCompoundType**</span><span class="sxs-lookup"><span data-stu-id="24c0e-127">**visCompoundType**</span></span> <br/> |
   

