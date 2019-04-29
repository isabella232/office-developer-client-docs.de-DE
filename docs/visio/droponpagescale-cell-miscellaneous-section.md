---
title: Zelle "DropOnPageScale" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60042
localization_priority: Normal
ms.assetid: 8927f811-7d8e-ed54-9eec-b86a781168dd
ms.openlocfilehash: 17c597df3d9e7e741d902fd566cc9a5de1f31ea0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423762"
---
# <a name="droponpagescale-cell-miscellaneous-section"></a><span data-ttu-id="605e1-102">Zelle "DropOnPageScale" (Abschnitt "Miscellaneous")</span><span class="sxs-lookup"><span data-stu-id="605e1-102">DropOnPageScale Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="605e1-103">Enthält den Prozentsatz, um den ein Shape beim Ablegen auf dem Zeichenblatt skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="605e1-103">Contains the percentage by which a shape is scaled when dropped on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="605e1-104">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="605e1-104">Remarks</span></span>

<span data-ttu-id="605e1-105">In den folgenden zwei Fällen werden Shapes in Visio so skaliert, dass sie entsprechend auf dem Zeichenblatt angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="605e1-105">In the following two cases, Visio scales shapes so that they appear appropriately on the drawing page:</span></span>
  
- <span data-ttu-id="605e1-106">Beim Ablegen von Shapes ohne Bemaßung auf skalierten Zeichnungen.</span><span class="sxs-lookup"><span data-stu-id="605e1-106">When unmeasured shapes are dropped onto scaled drawings.</span></span>
    
- <span data-ttu-id="605e1-107">Wenn gemessene Formen auf nicht skalierten Zeichnungen abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="605e1-107">When measured shapes are dropped onto unscaled drawings.</span></span>
    
<span data-ttu-id="605e1-108">Der Prozentsatz in der Zelle Zelle DropOnPageScale gibt den Faktor an, mit dem Visio die Form skaliert hat (\>100) oder nach unten\<(100).</span><span class="sxs-lookup"><span data-stu-id="605e1-108">The percentage in the DropOnPageScale cell indicates the factor by which Visio scaled the shape, either up (\>100) or down (\<100).</span></span> <span data-ttu-id="605e1-109">Sie können diese Zahl beim Berechnen von festgelegten Werten als Faktor verwenden.</span><span class="sxs-lookup"><span data-stu-id="605e1-109">You can use this number as a factor when calculating hard-coded values.</span></span> 
  
<span data-ttu-id="605e1-110">Dieser Wert beträgt für Shapes mit Bemaßung auf skalierten Zeichnungen und für Shapes ohne Bemaßung auf nicht skalierten Zeichnungen 100 %.</span><span class="sxs-lookup"><span data-stu-id="605e1-110">This value is 100% for measured shapes on scaled drawings or unmeasured shapes on unscaled drawings.</span></span> 
  
<span data-ttu-id="605e1-111">Wenn Sie einen Verweis auf die Zelle Zelle DropOnPageScale aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="605e1-111">To get a reference to the DropOnPageScale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="605e1-112">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="605e1-112">Cell name:</span></span>  <br/> | <span data-ttu-id="605e1-113">Zelle DropOnPageScale</span><span class="sxs-lookup"><span data-stu-id="605e1-113">DropOnPageScale</span></span>  <br/> |
   
<span data-ttu-id="605e1-114">Wenn Sie einen Verweis auf die Zelle Zelle DropOnPageScale aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="605e1-114">To get a reference to the DropOnPageScale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="605e1-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="605e1-115">Section index:</span></span>  <br/> |<span data-ttu-id="605e1-116">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="605e1-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="605e1-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="605e1-117">Row index:</span></span>  <br/> |<span data-ttu-id="605e1-118">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="605e1-118">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="605e1-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="605e1-119">Cell index:</span></span>  <br/> |<span data-ttu-id="605e1-120">**visObjDropOnPageScale**</span><span class="sxs-lookup"><span data-stu-id="605e1-120">**visObjDropOnPageScale**</span></span> <br/> |
   

