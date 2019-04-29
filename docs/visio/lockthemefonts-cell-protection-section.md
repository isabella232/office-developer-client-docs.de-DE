---
title: LockThemeFonts Cell (Protection section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: Verhindert, dass die Zelle FontIndex in der Zeile Designeigenschaften durch Anwenden eines neuen Designs geändert wird. Verhindert nicht, dass Benutzer diesen Wert manuell im ShapeSheet bearbeiten.
ms.openlocfilehash: b3bd21c1dcd8c8c13d843c50cb29edcc5b8c4999
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421228"
---
# <a name="lockthemefonts-cell-protection-section"></a><span data-ttu-id="535fc-104">LockThemeFonts Cell (Protection section)</span><span class="sxs-lookup"><span data-stu-id="535fc-104">LockThemeFonts Cell (Protection Section)</span></span>

<span data-ttu-id="535fc-105">Verhindert, dass die Zelle **FontIndex** in der Zeile **Designeigenschaften** durch Anwenden eines neuen Designs geändert wird.</span><span class="sxs-lookup"><span data-stu-id="535fc-105">Prevents the **FontIndex** cell in the **Theme Properties** row from being altered by applying a new theme.</span></span> <span data-ttu-id="535fc-106">Verhindert nicht, dass Benutzer diesen Wert manuell im ShapeSheet bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="535fc-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="535fc-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="535fc-107">**Value**</span></span>|<span data-ttu-id="535fc-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="535fc-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="535fc-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="535fc-109">TRUE</span></span>  <br/> |<span data-ttu-id="535fc-110">Die Zelle **FontIndex** kann nicht von Ihrem aktuellen Wert geändert werden, es sei denn, Sie wurde direkt im ShapeSheet geändert.</span><span class="sxs-lookup"><span data-stu-id="535fc-110">The **FontIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="535fc-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="535fc-111">FALSE</span></span>  <br/> |<span data-ttu-id="535fc-112">Die Zelle **FontIndex** kann vom aktuellen Wert geändert werden, wenn das Design geändert wird.</span><span class="sxs-lookup"><span data-stu-id="535fc-112">The **FontIndex** cell can be changed from its current value when the theme is changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="535fc-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="535fc-113">Remarks</span></span>

<span data-ttu-id="535fc-114">Wenn Sie einen Verweis auf die Zelle **LockThemeFonts** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="535fc-114">To get a reference to the **LockThemeFonts** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="535fc-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="535fc-115">Cell name:</span></span>  <br/> | <span data-ttu-id="535fc-116">LockThemeFonts</span><span class="sxs-lookup"><span data-stu-id="535fc-116">LockThemeFonts</span></span>  <br/> |
   
<span data-ttu-id="535fc-117">Wenn Sie einen Verweis auf die Zelle **LockThemeFonts** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="535fc-117">To get a reference to the **LockThemeFonts** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="535fc-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="535fc-118">Section index:</span></span>  <br/> |<span data-ttu-id="535fc-119">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="535fc-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="535fc-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="535fc-120">Row index:</span></span>  <br/> |<span data-ttu-id="535fc-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="535fc-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="535fc-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="535fc-122">Cell index:</span></span>  <br/> |<span data-ttu-id="535fc-123">**visLockThemeFonts**</span><span class="sxs-lookup"><span data-stu-id="535fc-123">**visLockThemeFonts**</span></span> <br/> |
   

