---
title: Zelle "LockReplace" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b3880511-dd27-4dc2-9e50-a49084ef8195
description: Gibt an, ob ein Shape an einem Ersetzungsvorgang teilnehmen kann (entweder als Ziel- oder als Ersatzform).
ms.openlocfilehash: 8b0e3175cacd9b906d91a4185dcd98fad604d8bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404141"
---
# <a name="lockreplace-cell-protection-section"></a><span data-ttu-id="91291-103">Zelle "LockReplace" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="91291-103">LockReplace Cell (Protection Section)</span></span>

<span data-ttu-id="91291-104">Gibt an, ob ein Shape an einem Ersetzungsvorgang teilnehmen kann (entweder als Ziel- oder als Ersatzform).</span><span class="sxs-lookup"><span data-stu-id="91291-104">Indicates whether a shape can participate in a replacement operation (as either a target or a replacement shape).</span></span> 
  
|<span data-ttu-id="91291-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="91291-105">**Value**</span></span>|<span data-ttu-id="91291-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="91291-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="91291-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="91291-107">TRUE</span></span>  <br/> |<span data-ttu-id="91291-108">Das Shape kann nicht ersetzt oder als Ersatzform verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="91291-108">The shape cannot be replaced or be used as a replacement shape.</span></span>  <br/> <span data-ttu-id="91291-109">Für eine Form auf dem Zeichenbereich wird die Schaltfläche **Shape** ändern deaktiviert, wenn die Form ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="91291-109">For a shape on the canvas, the **Change Shape** button is disabled when the shape is selected.</span></span>  <br/> <span data-ttu-id="91291-110">Bei einer Form auf einer Schablone wird das Shape nicht  als Ersatzform angezeigt, wenn auf die Schaltfläche Shape ändern geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="91291-110">For a shape on a stencil, the shape does not appear as a replacement shape when the **Change Shape** button is clicked.</span></span>  <br/> |
|<span data-ttu-id="91291-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="91291-111">FALSE</span></span>  <br/> |<span data-ttu-id="91291-112">Das Shape kann ersetzt oder als Ersatzform verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="91291-112">The shape can be replaced or used as a replacement shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91291-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="91291-113">Remarks</span></span>

<span data-ttu-id="91291-114">Verwenden Sie zum Erhalten eines Verweises auf die **Zelle LockReplace** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="91291-114">To get a reference to the **LockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="91291-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="91291-115">Cell name:</span></span>  <br/> | <span data-ttu-id="91291-116">LockReplace</span><span class="sxs-lookup"><span data-stu-id="91291-116">LockReplace</span></span>  <br/> |
   
<span data-ttu-id="91291-117">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle LockReplace** nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="91291-117">To get a reference to the **LockReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="91291-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="91291-118">Section index:</span></span>  <br/> |<span data-ttu-id="91291-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="91291-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="91291-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="91291-120">Row index:</span></span>  <br/> |<span data-ttu-id="91291-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="91291-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="91291-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="91291-122">Cell index:</span></span>  <br/> |<span data-ttu-id="91291-123">**visLockReplace**</span><span class="sxs-lookup"><span data-stu-id="91291-123">**visLockReplace**</span></span> <br/> |
   

