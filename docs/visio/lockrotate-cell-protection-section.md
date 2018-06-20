---
title: Zelle "LockRotate" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm655
localization_priority: Normal
ms.assetid: 2d97b31d-9008-307d-273a-1726007eeb34
description: Sperrt 2D-Shapes, damit Sie mit dem Drehpunkt oder nach links drehen gedreht 90° oder Rechtsdrehung 90°-Befehl.
ms.openlocfilehash: 450fe4786594472d018b705df4678fe636390ac3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797392"
---
# <a name="lockrotate-cell-protection-section"></a><span data-ttu-id="23382-103">LockRotate Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="23382-103">LockRotate Cell (Protection Section)</span></span>

<span data-ttu-id="23382-104">Sperrt 2D-Shapes gegen mit dem Drehpunkt oder den **Rechtsdrehung linken 90 Grad** oder Befehl **Rechtsdrehung 90 Grad** gedreht werden.</span><span class="sxs-lookup"><span data-stu-id="23382-104">Locks 2-D shapes against being rotated with the rotation handle or the **Rotate Left 90°** or **Rotate Right 90°** command.</span></span> 
  
|<span data-ttu-id="23382-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="23382-105">**Value**</span></span>|<span data-ttu-id="23382-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="23382-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="23382-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="23382-107">TRUE</span></span>  <br/> | <span data-ttu-id="23382-108">Shape kann nicht gedreht werden.</span><span class="sxs-lookup"><span data-stu-id="23382-108">Shape cannot be rotated.</span></span>  <br/> |
| <span data-ttu-id="23382-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="23382-109">FALSE</span></span>  <br/> | <span data-ttu-id="23382-110">Shape kann gedreht werden (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="23382-110">Shape can be rotated (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23382-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="23382-111">Remarks</span></span>

<span data-ttu-id="23382-p101">Die Zelle LockRotate verhindert nicht das Drehen eines 1D-Shapes, wenn an einem Endpunkt gezogen wird. Um ein 1D-Shape zu sperren, damit es nicht gedreht werden kann, legen Sie in der Zelle LockRotate einen Wert ungleich Null (TRUE) fest.</span><span class="sxs-lookup"><span data-stu-id="23382-p101">The LockRotate cell does not prevent a 1-D shape from being rotated when an endpoint is dragged. To lock a 1-D shape against rotation, set the LockWidth cell to a non-zero value (TRUE).</span></span>
  
<span data-ttu-id="23382-114">Wenn Sie einen Verweis auf die Zelle LockRotate nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="23382-114">To get a reference to the LockRotate cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="23382-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="23382-115">Cell name:</span></span>  <br/> | <span data-ttu-id="23382-116">LockRotate</span><span class="sxs-lookup"><span data-stu-id="23382-116">LockRotate</span></span>  <br/> |
   
<span data-ttu-id="23382-117">Wenn Sie einen Verweis auf die Zelle LockRotate aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="23382-117">To get a reference to the LockRotate cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="23382-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="23382-118">Section index:</span></span>  <br/> |<span data-ttu-id="23382-119">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="23382-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="23382-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="23382-120">Row index:</span></span>  <br/> |<span data-ttu-id="23382-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="23382-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="23382-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="23382-122">Cell index:</span></span>  <br/> |<span data-ttu-id="23382-123">**visLockRotate**</span><span class="sxs-lookup"><span data-stu-id="23382-123">**visLockRotate**</span></span> <br/> |
   

