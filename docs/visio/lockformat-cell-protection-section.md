---
title: Zelle "LockFormat" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm625
localization_priority: Normal
ms.assetid: e9a640f4-0af0-317c-b77b-f32c651e87b4
description: Sperrt die Formatierung eines Shapes, damit dieses nicht geändert werden kann.
ms.openlocfilehash: e0d1bb8a65b8087136e57bb46ad9f5363da30030
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359613"
---
# <a name="lockformat-cell-protection-section"></a><span data-ttu-id="444f8-103">Zelle "LockFormat" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="444f8-103">LockFormat Cell (Protection Section)</span></span>

<span data-ttu-id="444f8-104">Sperrt die Formatierung eines Shapes, damit dieses nicht geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="444f8-104">Locks the formatting of a shape so it cannot be changed.</span></span>
  
|<span data-ttu-id="444f8-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="444f8-105">**Value**</span></span>|<span data-ttu-id="444f8-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="444f8-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="444f8-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="444f8-107">TRUE</span></span>  <br/> | <span data-ttu-id="444f8-108">Formatierung kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="444f8-108">Formatting cannot be changed.</span></span>  <br/> |
| <span data-ttu-id="444f8-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="444f8-109">FALSE</span></span>  <br/> | <span data-ttu-id="444f8-110">Formatierung kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="444f8-110">Formatting can be changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="444f8-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="444f8-111">Remarks</span></span>

<span data-ttu-id="444f8-112">Wenn Sie einen Verweis auf die Zelle "Lock Format aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="444f8-112">To get a reference to the LockFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="444f8-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="444f8-113">Cell name:</span></span>  <br/> | <span data-ttu-id="444f8-114">"Lock Format</span><span class="sxs-lookup"><span data-stu-id="444f8-114">LockFormat</span></span>  <br/> |
   
<span data-ttu-id="444f8-115">Wenn Sie einen Verweis auf die Zelle "Lock Format aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="444f8-115">To get a reference to the LockFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="444f8-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="444f8-116">Section index:</span></span>  <br/> |<span data-ttu-id="444f8-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="444f8-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="444f8-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="444f8-118">Row index:</span></span>  <br/> |<span data-ttu-id="444f8-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="444f8-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="444f8-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="444f8-120">Cell index:</span></span>  <br/> |<span data-ttu-id="444f8-121">**visLockFormat**</span><span class="sxs-lookup"><span data-stu-id="444f8-121">**visLockFormat**</span></span> <br/> |
   

