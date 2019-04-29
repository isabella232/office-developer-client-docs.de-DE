---
title: LockThemeIndex Cell (Protection section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: Verhindert, dass die ThemeIndex Zelle in Designeigenschaften Zeile geändert wird, indem ein neues Design angewendet oder ein neues Connector-Schema ausgewählt wird. Verhindert nicht, dass Benutzer diesen Wert manuell im ShapeSheet bearbeiten.
ms.openlocfilehash: 519c17f6e00c9aad2b5522bc66b41c0ceb75911b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411239"
---
# <a name="lockthemeindex-cell-protection-section"></a><span data-ttu-id="81e02-104">LockThemeIndex Cell (Protection section)</span><span class="sxs-lookup"><span data-stu-id="81e02-104">LockThemeIndex Cell (Protection Section)</span></span>

<span data-ttu-id="81e02-105">Verhindert, dass die **ThemeIndex** Zelle in **Designeigenschaften** Zeile geändert wird, indem ein neues Design angewendet oder ein neues Connector-Schema ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="81e02-105">Prevents **ThemeIndex** cell in **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme.</span></span> <span data-ttu-id="81e02-106">Verhindert nicht, dass Benutzer diesen Wert manuell im ShapeSheet bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="81e02-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="81e02-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="81e02-107">**Value**</span></span>|<span data-ttu-id="81e02-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="81e02-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="81e02-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="81e02-109">TRUE</span></span>  <br/> |<span data-ttu-id="81e02-110">Die Zelle **ThemeIndex** kann nicht von Ihrem aktuellen Wert geändert werden, es sei denn, Sie wurde direkt im ShapeSheet geändert.</span><span class="sxs-lookup"><span data-stu-id="81e02-110">The **ThemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="81e02-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="81e02-111">FALSE</span></span>  <br/> |<span data-ttu-id="81e02-112">Die Zelle **ThemeIndex** kann vom aktuellen Wert geändert werden, wenn das Design geändert wird.</span><span class="sxs-lookup"><span data-stu-id="81e02-112">The **ThemeIndex** cell can be changed from its current value when the theme is changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81e02-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81e02-113">Remarks</span></span>

<span data-ttu-id="81e02-114">Wenn Sie einen Verweis auf die Zelle **LockThemeIndex** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="81e02-114">To get a reference to the **LockThemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="81e02-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="81e02-115">Cell name:</span></span>  <br/> | <span data-ttu-id="81e02-116">LockThemeIndex</span><span class="sxs-lookup"><span data-stu-id="81e02-116">LockThemeIndex</span></span>  <br/> |
   
<span data-ttu-id="81e02-117">Wenn Sie einen Verweis auf die Zelle **LockThemeIndex** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="81e02-117">To get a reference to the **LockThemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="81e02-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="81e02-118">Section index:</span></span>  <br/> |<span data-ttu-id="81e02-119">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="81e02-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="81e02-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="81e02-120">Row index:</span></span>  <br/> |<span data-ttu-id="81e02-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="81e02-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="81e02-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="81e02-122">Cell index:</span></span>  <br/> |<span data-ttu-id="81e02-123">**visLockThemeIndex**</span><span class="sxs-lookup"><span data-stu-id="81e02-123">**visLockThemeIndex**</span></span> <br/> |
   

