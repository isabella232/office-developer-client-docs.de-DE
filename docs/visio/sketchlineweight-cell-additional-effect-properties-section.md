---
title: SketchLineWeight Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cb838be-1d6d-48e1-8e9e-bd126f0c2385
description: Bestimmt die zusätzliche Stärke als Ergebnis einer Skizze Wirkung in Punkt im Bereich von 0 bis 50 Linienbreite hinzugefügt. Die Stärke der Linie ein Shape wird als der Wert der Zelle erhöht SketchLineWeight erhöht.
ms.openlocfilehash: 9ab99faab907ddf0d944abbeea39672906b4c03d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798145"
---
# <a name="sketchlineweight-cell-additional-effect-properties-section"></a><span data-ttu-id="516cd-104">SketchLineWeight Cell (Additional Effect Properties Section)</span><span class="sxs-lookup"><span data-stu-id="516cd-104">SketchLineWeight Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="516cd-105">Bestimmt die zusätzliche Stärke als Ergebnis einer Skizze Wirkung in Punkt im Bereich von 0 bis 50 Linienbreite hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="516cd-105">Determines the additional thickness added to line weight as the result of a sketch effect, in points from 0 to 50.</span></span> <span data-ttu-id="516cd-106">Die Stärke der Linie ein Shape erhöht als Wert des **SketchLineWeight** Zelle erhöht.</span><span class="sxs-lookup"><span data-stu-id="516cd-106">The thickness of a shape's line increases as the value of the **SketchLineWeight** cell increases.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="516cd-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="516cd-107">Remarks</span></span>

<span data-ttu-id="516cd-108">Wenn Sie einen Verweis auf die Zelle **SketchLineWeight** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="516cd-108">To get a reference to the **SketchLineWeight** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="516cd-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="516cd-109">Cell name:</span></span>  <br/> | <span data-ttu-id="516cd-110">SketchLineWeight</span><span class="sxs-lookup"><span data-stu-id="516cd-110">SketchLineWeight</span></span>  <br/> |
   
<span data-ttu-id="516cd-111">Wenn Sie einen Verweis auf die Zelle **SketchLineWeight** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="516cd-111">To get a reference to the **SketchLineWeight** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="516cd-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="516cd-112">Section index:</span></span>  <br/> |<span data-ttu-id="516cd-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="516cd-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="516cd-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="516cd-114">Row index:</span></span>  <br/> |<span data-ttu-id="516cd-115">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="516cd-115">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="516cd-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="516cd-116">Cell index:</span></span>  <br/> |<span data-ttu-id="516cd-117">**visSketchLineWeight**</span><span class="sxs-lookup"><span data-stu-id="516cd-117">**visSketchLineWeight**</span></span> <br/> |
   

