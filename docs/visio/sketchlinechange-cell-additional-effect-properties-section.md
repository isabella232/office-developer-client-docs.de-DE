---
title: SketchLineChange Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 39192535-b55b-4c49-b63f-edb542c7a2e5
description: Bestimmt die Menge der zufällige Zeile aus der Shape-Geometrie des Shapes an, wenn ein Effekt Skizze als Prozentwert der Länge eines Abschnitts mit. Wenn der Wert der Zelle SketchLineChange auf 0 % festgelegt ist, entspricht die Geometrie des Shapes Zeile der Shape-Geometrie. Ist der Wert auf 100 %, folgt die Geometrie Zeile des Shapes nicht die Geometrie des Shapes.
ms.openlocfilehash: 57d2af1a914710d7e5a58686b577014ceb7af424
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798128"
---
# <a name="sketchlinechange-cell-additional-effect-properties-section"></a><span data-ttu-id="b128f-105">SketchLineChange Cell (Additional Effect Properties Section)</span><span class="sxs-lookup"><span data-stu-id="b128f-105">SketchLineChange Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="b128f-106">Bestimmt die Menge der zufällige Zeile aus der Shape-Geometrie des Shapes an, wenn ein Effekt Skizze als Prozentwert der Länge eines Abschnitts mit.</span><span class="sxs-lookup"><span data-stu-id="b128f-106">Determines the amount of randomization of the shape's line from the shape's geometry when using a sketch effect, as a percentage of the length of a section.</span></span> <span data-ttu-id="b128f-107">Wenn der Wert der Zelle **SketchLineChange** auf 0 % festgelegt ist, entspricht die Geometrie des Shapes Zeile der Shape-Geometrie.</span><span class="sxs-lookup"><span data-stu-id="b128f-107">If the value of the **SketchLineChange** cell is set to 0%, the geometry of the shape's line matches the shape's geometry.</span></span> <span data-ttu-id="b128f-108">Ist der Wert auf 100 %, folgt die Geometrie Zeile des Shapes nicht die Geometrie des Shapes.</span><span class="sxs-lookup"><span data-stu-id="b128f-108">If the value is 100%, the geometry of the shape's line does not follow the geometry of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b128f-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b128f-109">Remarks</span></span>

<span data-ttu-id="b128f-110">Die besten Ergebnisse zu erzielen ist ideale Wertebereich für die Zelle **SketchLineChange** zwischen 15 % und 50 %.</span><span class="sxs-lookup"><span data-stu-id="b128f-110">For best results, the ideal range of values for the **SketchLineChange** cell is between 15% and 50%.</span></span> <span data-ttu-id="b128f-111">Es wird ein Wert weniger als 15 % kaum Renderingzeit; ein Wert größer als 50 % die Zeile zu viel randomize konnte.</span><span class="sxs-lookup"><span data-stu-id="b128f-111">A value below 15% is barely noticeable; a value greater than 50% could randomize the line too much.</span></span> 
  
<span data-ttu-id="b128f-112">Wenn Sie einen Verweis auf die Zelle **SketchLineChange** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b128f-112">To get a reference to the **SketchLineChange** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b128f-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b128f-113">Cell name:</span></span>  <br/> | <span data-ttu-id="b128f-114">SketchLineChange</span><span class="sxs-lookup"><span data-stu-id="b128f-114">SketchLineChange</span></span>  <br/> |
   
<span data-ttu-id="b128f-115">Wenn Sie einen Verweis auf die Zelle **SketchLineChange** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="b128f-115">To get a reference to the **SketchLineChange** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b128f-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b128f-116">Section index:</span></span>  <br/> |<span data-ttu-id="b128f-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b128f-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b128f-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b128f-118">Row index:</span></span>  <br/> |<span data-ttu-id="b128f-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="b128f-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="b128f-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b128f-120">Cell index:</span></span>  <br/> |<span data-ttu-id="b128f-121">**visSketchLineChange**</span><span class="sxs-lookup"><span data-stu-id="b128f-121">**visSketchLineChange**</span></span> <br/> |
   

