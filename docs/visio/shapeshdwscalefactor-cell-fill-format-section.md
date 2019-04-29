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
ms.openlocfilehash: 5862b61ca1f5df25ca97bf8742b9e20bf45091a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436265"
---
# <a name="shapeshdwscalefactor-cell-fill-format-section"></a><span data-ttu-id="f6f28-103">Zelle "ShapeShdwScaleFactor" (Abschnitt "Fill Format")</span><span class="sxs-lookup"><span data-stu-id="f6f28-103">ShapeShdwScaleFactor Cell (Fill Format Section)</span></span>

<span data-ttu-id="f6f28-104">Gibt den Prozentsatz an, um den der Schatten eines Shapes vergrößert oder verkleinert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f6f28-104">Specifies the percentage by which the shadow of a shape can be enlarged or reduced.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f6f28-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6f28-105">Remarks</span></span>

<span data-ttu-id="f6f28-106">Jeder Schatten hat eine schattierte Pin-Position, die ein Punkt auf dem Schatten ist, der der PIN des Shapes entspricht.</span><span class="sxs-lookup"><span data-stu-id="f6f28-106">Each shadow has a shadowed pin location, which is a point on the shadow that corresponds to the shape's pin.</span></span> <span data-ttu-id="f6f28-107">Wenn sich beispielsweise die PIN eines Shapes in der Mitte des Shapes befindet, ist die schattierte Position des Pins der Punkt in der Mitte des Schattens.</span><span class="sxs-lookup"><span data-stu-id="f6f28-107">For example, if a shape's pin is in the center of the shape, then the shadowed pin location would be the point in the center of the shadow.</span></span> <span data-ttu-id="f6f28-108">Wenn Sie die Skalierung auf einfache Schatten anwenden, wird die Vergrößerung an der schattierten Pin-Position zentriert. Wenn Sie die Skalierung auf schräge Schatten anwenden, wird die Vergrößerung in schräger Richtung angewendet.</span><span class="sxs-lookup"><span data-stu-id="f6f28-108">When applying scale to simple shadows, magnification is centered at the shadowed pin location; when applying scale to oblique shadows, magnification is applied in the oblique direction.</span></span> 
  
<span data-ttu-id="f6f28-109">Wenn Sie diesen Wert für alle Shapes auf einem Zeichenblatt festlegen möchten, verwenden Sie die Zelle ShapeShdwScaleFactor im Abschnitt Page Properties.</span><span class="sxs-lookup"><span data-stu-id="f6f28-109">To set this value for all the shapes on a page, use the ShdwScaleFactor cell in the Page Properties section.</span></span>
  
<span data-ttu-id="f6f28-110">Dieser Wert entspricht dem Wert der Einstellung **Vergrößerung** im Dialogfeld **Schatten** (klicken Sie auf der Registerkarte **Start** in der Gruppe **Shape** auf **Schatten**, und klicken Sie dann auf **Schattenoptionen**).</span><span class="sxs-lookup"><span data-stu-id="f6f28-110">This value corresponds to the value of the **Magnification** setting in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="f6f28-111">Wenn Sie einen Verweis auf die Zelle Zelle ShapeShdwScaleFactor aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f6f28-111">To get a reference to the ShapeShdwScaleFactor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f6f28-112">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="f6f28-112">Cell name:</span></span>  <br/> |<span data-ttu-id="f6f28-113">Zelle ShapeShdwScaleFactor</span><span class="sxs-lookup"><span data-stu-id="f6f28-113">ShapeShdwScaleFactor</span></span>  <br/> |
   
<span data-ttu-id="f6f28-114">Wenn Sie einen Verweis auf die Zelle Zelle ShapeShdwScaleFactor aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="f6f28-114">To get a reference to the ShapeShdwScaleFactor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f6f28-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="f6f28-115">Section index:</span></span>  <br/> |<span data-ttu-id="f6f28-116">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f6f28-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f6f28-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="f6f28-117">Row index:</span></span>  <br/> |<span data-ttu-id="f6f28-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="f6f28-118">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="f6f28-119">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="f6f28-119">Cell index:</span></span>  <br/> |<span data-ttu-id="f6f28-120">**visFillShdwScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="f6f28-120">**visFillShdwScaleFactor**</span></span> <br/> |
   

