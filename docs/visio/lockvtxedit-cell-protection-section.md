---
title: Zelle "LockVtxEdit" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251224
localization_priority: Normal
ms.assetid: 966cde5c-f04e-7149-3660-720ffa4f7079
description: Sperrt die Scheitelpunkte eines Shapes, sodass sie nicht bearbeitet werden können.
ms.openlocfilehash: 3766df62bb85e1470ad0fa46274b9bbbd96b8406
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19797416"
---
# <a name="lockvtxedit-cell-protection-section"></a><span data-ttu-id="3d8c6-103">LockVtxEdit Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="3d8c6-103">LockVtxEdit Cell (Protection Section)</span></span>

<span data-ttu-id="3d8c6-104">Sperrt die Scheitelpunkte eines Shapes, sodass sie nicht bearbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="3d8c6-104">Locks the vertices of a shape so that they cannot be edited.</span></span>
  
|<span data-ttu-id="3d8c6-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="3d8c6-105">**Value**</span></span>|<span data-ttu-id="3d8c6-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3d8c6-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3d8c6-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="3d8c6-107">TRUE</span></span>  <br/> |<span data-ttu-id="3d8c6-108">Scheitelpunkte können nicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="3d8c6-108">Vertices cannot be edited.</span></span>  <br/> |
|<span data-ttu-id="3d8c6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="3d8c6-109">FALSE</span></span>  <br/> |<span data-ttu-id="3d8c6-110">Scheitelpunkte können bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="3d8c6-110">Vertices can be edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d8c6-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d8c6-111">Remarks</span></span>

<span data-ttu-id="3d8c6-112">Wenn Sie einen Verweis auf die Zelle LockVtxEdit nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="3d8c6-112">To get a reference to the LockVtxEdit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3d8c6-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="3d8c6-113">Cell name:</span></span>  <br/> |<span data-ttu-id="3d8c6-114">LockVtxEdit</span><span class="sxs-lookup"><span data-stu-id="3d8c6-114">LockVtxEdit</span></span>  <br/> |
   
<span data-ttu-id="3d8c6-115">Wenn Sie einen Verweis auf die Zelle LockVtxEdit aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="3d8c6-115">To get a reference to the LockVtxEdit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3d8c6-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="3d8c6-116">Section index:</span></span>  <br/> |<span data-ttu-id="3d8c6-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3d8c6-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="3d8c6-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="3d8c6-118">Row index:</span></span>  <br/> |<span data-ttu-id="3d8c6-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="3d8c6-119">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="3d8c6-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="3d8c6-120">Cell index:</span></span>  <br/> |<span data-ttu-id="3d8c6-121">**visLockVtxEdit**</span><span class="sxs-lookup"><span data-stu-id="3d8c6-121">**visLockVtxEdit**</span></span> <br/> |
   

