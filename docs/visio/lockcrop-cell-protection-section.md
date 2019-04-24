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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359626"
---
# <a name="lockcrop-cell-protection-section"></a><span data-ttu-id="2289a-103">Zelle "LockCrop" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="2289a-103">LockCrop Cell (Protection Section)</span></span>

<span data-ttu-id="2289a-104">Sperrt ein Objekt aus einem anderen Programm, damit es nicht mithilfe des Zuschneidetools zugeschnitten werden kann.</span><span class="sxs-lookup"><span data-stu-id="2289a-104">Locks an object from another program against being cropped with the **Crop** tool.</span></span> 
  
|<span data-ttu-id="2289a-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2289a-105">**Value**</span></span>|<span data-ttu-id="2289a-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2289a-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2289a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="2289a-107">TRUE</span></span>  <br/> | <span data-ttu-id="2289a-108">Shape kann nicht zugeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="2289a-108">Shape cannot be cropped</span></span>  <br/> |
| <span data-ttu-id="2289a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="2289a-109">FALSE</span></span>  <br/> | <span data-ttu-id="2289a-110">Shape kann zugeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="2289a-110">Shape can be cropped.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2289a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2289a-111">Remarks</span></span>

<span data-ttu-id="2289a-112">Wenn Sie einen Verweis auf die Zelle Zelle LockCrop aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2289a-112">To get a reference to the LockCrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2289a-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2289a-113">Cell name:</span></span>  <br/> | <span data-ttu-id="2289a-114">Zelle LockCrop</span><span class="sxs-lookup"><span data-stu-id="2289a-114">LockCrop</span></span>  <br/> |
   
<span data-ttu-id="2289a-115">Wenn Sie einen Verweis auf die Zelle Zelle LockCrop aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="2289a-115">To get a reference to the LockCrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2289a-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2289a-116">Section index:</span></span>  <br/> |<span data-ttu-id="2289a-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2289a-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2289a-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2289a-118">Row index:</span></span>  <br/> |<span data-ttu-id="2289a-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="2289a-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="2289a-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="2289a-120">Cell index:</span></span>  <br/> |<span data-ttu-id="2289a-121">**visLockCrop**</span><span class="sxs-lookup"><span data-stu-id="2289a-121">**visLockCrop**</span></span> <br/> |
   

