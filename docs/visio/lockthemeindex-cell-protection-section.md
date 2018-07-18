---
title: LockThemeIndex Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: Verhindert, dass ThemeIndex-Zelle in der Zeile mit Komponenteneigenschaften Design durch Anwenden eines neuen Designs oder Auswählen eines neuen Connector Schemas geändert wird. Verhindert nicht, dass Benutzer diesen Wert in das ShapeSheet manuell zu bearbeiten.
ms.openlocfilehash: 4bef3eb799c943ff89027e69ae8580c9c0e51243
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797404"
---
# <a name="lockthemeindex-cell-protection-section"></a><span data-ttu-id="c2761-104">LockThemeIndex Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="c2761-104">LockThemeIndex Cell (Protection Section)</span></span>

<span data-ttu-id="c2761-105">Verhindert, dass **ThemeIndex** -Zelle in der Zeile mit **Komponenteneigenschaften Design** durch Anwenden eines neuen Designs oder Auswählen eines neuen Connector Schemas geändert wird.</span><span class="sxs-lookup"><span data-stu-id="c2761-105">Prevents **ThemeIndex** cell in **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme.</span></span> <span data-ttu-id="c2761-106">Verhindert nicht, dass Benutzer diesen Wert in das ShapeSheet manuell zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="c2761-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="c2761-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="c2761-107">**Value**</span></span>|<span data-ttu-id="c2761-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c2761-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c2761-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="c2761-109">TRUE</span></span>  <br/> |<span data-ttu-id="c2761-110">Die Zelle **ThemeIndex** kann nicht aus dem aktuellen Wert geändert werden, sofern nicht direkt im ShapeSheet geändert.</span><span class="sxs-lookup"><span data-stu-id="c2761-110">The **ThemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="c2761-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="c2761-111">FALSE</span></span>  <br/> |<span data-ttu-id="c2761-112">Die Zelle **ThemeIndex** kann vom aktuellen Wert geändert werden, wenn das Design geändert wird.</span><span class="sxs-lookup"><span data-stu-id="c2761-112">The **ThemeIndex** cell can be changed from its current value when the theme is changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2761-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2761-113">Remarks</span></span>

<span data-ttu-id="c2761-114">Wenn Sie einen Verweis auf die Zelle **LockThemeIndex** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c2761-114">To get a reference to the **LockThemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c2761-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="c2761-115">Cell name:</span></span>  <br/> | <span data-ttu-id="c2761-116">LockThemeIndex</span><span class="sxs-lookup"><span data-stu-id="c2761-116">LockThemeIndex</span></span>  <br/> |
   
<span data-ttu-id="c2761-117">Wenn Sie einen Verweis auf die Zelle **LockThemeIndex** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="c2761-117">To get a reference to the **LockThemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c2761-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="c2761-118">Section index:</span></span>  <br/> |<span data-ttu-id="c2761-119">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c2761-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c2761-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="c2761-120">Row index:</span></span>  <br/> |<span data-ttu-id="c2761-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="c2761-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="c2761-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="c2761-122">Cell index:</span></span>  <br/> |<span data-ttu-id="c2761-123">**visLockThemeIndex**</span><span class="sxs-lookup"><span data-stu-id="c2761-123">**visLockThemeIndex**</span></span> <br/> |
   

