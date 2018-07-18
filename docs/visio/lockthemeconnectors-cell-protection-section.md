---
title: LockThemeConnectors Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: Verhindert, dass die ConnectorsSchemeIndex Zelle in der Zeile mit Design durch Anwenden eines neuen Designs oder Auswählen eines neuen Connector Schemas geändert wird. Verhindert nicht, dass Benutzer diesen Wert in das ShapeSheet manuell zu bearbeiten.
ms.openlocfilehash: c74bcf554f0f14de47480397a96680469826d2c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797401"
---
# <a name="lockthemeconnectors-cell-protection-section"></a><span data-ttu-id="31e87-104">LockThemeConnectors Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="31e87-104">LockThemeConnectors Cell (Protection Section)</span></span>

<span data-ttu-id="31e87-105">Verhindert, dass die **ConnectorsSchemeIndex** Zelle in der Zeile mit **Design** durch Anwenden eines neuen Designs oder Auswählen eines neuen Connector Schemas geändert wird.</span><span class="sxs-lookup"><span data-stu-id="31e87-105">Prevents the **ConnectorsSchemeIndex** cell in the **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme.</span></span> <span data-ttu-id="31e87-106">Verhindert nicht, dass Benutzer diesen Wert in das ShapeSheet manuell zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="31e87-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="31e87-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="31e87-107">**Value**</span></span>|<span data-ttu-id="31e87-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="31e87-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="31e87-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="31e87-109">TRUE</span></span>  <br/> |<span data-ttu-id="31e87-110">Die Zelle **ConnectorsSchemeIndex** kann nicht aus dem aktuellen Wert geändert werden, sofern nicht direkt im ShapeSheet geändert.</span><span class="sxs-lookup"><span data-stu-id="31e87-110">The **ConnectorsSchemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="31e87-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="31e87-111">FALSE</span></span>  <br/> |<span data-ttu-id="31e87-112">Die Zelle **ConnectorsSchemeIndex** kann vom aktuellen Wert über die Benutzeroberfläche geändert werden.</span><span class="sxs-lookup"><span data-stu-id="31e87-112">The **ConnectorsSchemeIndex** cell can be changed from its current value through the UI.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31e87-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31e87-113">Remarks</span></span>

<span data-ttu-id="31e87-114">Wenn Sie einen Verweis auf die Zelle **LockThemeConnectors** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="31e87-114">To get a reference to the **LockThemeConnectors** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="31e87-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="31e87-115">Cell name:</span></span>  <br/> | <span data-ttu-id="31e87-116">LockThemeConnectors</span><span class="sxs-lookup"><span data-stu-id="31e87-116">LockThemeConnectors</span></span>  <br/> |
   
<span data-ttu-id="31e87-117">Wenn Sie einen Verweis auf die Zelle **LockThemeConnectors** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="31e87-117">To get a reference to the **LockThemeConnectors** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="31e87-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="31e87-118">Section index:</span></span>  <br/> |<span data-ttu-id="31e87-119">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="31e87-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="31e87-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="31e87-120">Row index:</span></span>  <br/> |<span data-ttu-id="31e87-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="31e87-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="31e87-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="31e87-122">Cell index:</span></span>  <br/> |<span data-ttu-id="31e87-123">**visLockThemeConnectors**</span><span class="sxs-lookup"><span data-stu-id="31e87-123">**visLockThemeConnectors**</span></span> <br/> |
   

