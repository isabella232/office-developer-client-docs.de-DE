---
title: SoftEdgesSize Cell (Additional Effect Properties section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a5cde2ca-f343-4a6e-b5d9-a1b78b3cd240
description: Bestimmt die Größe eines weichen Kanten Effekts in Punkt von 0,00 bis 100,00. Wenn die Zelle SoftEdgesSize den Wert 0 hat, weist die Form keine weichen Ränder auf.
ms.openlocfilehash: e749fefde8e0358cbf4ab8388a61ad703c7d52ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334538"
---
# <a name="softedgessize-cell-additional-effect-properties-section"></a><span data-ttu-id="abe57-104">SoftEdgesSize Cell (Additional Effect Properties section)</span><span class="sxs-lookup"><span data-stu-id="abe57-104">SoftEdgesSize Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="abe57-105">Bestimmt die Größe eines weichen Kanten Effekts in Punkt von 0,00 bis 100,00.</span><span class="sxs-lookup"><span data-stu-id="abe57-105">Determines the size of a soft edge effect, in points from 0.00 to 100.00.</span></span> <span data-ttu-id="abe57-106">Wenn die Zelle **SoftEdgesSize** den Wert 0 hat, weist die Form keine weichen Ränder auf.</span><span class="sxs-lookup"><span data-stu-id="abe57-106">If the **SoftEdgesSize** cell has a value of 0, the shape does not have soft edges.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="abe57-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="abe57-107">Remarks</span></span>

<span data-ttu-id="abe57-108">Wenn Sie einen Verweis auf die Zelle **SoftEdgesSize** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="abe57-108">To get a reference to the **SoftEdgesSize** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="abe57-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="abe57-109">Cell name:</span></span>  <br/> | <span data-ttu-id="abe57-110">SoftEdgesSize</span><span class="sxs-lookup"><span data-stu-id="abe57-110">SoftEdgesSize</span></span>  <br/> |
   
<span data-ttu-id="abe57-111">Wenn Sie einen Verweis auf die Zelle **SoftEdgesSize** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="abe57-111">To get a reference to the **SoftEdgesSize** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="abe57-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="abe57-112">Section index:</span></span>  <br/> |<span data-ttu-id="abe57-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="abe57-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="abe57-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="abe57-114">Row index:</span></span>  <br/> |<span data-ttu-id="abe57-115">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="abe57-115">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="abe57-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="abe57-116">Cell index:</span></span>  <br/> |<span data-ttu-id="abe57-117">**visSoftEdgesSize**</span><span class="sxs-lookup"><span data-stu-id="abe57-117">**visSoftEdgesSize**</span></span> <br/> |
   

