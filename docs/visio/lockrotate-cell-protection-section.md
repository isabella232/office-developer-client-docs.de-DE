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
description: Sperrt 2D-Shapes, damit sie nicht mit dem Drehpunkt oder den Befehlen Linksdrehung 90 Grad und Rechtsdrehung 90 Grad gedreht werden können.
ms.openlocfilehash: 36da1868e4f974bd19d00e86e31bea96eb8ad5bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404673"
---
# <a name="lockrotate-cell-protection-section"></a><span data-ttu-id="d6743-103">Zelle "LockRotate" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="d6743-103">LockRotate Cell (Protection Section)</span></span>

<span data-ttu-id="d6743-104">Sperrt 2D-Shapes, damit sie nicht mit dem Drehpunkt oder den Befehlen **Linksdrehung 90 Grad** und **Rechtsdrehung 90 Grad** gedreht werden können.</span><span class="sxs-lookup"><span data-stu-id="d6743-104">Locks 2-D shapes against being rotated with the rotation handle or the **Rotate Left 90°** or **Rotate Right 90°** command.</span></span> 
  
|<span data-ttu-id="d6743-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d6743-105">**Value**</span></span>|<span data-ttu-id="d6743-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6743-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d6743-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d6743-107">TRUE</span></span>  <br/> | <span data-ttu-id="d6743-108">Shape kann nicht gedreht werden.</span><span class="sxs-lookup"><span data-stu-id="d6743-108">Shape cannot be rotated.</span></span>  <br/> |
| <span data-ttu-id="d6743-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d6743-109">FALSE</span></span>  <br/> | <span data-ttu-id="d6743-110">Shape kann gedreht werden (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="d6743-110">Shape can be rotated (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6743-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d6743-111">Remarks</span></span>

<span data-ttu-id="d6743-p101">Die Zelle LockRotate verhindert nicht das Drehen eines 1D-Shapes, wenn an einem Endpunkt gezogen wird. Um ein 1D-Shape zu sperren, damit es nicht gedreht werden kann, legen Sie in der Zelle LockRotate einen Wert ungleich Null (TRUE) fest.</span><span class="sxs-lookup"><span data-stu-id="d6743-p101">The LockRotate cell does not prevent a 1-D shape from being rotated when an endpoint is dragged. To lock a 1-D shape against rotation, set the LockWidth cell to a non-zero value (TRUE).</span></span>
  
<span data-ttu-id="d6743-114">Um einen Verweis auf die Zelle LockRotate anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="d6743-114">To get a reference to the LockRotate cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d6743-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="d6743-115">Cell name:</span></span>  <br/> | <span data-ttu-id="d6743-116">LockRotate</span><span class="sxs-lookup"><span data-stu-id="d6743-116">LockRotate</span></span>  <br/> |
   
<span data-ttu-id="d6743-117">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LockRotate nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="d6743-117">To get a reference to the LockRotate cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d6743-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="d6743-118">Section index:</span></span>  <br/> |<span data-ttu-id="d6743-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d6743-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d6743-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d6743-120">Row index:</span></span>  <br/> |<span data-ttu-id="d6743-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="d6743-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="d6743-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d6743-122">Cell index:</span></span>  <br/> |<span data-ttu-id="d6743-123">**visLockRotate**</span><span class="sxs-lookup"><span data-stu-id="d6743-123">**visLockRotate**</span></span> <br/> |
   

