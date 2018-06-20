---
title: Zelle "LockWidth" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm675
localization_priority: Normal
ms.assetid: fef022ea-38ab-2b66-60c8-b94a6b0bdfbf
description: Sperrt die Breite des Shapes, sodass sich diese nicht ändert, wenn die Größe des Shapes geändert wird.
ms.openlocfilehash: abdcc0d5285e98e5856524925a41c4f72ee7f6ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797408"
---
# <a name="lockwidth-cell-protection-section"></a><span data-ttu-id="2ce1d-103">Zelle "LockWidth" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="2ce1d-103">LockWidth Cell (Protection Section)</span></span>

<span data-ttu-id="2ce1d-104">Sperrt die Breite des Shapes, sodass sich diese nicht ändert, wenn die Größe des Shapes geändert wird.</span><span class="sxs-lookup"><span data-stu-id="2ce1d-104">Locks the width of the shape so that its width remains unchanged when the shape is sized.</span></span>
  
|<span data-ttu-id="2ce1d-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2ce1d-105">**Value**</span></span>|<span data-ttu-id="2ce1d-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2ce1d-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2ce1d-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="2ce1d-107">TRUE</span></span>  <br/> | <span data-ttu-id="2ce1d-108">Breite ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="2ce1d-108">Width is locked.</span></span>  <br/> |
| <span data-ttu-id="2ce1d-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="2ce1d-109">FALSE</span></span>  <br/> | <span data-ttu-id="2ce1d-110">Breite ist nicht gesperrt.</span><span class="sxs-lookup"><span data-stu-id="2ce1d-110">Width is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ce1d-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2ce1d-111">Remarks</span></span>

<span data-ttu-id="2ce1d-112">Wenn Sie einen Verweis auf die Zelle LockWidth nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2ce1d-112">To get a reference to the LockWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2ce1d-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2ce1d-113">Cell name:</span></span>  <br/> | <span data-ttu-id="2ce1d-114">LockWidth</span><span class="sxs-lookup"><span data-stu-id="2ce1d-114">LockWidth</span></span>  <br/> |
   
<span data-ttu-id="2ce1d-115">Wenn Sie einen Verweis auf die Zelle LockWidth aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="2ce1d-115">To get a reference to the LockWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2ce1d-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2ce1d-116">Section index:</span></span>  <br/> |<span data-ttu-id="2ce1d-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2ce1d-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2ce1d-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2ce1d-118">Row index:</span></span>  <br/> |<span data-ttu-id="2ce1d-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="2ce1d-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="2ce1d-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="2ce1d-120">Cell index:</span></span>  <br/> |<span data-ttu-id="2ce1d-121">**visLockWidth**</span><span class="sxs-lookup"><span data-stu-id="2ce1d-121">**visLockWidth**</span></span> <br/> |
   

