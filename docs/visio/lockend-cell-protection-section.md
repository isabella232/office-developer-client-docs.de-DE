---
title: Zelle "LockEnd" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm620
localization_priority: Normal
ms.assetid: e9742142-4d34-1ba9-480e-d1ecff4fc7cd
description: Sperrt den Endpunkt (EndeX, EndeY) eines 1D-Shapes an einer bestimmten Position.
ms.openlocfilehash: d29f07e5b4b77ed2fb8b104769a2fdca55abcc8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797377"
---
# <a name="lockend-cell-protection-section"></a><span data-ttu-id="11a8f-103">Zelle "LockEnd" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="11a8f-103">LockEnd Cell (Protection Section)</span></span>

<span data-ttu-id="11a8f-104">Sperrt den Endpunkt (EndeX, EndeY) eines 1D-Shapes an einer bestimmten Position.</span><span class="sxs-lookup"><span data-stu-id="11a8f-104">Locks the endpoint (EndX, EndY) of a 1-D shape to a specific location.</span></span>
  
|<span data-ttu-id="11a8f-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="11a8f-105">**Value**</span></span>|<span data-ttu-id="11a8f-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="11a8f-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="11a8f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="11a8f-107">TRUE</span></span>  <br/> | <span data-ttu-id="11a8f-108">Endpunkt ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="11a8f-108">Endpoint is locked.</span></span>  <br/> |
| <span data-ttu-id="11a8f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="11a8f-109">FALSE</span></span>  <br/> | <span data-ttu-id="11a8f-110">Endpunkt ist nicht gesperrt.</span><span class="sxs-lookup"><span data-stu-id="11a8f-110">Endpoint is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11a8f-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="11a8f-111">Remarks</span></span>

<span data-ttu-id="11a8f-112">Wenn Sie einen Verweis auf die Zelle LockEnd nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="11a8f-112">To get a reference to the LockEnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="11a8f-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="11a8f-113">Cell name:</span></span>  <br/> | <span data-ttu-id="11a8f-114">LockEnd</span><span class="sxs-lookup"><span data-stu-id="11a8f-114">LockEnd</span></span>  <br/> |
   
<span data-ttu-id="11a8f-115">Wenn Sie einen Verweis auf die Zelle LockEnd aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="11a8f-115">To get a reference to the LockEnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="11a8f-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="11a8f-116">Section index:</span></span>  <br/> |<span data-ttu-id="11a8f-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="11a8f-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="11a8f-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="11a8f-118">Row index:</span></span>  <br/> |<span data-ttu-id="11a8f-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="11a8f-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="11a8f-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="11a8f-120">Cell index:</span></span>  <br/> |<span data-ttu-id="11a8f-121">**visLockEnd**</span><span class="sxs-lookup"><span data-stu-id="11a8f-121">**visLockEnd**</span></span> <br/> |
   

