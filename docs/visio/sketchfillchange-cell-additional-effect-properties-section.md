---
title: SketchFillChange Cell (Additional Effect Properties section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: Bestimmt die Menge der Zufallsgenerierung der Formfüllung aus der Geometrie der Form bei Verwendung eines Skizzen Effekts als Prozentsatz der Länge eines Abschnitts. Wenn der Wert der Zelle SketchFillChange auf 0% festgelegt ist, entspricht die umschließende Geometrie der Füllung einer Form der Geometrie der Form. Wenn der Wert 100% ist, folgt die begrenzungsgeometrie der Füllung der Form nicht der Geometrie der Form.
ms.openlocfilehash: 8726e9dd6ca6257fb8dbbbef3dce1d4ec344e28b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339812"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a><span data-ttu-id="649ec-105">SketchFillChange Cell (Additional Effect Properties section)</span><span class="sxs-lookup"><span data-stu-id="649ec-105">SketchFillChange Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="649ec-106">Bestimmt die Menge der Zufallsgenerierung der Formfüllung aus der Geometrie der Form bei Verwendung eines Skizzen Effekts als Prozentsatz der Länge eines Abschnitts.</span><span class="sxs-lookup"><span data-stu-id="649ec-106">Determines the amount of randomization of the shape's fill from the shape's geometry when using a sketch effect, as a percentage of the length of a section.</span></span> <span data-ttu-id="649ec-107">Wenn der Wert der Zelle **SketchFillChange** auf 0% festgelegt ist, entspricht die umschließende Geometrie der Füllung einer Form der Geometrie der Form.</span><span class="sxs-lookup"><span data-stu-id="649ec-107">If the value of the **SketchFillChange** cell is set to 0%, the bounding geometry of a shape's fill matches the shape's geometry.</span></span> <span data-ttu-id="649ec-108">Wenn der Wert 100% ist, folgt die begrenzungsgeometrie der Füllung der Form nicht der Geometrie der Form.</span><span class="sxs-lookup"><span data-stu-id="649ec-108">If the value is 100%, the bounding geometry of the shape's fill does not follow the geometry of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="649ec-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="649ec-109">Remarks</span></span>

<span data-ttu-id="649ec-110">Optimale Ergebnisse erzielen Sie, wenn der optimale Wert für die **SketchFillChange** -Zelle zwischen 15% und 50% liegt.</span><span class="sxs-lookup"><span data-stu-id="649ec-110">For best results, the ideal range of values for the **SketchFillChange** cell is between 15% and 50%.</span></span> <span data-ttu-id="649ec-111">Ein Wert unter 15% ist kaum spürbar; ein Wert größer als 50% wird zunehmend randomisiert.</span><span class="sxs-lookup"><span data-stu-id="649ec-111">A value below 15% is barely noticeable; a value greater than 50% is increasingly more randomized.</span></span> 
  
<span data-ttu-id="649ec-112">Wenn Sie einen Verweis auf die Zelle **SketchFillChange** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="649ec-112">To get a reference to the **SketchFillChange** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="649ec-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="649ec-113">Cell name:</span></span>  <br/> | <span data-ttu-id="649ec-114">SketchFillChange</span><span class="sxs-lookup"><span data-stu-id="649ec-114">SketchFillChange</span></span>  <br/> |
   
<span data-ttu-id="649ec-115">Wenn Sie einen Verweis auf die Zelle **SketchFillChange** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="649ec-115">To get a reference to the **SketchFillChange** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="649ec-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="649ec-116">Section index:</span></span>  <br/> |<span data-ttu-id="649ec-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="649ec-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="649ec-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="649ec-118">Row index:</span></span>  <br/> |<span data-ttu-id="649ec-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="649ec-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="649ec-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="649ec-120">Cell index:</span></span>  <br/> |<span data-ttu-id="649ec-121">**visSketchFillChange**</span><span class="sxs-lookup"><span data-stu-id="649ec-121">**visSketchFillChange**</span></span> <br/> |
   

