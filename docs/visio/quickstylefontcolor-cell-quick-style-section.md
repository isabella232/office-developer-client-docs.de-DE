---
title: Zelle "QuickStyleFontColor" (Abschnitt "Quick Style")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31c56d08-19ea-4b8b-8be7-42e1c736fbca
description: Bestimmt die Schriftfarbe aus den Schnellformatvorlagen, die der Text eines Shapes vom aktiven Design erbt, als ganze Zahl von 0 bis 1.
ms.openlocfilehash: bd645383df02260fcf6a2045764d9a1b44126090
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415026"
---
# <a name="quickstylefontcolor-cell-quick-style-section"></a><span data-ttu-id="437da-103">Zelle "QuickStyleFontColor" (Abschnitt "Quick Style")</span><span class="sxs-lookup"><span data-stu-id="437da-103">QuickStyleFontColor Cell (Quick Style Section)</span></span>

<span data-ttu-id="437da-104">Bestimmt die Schriftfarbe aus den Schnellformatvorlagen, die der Text eines Shapes vom aktiven Design erbt, als ganze Zahl von 0 bis 1.</span><span class="sxs-lookup"><span data-stu-id="437da-104">Determines the font color from the Quick Styles that a shape's text inherits from the active theme, as an integer from 0-1.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="437da-105">Wert</span><span class="sxs-lookup"><span data-stu-id="437da-105">Value</span></span>  <br/> |<span data-ttu-id="437da-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="437da-106">Description</span></span>  <br/> |
|<span data-ttu-id="437da-107">0</span><span class="sxs-lookup"><span data-stu-id="437da-107">0</span></span>  <br/> |<span data-ttu-id="437da-108">Der Formtext verwendet die Schriftfarbe Dunkel.</span><span class="sxs-lookup"><span data-stu-id="437da-108">The shape text uses the Dark font color.</span></span>  <br/> |
|<span data-ttu-id="437da-109">1</span><span class="sxs-lookup"><span data-stu-id="437da-109">1</span></span>  <br/> |<span data-ttu-id="437da-110">Der Formtext verwendet die Schriftfarbe Light.</span><span class="sxs-lookup"><span data-stu-id="437da-110">The shape text uses the Light font color.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="437da-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="437da-111">Remarks</span></span>

<span data-ttu-id="437da-112">Verwenden Sie zum Erhalten eines Verweises auf die **QuickStyleFontColor-Zelle** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="437da-112">To get a reference to the **QuickStyleFontColor** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="437da-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="437da-113">Cell name:</span></span>  <br/> | <span data-ttu-id="437da-114">QuickStyleFontColor</span><span class="sxs-lookup"><span data-stu-id="437da-114">QuickStyleFontColor</span></span>  <br/> |
   
<span data-ttu-id="437da-115">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **QuickStyleFontColor-Zelle** nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="437da-115">To get a reference to the **QuickStyleFontColor** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="437da-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="437da-116">Section index:</span></span>  <br/> |<span data-ttu-id="437da-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="437da-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="437da-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="437da-118">Row index:</span></span>  <br/> |<span data-ttu-id="437da-119">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="437da-119">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="437da-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="437da-120">Cell index:</span></span>  <br/> |<span data-ttu-id="437da-121">**visQuickStyleFontColor**</span><span class="sxs-lookup"><span data-stu-id="437da-121">**visQuickStyleFontColor**</span></span> <br/> |
   

