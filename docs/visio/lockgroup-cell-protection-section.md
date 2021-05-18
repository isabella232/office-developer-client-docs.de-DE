---
title: Zelle "LockGroup" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251227
localization_priority: Normal
ms.assetid: 04b0fa5b-1680-cfe2-6aaf-0502ad196027
description: Sperrt eine Gruppe, damit die Gruppierung nicht aufgehoben werden kann.
ms.openlocfilehash: 0cb2c0653780dcb653e5903faaaa0ebf30ea9d69
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404309"
---
# <a name="lockgroup-cell-protection-section"></a><span data-ttu-id="f4b27-103">Zelle "LockGroup" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="f4b27-103">LockGroup Cell (Protection Section)</span></span>

<span data-ttu-id="f4b27-104">Sperrt eine Gruppe, damit die Gruppierung nicht aufgehoben werden kann.</span><span class="sxs-lookup"><span data-stu-id="f4b27-104">Locks a group so that it cannot be ungrouped.</span></span>
  
|<span data-ttu-id="f4b27-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="f4b27-105">**Value**</span></span>|<span data-ttu-id="f4b27-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f4b27-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f4b27-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="f4b27-107">TRUE</span></span>  <br/> |<span data-ttu-id="f4b27-108">Gruppierung der Gruppe kann nicht aufgehoben werden.</span><span class="sxs-lookup"><span data-stu-id="f4b27-108">Group cannot be ungrouped.</span></span>  <br/> |
|<span data-ttu-id="f4b27-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="f4b27-109">FALSE</span></span>  <br/> |<span data-ttu-id="f4b27-110">Gruppierung der Gruppe kann aufgehoben werden.</span><span class="sxs-lookup"><span data-stu-id="f4b27-110">Group can be ungrouped.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4b27-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f4b27-111">Remarks</span></span>

<span data-ttu-id="f4b27-112">Wenn Sie den Wert für LockGroupCell auf TRUE festlegen, wird auch das Löschen von Shapes verhindert, die Mitglieder der Gruppe sind.</span><span class="sxs-lookup"><span data-stu-id="f4b27-112">Setting the LockGroupCell value to TRUE also prevents deletion of any shapes that are members of the group.</span></span>
  
<span data-ttu-id="f4b27-113">Um einen Verweis auf die Zelle LockGroup anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="f4b27-113">To get a reference to the LockGroup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f4b27-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="f4b27-114">Cell name:</span></span>  <br/> |<span data-ttu-id="f4b27-115">LockGroup</span><span class="sxs-lookup"><span data-stu-id="f4b27-115">LockGroup</span></span>  <br/> |
   
<span data-ttu-id="f4b27-116">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LockGroup nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="f4b27-116">To get a reference to the LockGroup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f4b27-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="f4b27-117">Section index:</span></span>  <br/> |<span data-ttu-id="f4b27-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f4b27-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f4b27-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="f4b27-119">Row index:</span></span>  <br/> |<span data-ttu-id="f4b27-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="f4b27-120">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="f4b27-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="f4b27-121">Cell index:</span></span>  <br/> |<span data-ttu-id="f4b27-122">**visLockGroup**</span><span class="sxs-lookup"><span data-stu-id="f4b27-122">**visLockGroup**</span></span> <br/> |
   

