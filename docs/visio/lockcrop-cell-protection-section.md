---
title: Zelle "LockCrop" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm610
localization_priority: Normal
ms.assetid: ae05de63-b527-66e6-2c79-056c9c92ec95
description: Sperrt ein Objekt aus einem anderen Programm, damit es nicht mithilfe des Zuschneidetools zugeschnitten werden kann.
ms.openlocfilehash: bfb8bebd50908387fa3f94a8ca228935ef709133
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411855"
---
# <a name="lockcrop-cell-protection-section"></a><span data-ttu-id="fdca6-103">Zelle "LockCrop" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="fdca6-103">LockCrop Cell (Protection Section)</span></span>

<span data-ttu-id="fdca6-104">Sperrt ein Objekt aus einem anderen Programm, damit es nicht mithilfe des Zuschneidetools zugeschnitten werden kann.</span><span class="sxs-lookup"><span data-stu-id="fdca6-104">Locks an object from another program against being cropped with the **Crop** tool.</span></span> 
  
|<span data-ttu-id="fdca6-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="fdca6-105">**Value**</span></span>|<span data-ttu-id="fdca6-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fdca6-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="fdca6-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="fdca6-107">TRUE</span></span>  <br/> | <span data-ttu-id="fdca6-108">Shape kann nicht zugeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="fdca6-108">Shape cannot be cropped</span></span>  <br/> |
| <span data-ttu-id="fdca6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="fdca6-109">FALSE</span></span>  <br/> | <span data-ttu-id="fdca6-110">Shape kann zugeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="fdca6-110">Shape can be cropped.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fdca6-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fdca6-111">Remarks</span></span>

<span data-ttu-id="fdca6-112">Um einen Verweis auf die Zelle LockCrop anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="fdca6-112">To get a reference to the LockCrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fdca6-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="fdca6-113">Cell name:</span></span>  <br/> | <span data-ttu-id="fdca6-114">LockCrop</span><span class="sxs-lookup"><span data-stu-id="fdca6-114">LockCrop</span></span>  <br/> |
   
<span data-ttu-id="fdca6-115">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die LockCrop-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="fdca6-115">To get a reference to the LockCrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fdca6-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="fdca6-116">Section index:</span></span>  <br/> |<span data-ttu-id="fdca6-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fdca6-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fdca6-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="fdca6-118">Row index:</span></span>  <br/> |<span data-ttu-id="fdca6-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="fdca6-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="fdca6-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="fdca6-120">Cell index:</span></span>  <br/> |<span data-ttu-id="fdca6-121">**visLockCrop**</span><span class="sxs-lookup"><span data-stu-id="fdca6-121">**visLockCrop**</span></span> <br/> |
   

