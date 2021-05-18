---
title: Zelle "LockDelete" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251219
localization_priority: Normal
ms.assetid: 596c62b7-8d42-1854-d709-592db09a6a84
description: Sperrt das Shape, damit es nicht gelöscht werden kann.
ms.openlocfilehash: 0819969c9ba17a52de19341b359b33ceae5b44d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423139"
---
# <a name="lockdelete-cell-protection-section"></a><span data-ttu-id="2ae3f-103">Zelle "LockDelete" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="2ae3f-103">LockDelete Cell (Protection Section)</span></span>

<span data-ttu-id="2ae3f-104">Sperrt das Shape, damit es nicht gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="2ae3f-104">Locks the shape so that it cannot be deleted.</span></span>
  
|<span data-ttu-id="2ae3f-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2ae3f-105">**Value**</span></span>|<span data-ttu-id="2ae3f-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2ae3f-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2ae3f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="2ae3f-107">TRUE</span></span>  <br/> | <span data-ttu-id="2ae3f-108">Shape kann nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="2ae3f-108">Shape cannot be deleted</span></span>  <br/> |
| <span data-ttu-id="2ae3f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="2ae3f-109">FALSE</span></span>  <br/> | <span data-ttu-id="2ae3f-110">Shape kann gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="2ae3f-110">Shape can be deleted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ae3f-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2ae3f-111">Remarks</span></span>

<span data-ttu-id="2ae3f-112">Um einen Verweis auf die Zelle LockDelete anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="2ae3f-112">To get a reference to the LockDelete cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2ae3f-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2ae3f-113">Cell name:</span></span>  <br/> | <span data-ttu-id="2ae3f-114">LockDelete</span><span class="sxs-lookup"><span data-stu-id="2ae3f-114">LockDelete</span></span>  <br/> |
   
<span data-ttu-id="2ae3f-115">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LockDelete nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="2ae3f-115">To get a reference to the LockDelete cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2ae3f-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2ae3f-116">Section index:</span></span>  <br/> |<span data-ttu-id="2ae3f-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2ae3f-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2ae3f-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2ae3f-118">Row index:</span></span>  <br/> |<span data-ttu-id="2ae3f-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="2ae3f-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="2ae3f-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="2ae3f-120">Cell index:</span></span>  <br/> |<span data-ttu-id="2ae3f-121">**visLockDelete**</span><span class="sxs-lookup"><span data-stu-id="2ae3f-121">**visLockDelete**</span></span> <br/> |
   

