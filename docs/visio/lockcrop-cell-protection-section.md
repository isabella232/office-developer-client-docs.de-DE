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
ms.openlocfilehash: d7f231d5dcb022548477e0817c9d408a8d1b86ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797371"
---
# <a name="lockcrop-cell-protection-section"></a><span data-ttu-id="a5a95-103">LockCrop Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="a5a95-103">LockCrop Cell (Protection Section)</span></span>

<span data-ttu-id="a5a95-104">Sperrt ein Objekt aus einem anderen Programm, damit es mithilfe **des Zuschneidetools** zugeschnitten.</span><span class="sxs-lookup"><span data-stu-id="a5a95-104">Locks an object from another program against being cropped with the **Crop** tool.</span></span> 
  
|<span data-ttu-id="a5a95-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a5a95-105">**Value**</span></span>|<span data-ttu-id="a5a95-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a5a95-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a5a95-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a5a95-107">TRUE</span></span>  <br/> | <span data-ttu-id="a5a95-108">Shape kann nicht zugeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="a5a95-108">Shape cannot be cropped</span></span>  <br/> |
| <span data-ttu-id="a5a95-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a5a95-109">FALSE</span></span>  <br/> | <span data-ttu-id="a5a95-110">Shape kann zugeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="a5a95-110">Shape can be cropped.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5a95-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a5a95-111">Remarks</span></span>

<span data-ttu-id="a5a95-112">Wenn Sie einen Verweis auf die Zelle LockCrop aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a5a95-112">To get a reference to the LockCrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a5a95-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a5a95-113">Cell name:</span></span>  <br/> | <span data-ttu-id="a5a95-114">LockCrop</span><span class="sxs-lookup"><span data-stu-id="a5a95-114">LockCrop</span></span>  <br/> |
   
<span data-ttu-id="a5a95-115">Wenn Sie einen Verweis auf die Zelle LockCrop aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a5a95-115">To get a reference to the LockCrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a5a95-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a5a95-116">Section index:</span></span>  <br/> |<span data-ttu-id="a5a95-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a5a95-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a5a95-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a5a95-118">Row index:</span></span>  <br/> |<span data-ttu-id="a5a95-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="a5a95-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="a5a95-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a5a95-120">Cell index:</span></span>  <br/> |<span data-ttu-id="a5a95-121">**visLockCrop**</span><span class="sxs-lookup"><span data-stu-id="a5a95-121">**visLockCrop**</span></span> <br/> |
   

