---
title: LockThemeConnectors Cell (Protection section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: Verhindert, dass die Zelle ConnectorsSchemeIndex in der Zeile Designeigenschaften geändert wird, indem ein neues Design angewendet oder ein neues Connector-Schema ausgewählt wird. Verhindert nicht, dass Benutzer diesen Wert manuell im ShapeSheet bearbeiten.
ms.openlocfilehash: 8097e50646fd59f4ac0212cbe9ca2ecfaadab7a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348237"
---
# <a name="lockthemeconnectors-cell-protection-section"></a><span data-ttu-id="6a74e-104">LockThemeConnectors Cell (Protection section)</span><span class="sxs-lookup"><span data-stu-id="6a74e-104">LockThemeConnectors Cell (Protection Section)</span></span>

<span data-ttu-id="6a74e-105">Verhindert, dass die Zelle **ConnectorsSchemeIndex** in der Zeile **Designeigenschaften** geändert wird, indem ein neues Design angewendet oder ein neues Connector-Schema ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="6a74e-105">Prevents the **ConnectorsSchemeIndex** cell in the **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme.</span></span> <span data-ttu-id="6a74e-106">Verhindert nicht, dass Benutzer diesen Wert manuell im ShapeSheet bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="6a74e-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="6a74e-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="6a74e-107">**Value**</span></span>|<span data-ttu-id="6a74e-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6a74e-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6a74e-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="6a74e-109">TRUE</span></span>  <br/> |<span data-ttu-id="6a74e-110">Die Zelle **ConnectorsSchemeIndex** kann nicht von Ihrem aktuellen Wert geändert werden, es sei denn, Sie wurde direkt im ShapeSheet geändert.</span><span class="sxs-lookup"><span data-stu-id="6a74e-110">The **ConnectorsSchemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="6a74e-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="6a74e-111">FALSE</span></span>  <br/> |<span data-ttu-id="6a74e-112">Die **ConnectorsSchemeIndex** -Zelle kann von Ihrem aktuellen Wert über die Benutzeroberfläche geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6a74e-112">The **ConnectorsSchemeIndex** cell can be changed from its current value through the UI.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a74e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a74e-113">Remarks</span></span>

<span data-ttu-id="6a74e-114">Wenn Sie einen Verweis auf die Zelle **LockThemeConnectors** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6a74e-114">To get a reference to the **LockThemeConnectors** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6a74e-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="6a74e-115">Cell name:</span></span>  <br/> | <span data-ttu-id="6a74e-116">LockThemeConnectors</span><span class="sxs-lookup"><span data-stu-id="6a74e-116">LockThemeConnectors</span></span>  <br/> |
   
<span data-ttu-id="6a74e-117">Wenn Sie einen Verweis auf die Zelle **LockThemeConnectors** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="6a74e-117">To get a reference to the **LockThemeConnectors** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6a74e-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="6a74e-118">Section index:</span></span>  <br/> |<span data-ttu-id="6a74e-119">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6a74e-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6a74e-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="6a74e-120">Row index:</span></span>  <br/> |<span data-ttu-id="6a74e-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="6a74e-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="6a74e-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="6a74e-122">Cell index:</span></span>  <br/> |<span data-ttu-id="6a74e-123">**visLockThemeConnectors**</span><span class="sxs-lookup"><span data-stu-id="6a74e-123">**visLockThemeConnectors**</span></span> <br/> |
   

