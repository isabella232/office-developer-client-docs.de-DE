---
title: Zelle "LockThemeFonts" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: Verhindert, dass die Zelle FontIndex in der Zeile Designeigenschaften geändert wird, indem ein neues Design angewendet wird. Verhindert nicht, dass Benutzer diesen Wert im ShapeSheet manuell bearbeiten.
ms.openlocfilehash: b3bd21c1dcd8c8c13d843c50cb29edcc5b8c4999
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421228"
---
# <a name="lockthemefonts-cell-protection-section"></a><span data-ttu-id="d6dd7-104">Zelle "LockThemeFonts" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="d6dd7-104">LockThemeFonts Cell (Protection Section)</span></span>

<span data-ttu-id="d6dd7-105">Verhindert, **dass die Zelle FontIndex** in der Zeile **Designeigenschaften** geändert wird, indem ein neues Design angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="d6dd7-105">Prevents the **FontIndex** cell in the **Theme Properties** row from being altered by applying a new theme.</span></span> <span data-ttu-id="d6dd7-106">Verhindert nicht, dass Benutzer diesen Wert im ShapeSheet manuell bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="d6dd7-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="d6dd7-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d6dd7-107">**Value**</span></span>|<span data-ttu-id="d6dd7-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6dd7-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d6dd7-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="d6dd7-109">TRUE</span></span>  <br/> |<span data-ttu-id="d6dd7-110">Die **Zelle FontIndex** kann nicht vom aktuellen Wert geändert werden, es sei denn, sie wird direkt im ShapeSheet geändert.</span><span class="sxs-lookup"><span data-stu-id="d6dd7-110">The **FontIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="d6dd7-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="d6dd7-111">FALSE</span></span>  <br/> |<span data-ttu-id="d6dd7-112">Die **Zelle FontIndex** kann von ihrem aktuellen Wert geändert werden, wenn das Design geändert wird.</span><span class="sxs-lookup"><span data-stu-id="d6dd7-112">The **FontIndex** cell can be changed from its current value when the theme is changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6dd7-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d6dd7-113">Remarks</span></span>

<span data-ttu-id="d6dd7-114">Verwenden Sie zum Erhalten eines Verweises auf die **Zelle LockThemeFonts** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="d6dd7-114">To get a reference to the **LockThemeFonts** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d6dd7-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="d6dd7-115">Cell name:</span></span>  <br/> | <span data-ttu-id="d6dd7-116">LockThemeFonts</span><span class="sxs-lookup"><span data-stu-id="d6dd7-116">LockThemeFonts</span></span>  <br/> |
   
<span data-ttu-id="d6dd7-117">Um einen Verweis auf die **Zelle LockThemeFonts** nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="d6dd7-117">To get a reference to the **LockThemeFonts** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d6dd7-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="d6dd7-118">Section index:</span></span>  <br/> |<span data-ttu-id="d6dd7-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d6dd7-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d6dd7-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d6dd7-120">Row index:</span></span>  <br/> |<span data-ttu-id="d6dd7-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="d6dd7-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="d6dd7-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="d6dd7-122">Cell index:</span></span>  <br/> |<span data-ttu-id="d6dd7-123">**visLockThemeFonts**</span><span class="sxs-lookup"><span data-stu-id="d6dd7-123">**visLockThemeFonts**</span></span> <br/> |
   

