---
title: Zelle "LockCalcWH" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm605
localization_priority: Normal
ms.assetid: 6eb51e5a-03d8-3daa-b4e1-6107d540aed9
description: Sperrt das Auswahlrechteck eines Shapes, damit dieses nicht neu berechnet wird, wenn ein Scheitelpunkt bearbeitet oder ein Zeilentyp im Abschnitt Geometry geändert wird.
ms.openlocfilehash: f7f9c99eb4978e9b32968d3076b0341efe42faa6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797365"
---
# <a name="lockcalcwh-cell-protection-section"></a><span data-ttu-id="9d664-103">LockCalcWH Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="9d664-103">LockCalcWH Cell (Protection Section)</span></span>

<span data-ttu-id="9d664-104">Sperrt das Auswahlrechteck eines Shapes, damit dieses nicht neu berechnet wird, wenn ein Scheitelpunkt bearbeitet oder ein Zeilentyp im Abschnitt Geometry geändert wird.</span><span class="sxs-lookup"><span data-stu-id="9d664-104">Locks a shape's selection rectangle so it cannot be recalculated when a vertex is edited or a row type is changed in the Geometry section.</span></span>
  
|<span data-ttu-id="9d664-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9d664-105">**Value**</span></span>|<span data-ttu-id="9d664-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9d664-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="9d664-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="9d664-107">TRUE</span></span>  <br/> | <span data-ttu-id="9d664-108">Breite und Höhe können nicht neu berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="9d664-108">Width and height cannot be recalculated.</span></span>  <br/> |
| <span data-ttu-id="9d664-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="9d664-109">FALSE</span></span>  <br/> | <span data-ttu-id="9d664-110">Breite und Höhe können neu berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="9d664-110">Width and height can be recalculated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d664-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9d664-111">Remarks</span></span>

<span data-ttu-id="9d664-112">Wenn Sie einen Verweis auf die Zelle LockCalcWH aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9d664-112">To get a reference to the LockCalcWH cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9d664-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9d664-113">Cell name:</span></span>  <br/> | <span data-ttu-id="9d664-114">LockCalcWH</span><span class="sxs-lookup"><span data-stu-id="9d664-114">LockCalcWH</span></span>  <br/> |
   
<span data-ttu-id="9d664-115">Wenn Sie einen Verweis auf die Zelle LockCalcWH aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="9d664-115">To get a reference to the LockCalcWH cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9d664-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9d664-116">Section index:</span></span>  <br/> |<span data-ttu-id="9d664-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9d664-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9d664-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9d664-118">Row index:</span></span>  <br/> |<span data-ttu-id="9d664-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="9d664-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="9d664-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9d664-120">Cell index:</span></span>  <br/> |<span data-ttu-id="9d664-121">**visLockCalcWH**</span><span class="sxs-lookup"><span data-stu-id="9d664-121">**visLockCalcWH**</span></span> <br/> |
   

