---
title: QuickStyleFontColor Cell (Quick Style section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31c56d08-19ea-4b8b-8be7-42e1c736fbca
description: Bestimmt die Schriftfarbe aus den Schnellformatvorlagen, die der Text eines Shapes vom aktiven Design erbt, als ganze Zahl von 0-1.
ms.openlocfilehash: bd645383df02260fcf6a2045764d9a1b44126090
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282635"
---
# <a name="quickstylefontcolor-cell-quick-style-section"></a><span data-ttu-id="7efa1-103">QuickStyleFontColor Cell (Quick Style section)</span><span class="sxs-lookup"><span data-stu-id="7efa1-103">QuickStyleFontColor Cell (Quick Style Section)</span></span>

<span data-ttu-id="7efa1-104">Bestimmt die Schriftfarbe aus den Schnellformatvorlagen, die der Text eines Shapes vom aktiven Design erbt, als ganze Zahl von 0-1.</span><span class="sxs-lookup"><span data-stu-id="7efa1-104">Determines the font color from the Quick Styles that a shape's text inherits from the active theme, as an integer from 0-1.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7efa1-105">Wert</span><span class="sxs-lookup"><span data-stu-id="7efa1-105">Value</span></span>  <br/> |<span data-ttu-id="7efa1-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7efa1-106">Description</span></span>  <br/> |
|<span data-ttu-id="7efa1-107">0</span><span class="sxs-lookup"><span data-stu-id="7efa1-107">0</span></span>  <br/> |<span data-ttu-id="7efa1-108">Der Shape-Text verwendet die dunkle Schriftfarbe.</span><span class="sxs-lookup"><span data-stu-id="7efa1-108">The shape text uses the Dark font color.</span></span>  <br/> |
|<span data-ttu-id="7efa1-109">1</span><span class="sxs-lookup"><span data-stu-id="7efa1-109">1</span></span>  <br/> |<span data-ttu-id="7efa1-110">Der Shape-Text verwendet die Schriftfarbe Light.</span><span class="sxs-lookup"><span data-stu-id="7efa1-110">The shape text uses the Light font color.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7efa1-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7efa1-111">Remarks</span></span>

<span data-ttu-id="7efa1-112">Wenn Sie einen Verweis auf die Zelle **QuickStyleFontColor** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7efa1-112">To get a reference to the **QuickStyleFontColor** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7efa1-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="7efa1-113">Cell name:</span></span>  <br/> | <span data-ttu-id="7efa1-114">QuickStyleFontColor</span><span class="sxs-lookup"><span data-stu-id="7efa1-114">QuickStyleFontColor</span></span>  <br/> |
   
<span data-ttu-id="7efa1-115">Wenn Sie einen Verweis auf die Zelle **QuickStyleFontColor** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="7efa1-115">To get a reference to the **QuickStyleFontColor** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7efa1-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="7efa1-116">Section index:</span></span>  <br/> |<span data-ttu-id="7efa1-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7efa1-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7efa1-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="7efa1-118">Row index:</span></span>  <br/> |<span data-ttu-id="7efa1-119">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="7efa1-119">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="7efa1-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="7efa1-120">Cell index:</span></span>  <br/> |<span data-ttu-id="7efa1-121">**visQuickStyleFontColor**</span><span class="sxs-lookup"><span data-stu-id="7efa1-121">**visQuickStyleFontColor**</span></span> <br/> |
   

