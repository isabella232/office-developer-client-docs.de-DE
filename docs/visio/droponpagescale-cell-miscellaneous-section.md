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
ms.openlocfilehash: a586cca497e1ba04848142917a84c3aa8a25d081
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796895"
---
# <a name="droponpagescale-cell-miscellaneous-section"></a><span data-ttu-id="0419e-102">DropOnPageScale Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="0419e-102">DropOnPageScale Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="0419e-103">Enthält den Prozentsatz, um den ein Shape beim Ablegen auf dem Zeichenblatt skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="0419e-103">Contains the percentage by which a shape is scaled when dropped on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0419e-104">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0419e-104">Remarks</span></span>

<span data-ttu-id="0419e-105">In den folgenden zwei Fällen werden Shapes in Visio so skaliert, dass sie entsprechend auf dem Zeichenblatt angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="0419e-105">In the following two cases, Visio scales shapes so that they appear appropriately on the drawing page:</span></span>
  
- <span data-ttu-id="0419e-106">Beim Ablegen von Shapes ohne Bemaßung auf skalierten Zeichnungen.</span><span class="sxs-lookup"><span data-stu-id="0419e-106">When unmeasured shapes are dropped onto scaled drawings.</span></span>
    
- <span data-ttu-id="0419e-107">Wenn die Bemaßung auf nicht skalierten Zeichnungen abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0419e-107">When measured shapes are dropped onto unscaled drawings.</span></span>
    
<span data-ttu-id="0419e-108">Der Prozentsatz in der Zelle DropOnPageScale gibt den Faktor, mit dem Visio das Shape, entweder nach oben skaliert (\>100) oder nach unten (\<100).</span><span class="sxs-lookup"><span data-stu-id="0419e-108">The percentage in the DropOnPageScale cell indicates the factor by which Visio scaled the shape, either up (\>100) or down (\<100).</span></span> <span data-ttu-id="0419e-109">Sie können diese Nummer beim Berechnen von hartcodierte Werte als Faktor verwenden.</span><span class="sxs-lookup"><span data-stu-id="0419e-109">You can use this number as a factor when calculating hard-coded values.</span></span> 
  
<span data-ttu-id="0419e-110">Dieser Wert beträgt für Shapes mit Bemaßung auf skalierten Zeichnungen und für Shapes ohne Bemaßung auf nicht skalierten Zeichnungen 100 %.</span><span class="sxs-lookup"><span data-stu-id="0419e-110">This value is 100% for measured shapes on scaled drawings or unmeasured shapes on unscaled drawings.</span></span> 
  
<span data-ttu-id="0419e-111">Wenn Sie einen Verweis auf die Zelle DropOnPageScale nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="0419e-111">To get a reference to the DropOnPageScale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0419e-112">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="0419e-112">Cell name:</span></span>  <br/> | <span data-ttu-id="0419e-113">DropOnPageScale</span><span class="sxs-lookup"><span data-stu-id="0419e-113">DropOnPageScale</span></span>  <br/> |
   
<span data-ttu-id="0419e-114">Wenn Sie einen Verweis auf die Zelle DropOnPageScale aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="0419e-114">To get a reference to the DropOnPageScale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0419e-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="0419e-115">Section index:</span></span>  <br/> |<span data-ttu-id="0419e-116">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0419e-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0419e-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="0419e-117">Row index:</span></span>  <br/> |<span data-ttu-id="0419e-118">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="0419e-118">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="0419e-119">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="0419e-119">Cell index:</span></span>  <br/> |<span data-ttu-id="0419e-120">**visObjDropOnPageScale**</span><span class="sxs-lookup"><span data-stu-id="0419e-120">**visObjDropOnPageScale**</span></span> <br/> |
   

