---
title: Zelle "ShapeShdwShow" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Bestimmt, ob das Shape einen Schatten als ganze Zahl von 0 bis 2 anzeigt.
ms.openlocfilehash: 1da52c20acaa19eab79970a751fad2c225e212ae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422117"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a><span data-ttu-id="1f933-103">Zelle "ShapeShdwShow" (Abschnitt "Fill Format")</span><span class="sxs-lookup"><span data-stu-id="1f933-103">ShapeShdwShow Cell (Fill Format Section)</span></span>

<span data-ttu-id="1f933-104">Bestimmt, ob das Shape einen Schatten als ganze Zahl von 0 bis 2 anzeigt.</span><span class="sxs-lookup"><span data-stu-id="1f933-104">Determines whether the shape displays a shadow, as an integer from 0 to 2.</span></span>
  
|<span data-ttu-id="1f933-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="1f933-105">**Value**</span></span>|<span data-ttu-id="1f933-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1f933-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1f933-107">0</span><span class="sxs-lookup"><span data-stu-id="1f933-107">0</span></span>  <br/> |<span data-ttu-id="1f933-108">Zeigen Sie den Schatten immer an, wenn ein Schatten angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="1f933-108">Always display the shadow if a shadow is specified.</span></span> <span data-ttu-id="1f933-109">Die Schatten für Unterformen werden nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1f933-109">The shadows for sub-shapes are not displayed.</span></span>  <br/> |
|<span data-ttu-id="1f933-110">1</span><span class="sxs-lookup"><span data-stu-id="1f933-110">1</span></span>  <br/> |<span data-ttu-id="1f933-111">Rendern Sie keinen Schatten, es sei denn, die Form verfügt nicht über ein übergeordnetes Element.</span><span class="sxs-lookup"><span data-stu-id="1f933-111">Do not render a shadow unless the shape does not have a parent.</span></span> <span data-ttu-id="1f933-112">Verwenden Sie Schatten in Unterform, wenn sie zusammenge gruppieren.</span><span class="sxs-lookup"><span data-stu-id="1f933-112">Use sub-shape shadows if grouped together.</span></span>  <br/> |
|<span data-ttu-id="1f933-113">2</span><span class="sxs-lookup"><span data-stu-id="1f933-113">2</span></span>  <br/> |<span data-ttu-id="1f933-114">Wenn ein Schatten angegeben ist, wird immer ein Schatten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1f933-114">Always display a shadow if a shadow is specified.</span></span> <span data-ttu-id="1f933-115">Die Schatten für Unterformen werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1f933-115">The shadows for sub-shapes are displayed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f933-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1f933-116">Remarks</span></span>

<span data-ttu-id="1f933-117">Verwenden Sie zum Erhalten eines Verweises auf die **Zelle ShapeShdwShow** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="1f933-117">To get a reference to the **ShapeShdwShow** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1f933-118">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="1f933-118">Cell name:</span></span>  <br/> | <span data-ttu-id="1f933-119">ShapeShdwShow</span><span class="sxs-lookup"><span data-stu-id="1f933-119">ShapeShdwShow</span></span>  <br/> |
   
<span data-ttu-id="1f933-120">Um einen Verweis auf die **Zelle ShapeShdwShow** nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="1f933-120">To get a reference to the **ShapeShdwShow** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1f933-121">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="1f933-121">Section index:</span></span>  <br/> |<span data-ttu-id="1f933-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1f933-122">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1f933-123">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="1f933-123">Row index:</span></span>  <br/> |<span data-ttu-id="1f933-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="1f933-124">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="1f933-125">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="1f933-125">Cell index:</span></span>  <br/> |<span data-ttu-id="1f933-126">**visFillShdwShow**</span><span class="sxs-lookup"><span data-stu-id="1f933-126">**visFillShdwShow**</span></span> <br/> |
   

