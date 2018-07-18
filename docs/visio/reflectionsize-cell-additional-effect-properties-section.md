---
title: ReflectionSize Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7dfeb78e-a0fa-4492-b35f-70b1e2975d38
description: Bestimmt die Größe des Reflektions relativ zum Shape, als Prozentwert von 0,0 und 100,0 %. Eine Form mit einem Wert von 0 % in der Zelle ReflectionSize ist eine Spiegelung nicht mit. ein Wert von 100 % zeigt ein vollständiges Spiegelbild der Form.
ms.openlocfilehash: b525a5f7379b2702dd7152d4eccf6dab1879a6cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797788"
---
# <a name="reflectionsize-cell-additional-effect-properties-section"></a><span data-ttu-id="6a1bd-104">ReflectionSize Cell (Additional Effect Properties Section)</span><span class="sxs-lookup"><span data-stu-id="6a1bd-104">ReflectionSize Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="6a1bd-105">Bestimmt die Größe des Reflektions relativ zum Shape, als Prozentwert von 0,0 und 100,0 %.</span><span class="sxs-lookup"><span data-stu-id="6a1bd-105">Determines the size of the reflection relative to the shape, as a percentage from 0.0 to 100.0%.</span></span> <span data-ttu-id="6a1bd-106">Eine Form mit einem Wert von 0 % in der Zelle **ReflectionSize** ist eine Spiegelung nicht mit. ein Wert von 100 % zeigt ein vollständiges Spiegelbild der Form.</span><span class="sxs-lookup"><span data-stu-id="6a1bd-106">A shape with a value of 0% in the **ReflectionSize** cell does not have a reflection; a value of 100% displays a complete mirror image of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6a1bd-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a1bd-107">Remarks</span></span>

<span data-ttu-id="6a1bd-108">Wenn Sie einen Verweis auf die Zelle **ReflectionSize** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6a1bd-108">To get a reference to the **ReflectionSize** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6a1bd-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="6a1bd-109">Cell name:</span></span>  <br/> | <span data-ttu-id="6a1bd-110">ReflectionSize</span><span class="sxs-lookup"><span data-stu-id="6a1bd-110">ReflectionSize</span></span>  <br/> |
   
<span data-ttu-id="6a1bd-111">Wenn Sie einen Verweis auf die Zelle **ReflectionSize** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="6a1bd-111">To get a reference to the **ReflectionSize** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6a1bd-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="6a1bd-112">Section index:</span></span>  <br/> |<span data-ttu-id="6a1bd-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6a1bd-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6a1bd-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="6a1bd-114">Row index:</span></span>  <br/> |<span data-ttu-id="6a1bd-115">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="6a1bd-115">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="6a1bd-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="6a1bd-116">Cell index:</span></span>  <br/> |<span data-ttu-id="6a1bd-117">**visReflectionSize**</span><span class="sxs-lookup"><span data-stu-id="6a1bd-117">**visReflectionSize**</span></span> <br/> |
   

