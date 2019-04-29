---
title: SketchLineChange Cell (Additional Effect Properties section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 39192535-b55b-4c49-b63f-edb542c7a2e5
description: Bestimmt den Grad der Zufallsgenerierung der Linie der Form aus der Geometrie der Form bei Verwendung eines Skizzen Effekts als Prozentsatz der Länge eines Abschnitts. Wenn der Wert der Zelle SketchLineChange auf 0% festgelegt ist, stimmt die Geometrie der Formlinie mit der Geometrie der Form überein. Wenn der Wert 100% ist, folgt die Geometrie der Formlinie nicht der Geometrie der Form.
ms.openlocfilehash: ba57a4d2e43a91475f4c3ab4862f723eb2653a89
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419506"
---
# <a name="sketchlinechange-cell-additional-effect-properties-section"></a><span data-ttu-id="e8edf-105">SketchLineChange Cell (Additional Effect Properties section)</span><span class="sxs-lookup"><span data-stu-id="e8edf-105">SketchLineChange Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="e8edf-106">Bestimmt den Grad der Zufallsgenerierung der Linie der Form aus der Geometrie der Form bei Verwendung eines Skizzen Effekts als Prozentsatz der Länge eines Abschnitts.</span><span class="sxs-lookup"><span data-stu-id="e8edf-106">Determines the amount of randomization of the shape's line from the shape's geometry when using a sketch effect, as a percentage of the length of a section.</span></span> <span data-ttu-id="e8edf-107">Wenn der Wert der Zelle **SketchLineChange** auf 0% festgelegt ist, stimmt die Geometrie der Formlinie mit der Geometrie der Form überein.</span><span class="sxs-lookup"><span data-stu-id="e8edf-107">If the value of the **SketchLineChange** cell is set to 0%, the geometry of the shape's line matches the shape's geometry.</span></span> <span data-ttu-id="e8edf-108">Wenn der Wert 100% ist, folgt die Geometrie der Formlinie nicht der Geometrie der Form.</span><span class="sxs-lookup"><span data-stu-id="e8edf-108">If the value is 100%, the geometry of the shape's line does not follow the geometry of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e8edf-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8edf-109">Remarks</span></span>

<span data-ttu-id="e8edf-110">Optimale Ergebnisse erzielen Sie, wenn der optimale Wert für die **SketchLineChange** -Zelle zwischen 15% und 50% liegt.</span><span class="sxs-lookup"><span data-stu-id="e8edf-110">For best results, the ideal range of values for the **SketchLineChange** cell is between 15% and 50%.</span></span> <span data-ttu-id="e8edf-111">Ein Wert unter 15% ist kaum spürbar; ein Wert, der größer als 50% ist, kann die Leitung zu stark randomizen.</span><span class="sxs-lookup"><span data-stu-id="e8edf-111">A value below 15% is barely noticeable; a value greater than 50% could randomize the line too much.</span></span> 
  
<span data-ttu-id="e8edf-112">Wenn Sie einen Verweis auf die Zelle **SketchLineChange** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e8edf-112">To get a reference to the **SketchLineChange** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e8edf-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="e8edf-113">Cell name:</span></span>  <br/> | <span data-ttu-id="e8edf-114">SketchLineChange</span><span class="sxs-lookup"><span data-stu-id="e8edf-114">SketchLineChange</span></span>  <br/> |
   
<span data-ttu-id="e8edf-115">Wenn Sie einen Verweis auf die Zelle **SketchLineChange** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="e8edf-115">To get a reference to the **SketchLineChange** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e8edf-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="e8edf-116">Section index:</span></span>  <br/> |<span data-ttu-id="e8edf-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e8edf-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e8edf-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="e8edf-118">Row index:</span></span>  <br/> |<span data-ttu-id="e8edf-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="e8edf-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="e8edf-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="e8edf-120">Cell index:</span></span>  <br/> |<span data-ttu-id="e8edf-121">**visSketchLineChange**</span><span class="sxs-lookup"><span data-stu-id="e8edf-121">**visSketchLineChange**</span></span> <br/> |
   

