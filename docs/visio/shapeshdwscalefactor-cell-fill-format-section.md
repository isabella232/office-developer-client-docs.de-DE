---
title: Zelle "ShapeShdwScaleFactor" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033175
localization_priority: Normal
ms.assetid: 94ec06c5-8d2f-dd27-1eed-1abaf93daba8
description: Gibt den Prozentsatz an, um den der Schatten eines Shapes vergrößert oder verkleinert werden kann.
ms.openlocfilehash: 0b6392030e7efc8ea36c8d728b99c9b82482840b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798061"
---
# <a name="shapeshdwscalefactor-cell-fill-format-section"></a><span data-ttu-id="6c7ee-103">ShapeShdwScaleFactor Cell (Fill Format Section)</span><span class="sxs-lookup"><span data-stu-id="6c7ee-103">ShapeShdwScaleFactor Cell (Fill Format Section)</span></span>

<span data-ttu-id="6c7ee-104">Gibt den Prozentsatz an, um den der Schatten eines Shapes vergrößert oder verkleinert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6c7ee-104">Specifies the percentage by which the shadow of a shape can be enlarged or reduced.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6c7ee-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c7ee-105">Remarks</span></span>

<span data-ttu-id="6c7ee-106">Jeder Schatten weist eine schattierte Speicherorts eines Punkts auf der Schatten, die die Shape-PIN bis entspricht.</span><span class="sxs-lookup"><span data-stu-id="6c7ee-106">Each shadow has a shadowed pin location, which is a point on the shadow that corresponds to the shape's pin.</span></span> <span data-ttu-id="6c7ee-107">Wenn ein Shape-Pin in der Mitte des Shapes befindet, würde der schattierte Speicherort beispielsweise den Punkt in der Mitte des Schattens sein.</span><span class="sxs-lookup"><span data-stu-id="6c7ee-107">For example, if a shape's pin is in the center of the shape, then the shadowed pin location would be the point in the center of the shadow.</span></span> <span data-ttu-id="6c7ee-108">Skalierung auf einfache Schatten angewendet wird, wird an der Position schattierte Vergrößerung zentriert; Beim Skalieren einfache Schatten anwenden, wird die Vergrößerung in der Schräge angibt angewendet.</span><span class="sxs-lookup"><span data-stu-id="6c7ee-108">When applying scale to simple shadows, magnification is centered at the shadowed pin location; when applying scale to oblique shadows, magnification is applied in the oblique direction.</span></span> 
  
<span data-ttu-id="6c7ee-109">Wenn Sie diesen Wert für alle Shapes auf einem Zeichenblatt festlegen möchten, verwenden Sie die Zelle ShapeShdwScaleFactor im Abschnitt Page Properties.</span><span class="sxs-lookup"><span data-stu-id="6c7ee-109">To set this value for all the shapes on a page, use the ShdwScaleFactor cell in the Page Properties section.</span></span>
  
<span data-ttu-id="6c7ee-110">Dieser Wert entspricht dem Wert der Einstellung **Vergrößerung** im Dialogfeld **Schatten** (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** auf **Schatten**, und klicken Sie dann auf **Schattenoptionen**).</span><span class="sxs-lookup"><span data-stu-id="6c7ee-110">This value corresponds to the value of the **Magnification** setting in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="6c7ee-111">Wenn Sie einen Verweis auf die Zelle ShapeShdwScaleFactor aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6c7ee-111">To get a reference to the ShapeShdwScaleFactor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6c7ee-112">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="6c7ee-112">Cell name:</span></span>  <br/> |<span data-ttu-id="6c7ee-113">ShapeShdwScaleFactor</span><span class="sxs-lookup"><span data-stu-id="6c7ee-113">ShapeShdwScaleFactor</span></span>  <br/> |
   
<span data-ttu-id="6c7ee-114">Wenn Sie einen Verweis auf die Zelle ShapeShdwScaleFactor aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="6c7ee-114">To get a reference to the ShapeShdwScaleFactor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6c7ee-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="6c7ee-115">Section index:</span></span>  <br/> |<span data-ttu-id="6c7ee-116">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6c7ee-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="6c7ee-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="6c7ee-117">Row index:</span></span>  <br/> |<span data-ttu-id="6c7ee-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="6c7ee-118">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="6c7ee-119">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="6c7ee-119">Cell index:</span></span>  <br/> |<span data-ttu-id="6c7ee-120">**visFillShdwScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="6c7ee-120">**visFillShdwScaleFactor**</span></span> <br/> |
   

