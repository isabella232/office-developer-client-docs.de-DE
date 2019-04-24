---
title: LockReplace Cell (Protection section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b3880511-dd27-4dc2-9e50-a49084ef8195
description: Gibt an, ob ein Shape an einem Ersetzungsvorgang (als Ziel-oder als Ersatz-Shape) teilnehmen kann.
ms.openlocfilehash: 8b0e3175cacd9b906d91a4185dcd98fad604d8bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348223"
---
# <a name="lockreplace-cell-protection-section"></a><span data-ttu-id="a2a9a-103">LockReplace Cell (Protection section)</span><span class="sxs-lookup"><span data-stu-id="a2a9a-103">LockReplace Cell (Protection Section)</span></span>

<span data-ttu-id="a2a9a-104">Gibt an, ob ein Shape an einem Ersetzungsvorgang (als Ziel-oder als Ersatz-Shape) teilnehmen kann.</span><span class="sxs-lookup"><span data-stu-id="a2a9a-104">Indicates whether a shape can participate in a replacement operation (as either a target or a replacement shape).</span></span> 
  
|<span data-ttu-id="a2a9a-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a2a9a-105">**Value**</span></span>|<span data-ttu-id="a2a9a-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a2a9a-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a2a9a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a2a9a-107">TRUE</span></span>  <br/> |<span data-ttu-id="a2a9a-108">Das Shape kann nicht ersetzt oder als Ersatzform verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a2a9a-108">The shape cannot be replaced or be used as a replacement shape.</span></span>  <br/> <span data-ttu-id="a2a9a-109">Bei einem Shape auf dem Canvas ist die Schaltfläche **Shape ändern** deaktiviert, wenn das Shape ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="a2a9a-109">For a shape on the canvas, the **Change Shape** button is disabled when the shape is selected.</span></span>  <br/> <span data-ttu-id="a2a9a-110">Bei einem Shape auf einer Schablone wird das Shape nicht als Ersatzform angezeigt, wenn auf die Schaltfläche **Shape ändern** geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="a2a9a-110">For a shape on a stencil, the shape does not appear as a replacement shape when the **Change Shape** button is clicked.</span></span>  <br/> |
|<span data-ttu-id="a2a9a-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="a2a9a-111">FALSE</span></span>  <br/> |<span data-ttu-id="a2a9a-112">Die Form kann ersetzt oder als Ersatzform verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a2a9a-112">The shape can be replaced or used as a replacement shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a2a9a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2a9a-113">Remarks</span></span>

<span data-ttu-id="a2a9a-114">Wenn Sie einen Verweis auf die Zelle **LockReplace** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a2a9a-114">To get a reference to the **LockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a2a9a-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a2a9a-115">Cell name:</span></span>  <br/> | <span data-ttu-id="a2a9a-116">LockReplace</span><span class="sxs-lookup"><span data-stu-id="a2a9a-116">LockReplace</span></span>  <br/> |
   
<span data-ttu-id="a2a9a-117">Wenn Sie einen Verweis auf die Zelle **LockReplace** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a2a9a-117">To get a reference to the **LockReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a2a9a-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a2a9a-118">Section index:</span></span>  <br/> |<span data-ttu-id="a2a9a-119">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a2a9a-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a2a9a-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a2a9a-120">Row index:</span></span>  <br/> |<span data-ttu-id="a2a9a-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="a2a9a-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="a2a9a-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a2a9a-122">Cell index:</span></span>  <br/> |<span data-ttu-id="a2a9a-123">**visLockReplace**</span><span class="sxs-lookup"><span data-stu-id="a2a9a-123">**visLockReplace**</span></span> <br/> |
   

