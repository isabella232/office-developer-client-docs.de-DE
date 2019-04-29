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
ms.openlocfilehash: 1703769fe54171a14f7052f0f6686e1eb5ec92fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417666"
---
# <a name="lockvtxedit-cell-protection-section"></a><span data-ttu-id="2b7be-103">Zelle "LockVtxEdit" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="2b7be-103">LockVtxEdit Cell (Protection Section)</span></span>

<span data-ttu-id="2b7be-104">Sperrt die Scheitelpunkte eines Shapes, sodass sie nicht bearbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="2b7be-104">Locks the vertices of a shape so that they cannot be edited.</span></span>
  
|<span data-ttu-id="2b7be-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2b7be-105">**Value**</span></span>|<span data-ttu-id="2b7be-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2b7be-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2b7be-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="2b7be-107">TRUE</span></span>  <br/> |<span data-ttu-id="2b7be-108">Scheitelpunkte können nicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="2b7be-108">Vertices cannot be edited.</span></span>  <br/> |
|<span data-ttu-id="2b7be-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="2b7be-109">FALSE</span></span>  <br/> |<span data-ttu-id="2b7be-110">Scheitelpunkte können bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="2b7be-110">Vertices can be edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b7be-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b7be-111">Remarks</span></span>

<span data-ttu-id="2b7be-112">Wenn Sie einen Verweis auf die Zelle Zelle LockVtxEdit aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2b7be-112">To get a reference to the LockVtxEdit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2b7be-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2b7be-113">Cell name:</span></span>  <br/> |<span data-ttu-id="2b7be-114">Zelle LockVtxEdit</span><span class="sxs-lookup"><span data-stu-id="2b7be-114">LockVtxEdit</span></span>  <br/> |
   
<span data-ttu-id="2b7be-115">Wenn Sie einen Verweis auf die Zelle Zelle LockVtxEdit aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="2b7be-115">To get a reference to the LockVtxEdit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2b7be-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2b7be-116">Section index:</span></span>  <br/> |<span data-ttu-id="2b7be-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2b7be-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="2b7be-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2b7be-118">Row index:</span></span>  <br/> |<span data-ttu-id="2b7be-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="2b7be-119">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="2b7be-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="2b7be-120">Cell index:</span></span>  <br/> |<span data-ttu-id="2b7be-121">**visLockVtxEdit**</span><span class="sxs-lookup"><span data-stu-id="2b7be-121">**visLockVtxEdit**</span></span> <br/> |
   

