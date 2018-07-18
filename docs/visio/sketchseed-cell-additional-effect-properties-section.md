---
title: SketchSeed Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f62650d-36f8-4c6e-b79f-c9c397a5954d
description: Stellt einen zufällige Wert verwendet, um die Geometrie einer Skizze Auswirkung, wie eine positive ganze Zahl zu bestimmen. Der Wert der Zelle SketchSeed wird nach dem Zufallsprinzip erstellt, wenn eine Skizze Auswirkung auf die Form angewendet wird.
ms.openlocfilehash: 7c9d23e19da1a94bb37f1fc916e2f08095976d09
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798131"
---
# <a name="sketchseed-cell-additional-effect-properties-section"></a><span data-ttu-id="62e06-104">SketchSeed Cell (Additional Effect Properties Section)</span><span class="sxs-lookup"><span data-stu-id="62e06-104">SketchSeed Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="62e06-105">Stellt einen zufällige Wert verwendet, um die Geometrie einer Skizze Auswirkung, wie eine positive ganze Zahl zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="62e06-105">Represents a randomization value used to determine the geometry of a sketch effect, as a positive integer.</span></span> <span data-ttu-id="62e06-106">Der Wert der Zelle **SketchSeed** wird nach dem Zufallsprinzip erstellt, wenn eine Skizze Auswirkung auf die Form angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="62e06-106">The value of the **SketchSeed** cell is randomly created when a sketch effect is applied to the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="62e06-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62e06-107">Remarks</span></span>

<span data-ttu-id="62e06-108">Wenn Sie einen Verweis auf die Zelle **SketchSeed** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="62e06-108">To get a reference to the **SketchSeed** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="62e06-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="62e06-109">Cell name:</span></span>  <br/> | <span data-ttu-id="62e06-110">SketchSeed</span><span class="sxs-lookup"><span data-stu-id="62e06-110">SketchSeed</span></span>  <br/> |
   
<span data-ttu-id="62e06-111">Wenn Sie einen Verweis auf die Zelle **SketchSeed** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="62e06-111">To get a reference to the **SketchSeed** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="62e06-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="62e06-112">Section index:</span></span>  <br/> |<span data-ttu-id="62e06-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="62e06-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="62e06-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="62e06-114">Row index:</span></span>  <br/> |<span data-ttu-id="62e06-115">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="62e06-115">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="62e06-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="62e06-116">Cell index:</span></span>  <br/> |<span data-ttu-id="62e06-117">**visSketchSeed**</span><span class="sxs-lookup"><span data-stu-id="62e06-117">**visSketchSeed**</span></span> <br/> |
   

