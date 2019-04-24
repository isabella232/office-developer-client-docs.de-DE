---
title: Zelle "RotateGradientWithShape" (Abschnitt "Gradient Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aada005-3403-4666-9779-7ccb5b83b74a
description: Bestimmt, ob ein Füll Verlauf mit einer Form in der 2D-Rotation als boolescher Wert rotiert.
ms.openlocfilehash: 76a76a4a97128c81710269f75e9e17db90827377
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315659"
---
# <a name="rotategradientwithshape-cell-gradient-properties-section"></a><span data-ttu-id="6ecb7-103">Zelle "RotateGradientWithShape" (Abschnitt "Gradient Properties")</span><span class="sxs-lookup"><span data-stu-id="6ecb7-103">RotateGradientWithShape Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="6ecb7-104">Bestimmt, ob ein Füll Verlauf mit einer Form in der 2D-Rotation als boolescher Wert rotiert.</span><span class="sxs-lookup"><span data-stu-id="6ecb7-104">Determines whether a fill gradient rotates with a shape in 2D rotation, as a boolean.</span></span>
  
|<span data-ttu-id="6ecb7-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="6ecb7-105">**Value**</span></span>|<span data-ttu-id="6ecb7-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6ecb7-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6ecb7-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="6ecb7-107">TRUE</span></span>  <br/> |<span data-ttu-id="6ecb7-108">Der Farbverlauf wird mit der Form gedreht, wenn die Form um die Rotations-Pin gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="6ecb7-108">The gradient rotates with the shape when the shape is rotated around the rotation pin.</span></span> <span data-ttu-id="6ecb7-109">Der "obere" des Farbverlaufs ist parallel zum Drehpunkt.</span><span class="sxs-lookup"><span data-stu-id="6ecb7-109">The "top" of the gradient is parallel to the rotation handle.</span></span>  <br/> |
|<span data-ttu-id="6ecb7-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="6ecb7-110">FALSE</span></span>  <br/> |<span data-ttu-id="6ecb7-111">Der Farbverlauf wird nicht mit der Form gedreht, wenn die Form um die Rotations-Pin gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="6ecb7-111">The gradient does not rotate with the shape when the shape is rotated around the rotation pin.</span></span> <span data-ttu-id="6ecb7-112">Der "obere" des Farbverlaufs ist parallel zum Zeichenbereich.</span><span class="sxs-lookup"><span data-stu-id="6ecb7-112">The "top" of the gradient is parallel to the drawing canvas.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ecb7-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ecb7-113">Remarks</span></span>

<span data-ttu-id="6ecb7-114">Wenn Sie einen Verweis auf die Zelle **RotateGradientWithShape** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6ecb7-114">To get a reference to the **RotateGradientWithShape** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6ecb7-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="6ecb7-115">Cell name:</span></span>  <br/> | <span data-ttu-id="6ecb7-116">RotateGradientWithShape</span><span class="sxs-lookup"><span data-stu-id="6ecb7-116">RotateGradientWithShape</span></span>  <br/> |
   
<span data-ttu-id="6ecb7-117">Wenn Sie einen Verweis auf die Zelle **RotateGradientWithShape** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="6ecb7-117">To get a reference to the **RotateGradientWithShape** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6ecb7-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="6ecb7-118">Section index:</span></span>  <br/> |<span data-ttu-id="6ecb7-119">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6ecb7-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6ecb7-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="6ecb7-120">Row index:</span></span>  <br/> |<span data-ttu-id="6ecb7-121">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="6ecb7-121">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="6ecb7-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="6ecb7-122">Cell index:</span></span>  <br/> |<span data-ttu-id="6ecb7-123">**visRotateGradientWithShape**</span><span class="sxs-lookup"><span data-stu-id="6ecb7-123">**visRotateGradientWithShape**</span></span> <br/> |
   

