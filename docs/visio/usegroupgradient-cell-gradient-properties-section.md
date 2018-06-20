---
title: UseGroupGradient Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f1dcf0ec-8b4a-4ee1-9208-b1c84e30d37b
description: Bestimmt, ob die Form für einen Farbverlauf ausführt, wenn das Shape als boolescher Wert zusammen mit anderen Shapes gruppiert werden. Der Wert der Zelle UseGroupGradient betrifft nur die Füllung der Form.
ms.openlocfilehash: ca11ad1c54097b4883bb5348583c6cf39127e4e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798359"
---
# <a name="usegroupgradient-cell-gradient-properties-section"></a><span data-ttu-id="a3170-104">UseGroupGradient Cell (Gradient Properties Section)</span><span class="sxs-lookup"><span data-stu-id="a3170-104">UseGroupGradient Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="a3170-105">Bestimmt, ob die Form für einen Farbverlauf ausführt, wenn das Shape als boolescher Wert zusammen mit anderen Shapes gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="a3170-105">Determines whether the shape takes on a gradient when the shape is grouped together with other shapes, as a Boolean.</span></span> <span data-ttu-id="a3170-106">Der Wert der Zelle **UseGroupGradient** betrifft nur die Füllung der Form.</span><span class="sxs-lookup"><span data-stu-id="a3170-106">The value of **UseGroupGradient** cell affects the shape fill only.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a3170-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a3170-107">Remarks</span></span>

<span data-ttu-id="a3170-108">Wenn Sie einen Verweis auf die Zelle **UseGroupGradient** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a3170-108">To get a reference to the **UseGroupGradient** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a3170-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a3170-109">Cell name:</span></span>  <br/> | <span data-ttu-id="a3170-110">UseGroupGradient</span><span class="sxs-lookup"><span data-stu-id="a3170-110">UseGroupGradient</span></span>  <br/> |
   
<span data-ttu-id="a3170-111">Wenn Sie einen Verweis auf die Zelle **UseGroupGradient** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a3170-111">To get a reference to the **UseGroupGradient** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a3170-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a3170-112">Section index:</span></span>  <br/> |<span data-ttu-id="a3170-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a3170-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a3170-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a3170-114">Row index:</span></span>  <br/> |<span data-ttu-id="a3170-115">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="a3170-115">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="a3170-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a3170-116">Cell index:</span></span>  <br/> |<span data-ttu-id="a3170-117">** VisUseGroupGradient **</span><span class="sxs-lookup"><span data-stu-id="a3170-117">**visUseGroupGradient **</span></span> <br/> |
   

