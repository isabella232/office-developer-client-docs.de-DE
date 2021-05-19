---
title: Zelle "QuickStyleType" (Abschnitt "Quick Style")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: Bestimmt den Typ der Schnellformatvorlage (2-dimensional, 1-dimensional oder Verbinder), den die Form erbt.
ms.openlocfilehash: 95aced62c6397fc3229de29b98d3f18e5f69d05b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410504"
---
# <a name="quickstyletype-cell-quick-style-section"></a><span data-ttu-id="5073d-103">Zelle "QuickStyleType" (Abschnitt "Quick Style")</span><span class="sxs-lookup"><span data-stu-id="5073d-103">QuickStyleType Cell (Quick Style Section)</span></span>

<span data-ttu-id="5073d-104">Bestimmt den Typ der Schnellformatvorlage (2-dimensional, 1-dimensional oder Verbinder), den die Form erbt.</span><span class="sxs-lookup"><span data-stu-id="5073d-104">Determines the type of Quick Style (2-dimensional, 1-dimensional, or connector) that the shape inherits.</span></span> 
  
|<span data-ttu-id="5073d-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="5073d-105">**Value**</span></span>|<span data-ttu-id="5073d-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5073d-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5073d-107">0</span><span class="sxs-lookup"><span data-stu-id="5073d-107">0</span></span>  <br/> |<span data-ttu-id="5073d-108">Visio automatisch auswählen</span><span class="sxs-lookup"><span data-stu-id="5073d-108">Visio chooses automatically</span></span>  <br/> |
|<span data-ttu-id="5073d-109">1</span><span class="sxs-lookup"><span data-stu-id="5073d-109">1</span></span>  <br/> |<span data-ttu-id="5073d-110">1-dimensional</span><span class="sxs-lookup"><span data-stu-id="5073d-110">1-dimensional</span></span>  <br/> |
|<span data-ttu-id="5073d-111">2</span><span class="sxs-lookup"><span data-stu-id="5073d-111">2</span></span>  <br/> |<span data-ttu-id="5073d-112">2-dimensional</span><span class="sxs-lookup"><span data-stu-id="5073d-112">2-dimensional</span></span>  <br/> |
|<span data-ttu-id="5073d-113">3</span><span class="sxs-lookup"><span data-stu-id="5073d-113">3</span></span>  <br/> |<span data-ttu-id="5073d-114">Connector</span><span class="sxs-lookup"><span data-stu-id="5073d-114">Connector</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5073d-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5073d-115">Remarks</span></span>

<span data-ttu-id="5073d-116">Verwenden Sie zum Erhalten eines Verweises auf die **Zelle QuickStyleType** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="5073d-116">To get a reference to the **QuickStyleType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5073d-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="5073d-117">Cell name:</span></span>  <br/> | <span data-ttu-id="5073d-118">QuickStyleType</span><span class="sxs-lookup"><span data-stu-id="5073d-118">QuickStyleType</span></span>  <br/> |
   
<span data-ttu-id="5073d-119">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **QuickStyleType-Zelle** nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="5073d-119">To get a reference to the **QuickStyleType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5073d-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="5073d-120">Section index:</span></span>  <br/> |<span data-ttu-id="5073d-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5073d-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5073d-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="5073d-122">Row index:</span></span>  <br/> |<span data-ttu-id="5073d-123">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="5073d-123">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="5073d-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="5073d-124">Cell index:</span></span>  <br/> |<span data-ttu-id="5073d-125">**visQuickStyleType**</span><span class="sxs-lookup"><span data-stu-id="5073d-125">**visQuickStyleType**</span></span> <br/> |
   

