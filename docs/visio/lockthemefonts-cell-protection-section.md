---
title: LockThemeFonts Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: Verhindert, dass die FontIndex Zelle in der Zeile mit Design anwenden eines neuen Designs geändert werden. Verhindert nicht, dass Benutzer diesen Wert in das ShapeSheet manuell zu bearbeiten.
ms.openlocfilehash: b90ffe4c5555df017bb0506a78351514c954ec39
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797422"
---
# <a name="lockthemefonts-cell-protection-section"></a><span data-ttu-id="347a6-104">LockThemeFonts Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="347a6-104">LockThemeFonts Cell (Protection Section)</span></span>

<span data-ttu-id="347a6-105">Verhindert, dass die **FontIndex** Zelle in der Zeile mit **Design** Anwenden eines neuen Designs geändert werden.</span><span class="sxs-lookup"><span data-stu-id="347a6-105">Prevents the **FontIndex** cell in the **Theme Properties** row from being altered by applying a new theme.</span></span> <span data-ttu-id="347a6-106">Verhindert nicht, dass Benutzer diesen Wert in das ShapeSheet manuell zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="347a6-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="347a6-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="347a6-107">**Value**</span></span>|<span data-ttu-id="347a6-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="347a6-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="347a6-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="347a6-109">TRUE</span></span>  <br/> |<span data-ttu-id="347a6-110">Die Zelle **FontIndex** kann nicht aus dem aktuellen Wert geändert werden, sofern nicht direkt im ShapeSheet geändert.</span><span class="sxs-lookup"><span data-stu-id="347a6-110">The **FontIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="347a6-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="347a6-111">FALSE</span></span>  <br/> |<span data-ttu-id="347a6-112">Die Zelle **FontIndex** kann vom aktuellen Wert geändert werden, wenn das Design geändert wird.</span><span class="sxs-lookup"><span data-stu-id="347a6-112">The **FontIndex** cell can be changed from its current value when the theme is changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="347a6-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="347a6-113">Remarks</span></span>

<span data-ttu-id="347a6-114">Wenn Sie einen Verweis auf die Zelle **LockThemeFonts** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="347a6-114">To get a reference to the **LockThemeFonts** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="347a6-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="347a6-115">Cell name:</span></span>  <br/> | <span data-ttu-id="347a6-116">LockThemeFonts</span><span class="sxs-lookup"><span data-stu-id="347a6-116">LockThemeFonts</span></span>  <br/> |
   
<span data-ttu-id="347a6-117">Wenn Sie einen Verweis auf die Zelle **LockThemeFonts** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="347a6-117">To get a reference to the **LockThemeFonts** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="347a6-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="347a6-118">Section index:</span></span>  <br/> |<span data-ttu-id="347a6-119">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="347a6-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="347a6-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="347a6-120">Row index:</span></span>  <br/> |<span data-ttu-id="347a6-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="347a6-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="347a6-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="347a6-122">Cell index:</span></span>  <br/> |<span data-ttu-id="347a6-123">**visLockThemeFonts**</span><span class="sxs-lookup"><span data-stu-id="347a6-123">**visLockThemeFonts**</span></span> <br/> |
   

