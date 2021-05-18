---
title: Zelle RotateGradientWithShape (Abschnitt "Gradient Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aada005-3403-4666-9779-7ccb5b83b74a
description: Bestimmt, ob ein Füllgradient mit einer Form in 2D-Drehung gedreht wird, als boolescher Wert.
ms.openlocfilehash: 76a76a4a97128c81710269f75e9e17db90827377
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412219"
---
# <a name="rotategradientwithshape-cell-gradient-properties-section"></a><span data-ttu-id="2077b-103">Zelle RotateGradientWithShape (Abschnitt "Gradient Properties")</span><span class="sxs-lookup"><span data-stu-id="2077b-103">RotateGradientWithShape Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="2077b-104">Bestimmt, ob ein Füllgradient mit einer Form in 2D-Drehung gedreht wird, als boolescher Wert.</span><span class="sxs-lookup"><span data-stu-id="2077b-104">Determines whether a fill gradient rotates with a shape in 2D rotation, as a boolean.</span></span>
  
|<span data-ttu-id="2077b-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2077b-105">**Value**</span></span>|<span data-ttu-id="2077b-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2077b-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2077b-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="2077b-107">TRUE</span></span>  <br/> |<span data-ttu-id="2077b-108">Der Farbverlauf dreht sich mit der Form, wenn die Form um den Drehstift gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="2077b-108">The gradient rotates with the shape when the shape is rotated around the rotation pin.</span></span> <span data-ttu-id="2077b-109">Der "obere Rand" des Farbverlaufs ist parallel zum Drehziehpunkt.</span><span class="sxs-lookup"><span data-stu-id="2077b-109">The "top" of the gradient is parallel to the rotation handle.</span></span>  <br/> |
|<span data-ttu-id="2077b-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="2077b-110">FALSE</span></span>  <br/> |<span data-ttu-id="2077b-111">Der Farbverlauf dreht sich nicht mit der Form, wenn die Form um den Drehstift gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="2077b-111">The gradient does not rotate with the shape when the shape is rotated around the rotation pin.</span></span> <span data-ttu-id="2077b-112">Der "obere Rand" des Farbverlaufs ist parallel zum Zeichenbereich.</span><span class="sxs-lookup"><span data-stu-id="2077b-112">The "top" of the gradient is parallel to the drawing canvas.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2077b-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2077b-113">Remarks</span></span>

<span data-ttu-id="2077b-114">Verwenden Sie zum Erhalten eines Verweises auf die **Zelle RotateGradientWithShape** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="2077b-114">To get a reference to the **RotateGradientWithShape** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2077b-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2077b-115">Cell name:</span></span>  <br/> | <span data-ttu-id="2077b-116">RotateGradientWithShape</span><span class="sxs-lookup"><span data-stu-id="2077b-116">RotateGradientWithShape</span></span>  <br/> |
   
<span data-ttu-id="2077b-117">Um einen Verweis auf die **RotateGradientWithShape-Zelle** nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="2077b-117">To get a reference to the **RotateGradientWithShape** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2077b-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2077b-118">Section index:</span></span>  <br/> |<span data-ttu-id="2077b-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2077b-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2077b-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2077b-120">Row index:</span></span>  <br/> |<span data-ttu-id="2077b-121">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="2077b-121">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="2077b-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="2077b-122">Cell index:</span></span>  <br/> |<span data-ttu-id="2077b-123">**visRotateGradientWithShape**</span><span class="sxs-lookup"><span data-stu-id="2077b-123">**visRotateGradientWithShape**</span></span> <br/> |
   

