---
title: Zelle "TxtHeight" (Abschnitt "Text Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1025
localization_priority: Normal
ms.assetid: cfa3ecc6-61a8-506c-ba1d-b5e1f757d44f
description: 'Definiert die Höhe eines Textblocks. Die Standardformel lautet:'
ms.openlocfilehash: 8ad17cdf1deca6c4aa81f3388d7c112b4e179e2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409307"
---
# <a name="txtheight-cell-text-transform-section"></a><span data-ttu-id="363de-104">Zelle "TxtHeight" (Abschnitt "Text Transform")</span><span class="sxs-lookup"><span data-stu-id="363de-104">TxtHeight Cell (Text Transform Section)</span></span>

<span data-ttu-id="363de-p102">Definiert die Höhe eines Textblocks. Die Standardformel lautet:</span><span class="sxs-lookup"><span data-stu-id="363de-p102">Determines the height of the text block. The default formula is:</span></span>
  
<span data-ttu-id="363de-107">= Höhe \* 1</span><span class="sxs-lookup"><span data-stu-id="363de-107">= Height \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="363de-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="363de-108">Remarks</span></span>

<span data-ttu-id="363de-109">Um einen Verweis auf die Zelle TxtHeight anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="363de-109">To get a reference to the TxtHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="363de-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="363de-110">Cell name:</span></span>  <br/> | <span data-ttu-id="363de-111">TxtHeight</span><span class="sxs-lookup"><span data-stu-id="363de-111">TxtHeight</span></span>  <br/> |
   
<span data-ttu-id="363de-112">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle TxtHeight nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="363de-112">To get a reference to the TxtHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="363de-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="363de-113">Section index:</span></span>  <br/> |<span data-ttu-id="363de-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="363de-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="363de-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="363de-115">Row index:</span></span>  <br/> |<span data-ttu-id="363de-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="363de-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="363de-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="363de-117">Cell index:</span></span>  <br/> |<span data-ttu-id="363de-118">**visXFormHeight**</span><span class="sxs-lookup"><span data-stu-id="363de-118">**visXFormHeight**</span></span> <br/> |
   

