---
title: RotateGradientWithShape Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aada005-3403-4666-9779-7ccb5b83b74a
description: Bestimmt, ob eine graduelle Füllung mit einem Shape in 2D Drehung, als ein boolescher Wert dreht.
ms.openlocfilehash: d752f870fd08c1a47dfc7ce193b6976a1bdb2a1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797865"
---
# <a name="rotategradientwithshape-cell-gradient-properties-section"></a><span data-ttu-id="20b5a-103">RotateGradientWithShape Cell (Gradient Properties Section)</span><span class="sxs-lookup"><span data-stu-id="20b5a-103">RotateGradientWithShape Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="20b5a-104">Bestimmt, ob eine graduelle Füllung mit einem Shape in 2D Drehung, als ein boolescher Wert dreht.</span><span class="sxs-lookup"><span data-stu-id="20b5a-104">Determines whether a fill gradient rotates with a shape in 2D rotation, as a boolean.</span></span>
  
|<span data-ttu-id="20b5a-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="20b5a-105">**Value**</span></span>|<span data-ttu-id="20b5a-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="20b5a-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="20b5a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="20b5a-107">TRUE</span></span>  <br/> |<span data-ttu-id="20b5a-108">Der Farbverlauf wird mit der Form gedreht, wenn die Form um die Drehung Pin gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="20b5a-108">The gradient rotates with the shape when the shape is rotated around the rotation pin.</span></span> <span data-ttu-id="20b5a-109">"Top" des Farbverlaufs ist parallel zu den Drehpunkt.</span><span class="sxs-lookup"><span data-stu-id="20b5a-109">The "top" of the gradient is parallel to the rotation handle.</span></span>  <br/> |
|<span data-ttu-id="20b5a-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="20b5a-110">FALSE</span></span>  <br/> |<span data-ttu-id="20b5a-111">Der Farbverlauf wird nicht mit der Form gedreht, bei die Form um die Drehung Pin gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="20b5a-111">The gradient does not rotate with the shape when the shape is rotated around the rotation pin.</span></span> <span data-ttu-id="20b5a-112">"Top" des Farbverlaufs ist parallel zum Zeichenbereich.</span><span class="sxs-lookup"><span data-stu-id="20b5a-112">The "top" of the gradient is parallel to the drawing canvas.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="20b5a-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="20b5a-113">Remarks</span></span>

<span data-ttu-id="20b5a-114">Wenn Sie einen Verweis auf die Zelle **RotateGradientWithShape** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="20b5a-114">To get a reference to the **RotateGradientWithShape** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="20b5a-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="20b5a-115">Cell name:</span></span>  <br/> | <span data-ttu-id="20b5a-116">RotateGradientWithShape</span><span class="sxs-lookup"><span data-stu-id="20b5a-116">RotateGradientWithShape</span></span>  <br/> |
   
<span data-ttu-id="20b5a-117">Wenn Sie einen Verweis auf die Zelle **RotateGradientWithShape** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="20b5a-117">To get a reference to the **RotateGradientWithShape** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="20b5a-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="20b5a-118">Section index:</span></span>  <br/> |<span data-ttu-id="20b5a-119">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="20b5a-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="20b5a-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="20b5a-120">Row index:</span></span>  <br/> |<span data-ttu-id="20b5a-121">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="20b5a-121">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="20b5a-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="20b5a-122">Cell index:</span></span>  <br/> |<span data-ttu-id="20b5a-123">**visRotateGradientWithShape**</span><span class="sxs-lookup"><span data-stu-id="20b5a-123">**visRotateGradientWithShape**</span></span> <br/> |
   

