---
title: Zelle "LockThemeConnectors" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: Verhindert, dass die Zelle ConnectorsSchemeIndex in der Zeile Designeigenschaften geändert wird, indem ein neues Design angewendet oder ein neues Verbindungsschema ausgewählt wird. Verhindert nicht, dass Benutzer diesen Wert im ShapeSheet manuell bearbeiten.
ms.openlocfilehash: 8097e50646fd59f4ac0212cbe9ca2ecfaadab7a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438407"
---
# <a name="lockthemeconnectors-cell-protection-section"></a><span data-ttu-id="ac2a3-104">Zelle "LockThemeConnectors" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="ac2a3-104">LockThemeConnectors Cell (Protection Section)</span></span>

<span data-ttu-id="ac2a3-105">Verhindert, **dass die Zelle ConnectorsSchemeIndex** in der Zeile **Designeigenschaften** geändert wird, indem ein neues Design angewendet oder ein neues Verbindungsschema ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="ac2a3-105">Prevents the **ConnectorsSchemeIndex** cell in the **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme.</span></span> <span data-ttu-id="ac2a3-106">Verhindert nicht, dass Benutzer diesen Wert im ShapeSheet manuell bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="ac2a3-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="ac2a3-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ac2a3-107">**Value**</span></span>|<span data-ttu-id="ac2a3-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ac2a3-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ac2a3-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="ac2a3-109">TRUE</span></span>  <br/> |<span data-ttu-id="ac2a3-110">Die **Zelle ConnectorsSchemeIndex** kann nicht vom aktuellen Wert geändert werden, es sei denn, sie wird direkt im ShapeSheet geändert.</span><span class="sxs-lookup"><span data-stu-id="ac2a3-110">The **ConnectorsSchemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="ac2a3-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="ac2a3-111">FALSE</span></span>  <br/> |<span data-ttu-id="ac2a3-112">Die **Zelle ConnectorsSchemeIndex** kann über die Benutzeroberfläche von ihrem aktuellen Wert geändert werden.</span><span class="sxs-lookup"><span data-stu-id="ac2a3-112">The **ConnectorsSchemeIndex** cell can be changed from its current value through the UI.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac2a3-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ac2a3-113">Remarks</span></span>

<span data-ttu-id="ac2a3-114">Verwenden Sie zum Erhalten eines Verweises auf die **Zelle LockThemeConnectors** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="ac2a3-114">To get a reference to the **LockThemeConnectors** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ac2a3-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ac2a3-115">Cell name:</span></span>  <br/> | <span data-ttu-id="ac2a3-116">LockThemeConnectors</span><span class="sxs-lookup"><span data-stu-id="ac2a3-116">LockThemeConnectors</span></span>  <br/> |
   
<span data-ttu-id="ac2a3-117">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle LockThemeConnectors** nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="ac2a3-117">To get a reference to the **LockThemeConnectors** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ac2a3-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ac2a3-118">Section index:</span></span>  <br/> |<span data-ttu-id="ac2a3-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ac2a3-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ac2a3-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ac2a3-120">Row index:</span></span>  <br/> |<span data-ttu-id="ac2a3-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="ac2a3-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="ac2a3-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="ac2a3-122">Cell index:</span></span>  <br/> |<span data-ttu-id="ac2a3-123">**visLockThemeConnectors**</span><span class="sxs-lookup"><span data-stu-id="ac2a3-123">**visLockThemeConnectors**</span></span> <br/> |
   

