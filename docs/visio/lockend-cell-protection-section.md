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
ms.openlocfilehash: d9fe0372c44fe3b029a4d06056c8d3871c3f91e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425582"
---
# <a name="lockend-cell-protection-section"></a><span data-ttu-id="34a66-103">Zelle "LockEnd" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="34a66-103">LockEnd Cell (Protection Section)</span></span>

<span data-ttu-id="34a66-104">Sperrt den Endpunkt (EndeX, EndeY) eines 1D-Shapes an einer bestimmten Position.</span><span class="sxs-lookup"><span data-stu-id="34a66-104">Locks the endpoint (EndX, EndY) of a 1-D shape to a specific location.</span></span>
  
|<span data-ttu-id="34a66-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="34a66-105">**Value**</span></span>|<span data-ttu-id="34a66-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="34a66-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="34a66-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="34a66-107">TRUE</span></span>  <br/> | <span data-ttu-id="34a66-108">Endpunkt ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="34a66-108">Endpoint is locked.</span></span>  <br/> |
| <span data-ttu-id="34a66-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="34a66-109">FALSE</span></span>  <br/> | <span data-ttu-id="34a66-110">Endpunkt ist nicht gesperrt.</span><span class="sxs-lookup"><span data-stu-id="34a66-110">Endpoint is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="34a66-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="34a66-111">Remarks</span></span>

<span data-ttu-id="34a66-112">Verwenden Sie zum Erhalten eines Verweises auf die Zelle LockEnd anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="34a66-112">To get a reference to the LockEnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="34a66-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="34a66-113">Cell name:</span></span>  <br/> | <span data-ttu-id="34a66-114">LockEnd</span><span class="sxs-lookup"><span data-stu-id="34a66-114">LockEnd</span></span>  <br/> |
   
<span data-ttu-id="34a66-115">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die LockEnd-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="34a66-115">To get a reference to the LockEnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="34a66-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="34a66-116">Section index:</span></span>  <br/> |<span data-ttu-id="34a66-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="34a66-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="34a66-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="34a66-118">Row index:</span></span>  <br/> |<span data-ttu-id="34a66-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="34a66-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="34a66-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="34a66-120">Cell index:</span></span>  <br/> |<span data-ttu-id="34a66-121">**visLockEnd**</span><span class="sxs-lookup"><span data-stu-id="34a66-121">**visLockEnd**</span></span> <br/> |
   

