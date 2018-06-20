---
title: SketchFillChange Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: Bestimmt die Menge der zufälligen Anordnung von der Füllung der Form aus der Shape-Geometrie an, wenn Sie einen Effekt Skizze als Prozentwert der Länge eines Abschnitts verwenden. Wenn der Wert der Zelle SketchFillChange auf 0 % festgelegt ist, entspricht die umgebende Geometrie Füllung einer Form der Shape-Geometrie. Ist der Wert auf 100 %, folgt die umgebende Geometrie der Füllung der Form die Geometrie des Shapes nicht.
ms.openlocfilehash: 8dda34e03188909e167a4abda6f62da3d43c4dd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798133"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a><span data-ttu-id="1e127-105">SketchFillChange Cell (Additional Effect Properties Section)</span><span class="sxs-lookup"><span data-stu-id="1e127-105">SketchFillChange Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="1e127-106">Bestimmt die Menge der zufälligen Anordnung von der Füllung der Form aus der Shape-Geometrie an, wenn Sie einen Effekt Skizze als Prozentwert der Länge eines Abschnitts verwenden.</span><span class="sxs-lookup"><span data-stu-id="1e127-106">Determines the amount of randomization of the shape's fill from the shape's geometry when using a sketch effect, as a percentage of the length of a section.</span></span> <span data-ttu-id="1e127-107">Wenn der Wert der Zelle **SketchFillChange** auf 0 % festgelegt ist, entspricht die umgebende Geometrie Füllung einer Form der Shape-Geometrie.</span><span class="sxs-lookup"><span data-stu-id="1e127-107">If the value of the **SketchFillChange** cell is set to 0%, the bounding geometry of a shape's fill matches the shape's geometry.</span></span> <span data-ttu-id="1e127-108">Ist der Wert auf 100 %, folgt die umgebende Geometrie der Füllung der Form die Geometrie des Shapes nicht.</span><span class="sxs-lookup"><span data-stu-id="1e127-108">If the value is 100%, the bounding geometry of the shape's fill does not follow the geometry of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1e127-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1e127-109">Remarks</span></span>

<span data-ttu-id="1e127-110">Die besten Ergebnisse zu erzielen ist ideale Wertebereich für die Zelle **SketchFillChange** zwischen 15 % und 50 %.</span><span class="sxs-lookup"><span data-stu-id="1e127-110">For best results, the ideal range of values for the **SketchFillChange** cell is between 15% and 50%.</span></span> <span data-ttu-id="1e127-111">Es wird ein Wert weniger als 15 % kaum Renderingzeit; ein Wert größer als 50 % ist immer mehr zufällige.</span><span class="sxs-lookup"><span data-stu-id="1e127-111">A value below 15% is barely noticeable; a value greater than 50% is increasingly more randomized.</span></span> 
  
<span data-ttu-id="1e127-112">Wenn Sie einen Verweis auf die Zelle **SketchFillChange** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1e127-112">To get a reference to the **SketchFillChange** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1e127-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="1e127-113">Cell name:</span></span>  <br/> | <span data-ttu-id="1e127-114">SketchFillChange</span><span class="sxs-lookup"><span data-stu-id="1e127-114">SketchFillChange</span></span>  <br/> |
   
<span data-ttu-id="1e127-115">Wenn Sie einen Verweis auf die Zelle **SketchFillChange** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="1e127-115">To get a reference to the **SketchFillChange** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1e127-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="1e127-116">Section index:</span></span>  <br/> |<span data-ttu-id="1e127-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1e127-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1e127-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="1e127-118">Row index:</span></span>  <br/> |<span data-ttu-id="1e127-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="1e127-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="1e127-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="1e127-120">Cell index:</span></span>  <br/> |<span data-ttu-id="1e127-121">**visSketchFillChange**</span><span class="sxs-lookup"><span data-stu-id="1e127-121">**visSketchFillChange**</span></span> <br/> |
   

