---
title: Zelle "TxtWidth" (Abschnitt "Text Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251270
localization_priority: Normal
ms.assetid: e2215c67-25fa-1d75-9cce-f126bb8760a1
description: 'Definiert die Breite eines Textblocks. Die Standardformel lautet:'
ms.openlocfilehash: 806307166035ebc2f8e20e7025d5ecb03c4d6e79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426093"
---
# <a name="txtwidth-cell-text-transform-section"></a><span data-ttu-id="2853a-104">Zelle "TxtWidth" (Abschnitt "Text Transform")</span><span class="sxs-lookup"><span data-stu-id="2853a-104">TxtWidth Cell (Text Transform Section)</span></span>

<span data-ttu-id="2853a-p102">Definiert die Breite eines Textblocks. Die Standardformel lautet:</span><span class="sxs-lookup"><span data-stu-id="2853a-p102">Determines the width of the text block. The default formula is:</span></span>
  
<span data-ttu-id="2853a-107">= Breite \* 1</span><span class="sxs-lookup"><span data-stu-id="2853a-107">= Width \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2853a-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2853a-108">Remarks</span></span>

<span data-ttu-id="2853a-109">Um einen Verweis auf die Zelle TxtWidth anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="2853a-109">To get a reference to the TxtWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2853a-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2853a-110">Cell name:</span></span>  <br/> | <span data-ttu-id="2853a-111">TxtWidth</span><span class="sxs-lookup"><span data-stu-id="2853a-111">TxtWidth</span></span>  <br/> |
   
<span data-ttu-id="2853a-112">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle TxtWidth nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="2853a-112">To get a reference to the TxtWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2853a-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2853a-113">Section index:</span></span>  <br/> |<span data-ttu-id="2853a-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2853a-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2853a-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2853a-115">Row index:</span></span>  <br/> |<span data-ttu-id="2853a-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="2853a-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="2853a-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="2853a-117">Cell index:</span></span>  <br/> |<span data-ttu-id="2853a-118">**visXFormWidth**</span><span class="sxs-lookup"><span data-stu-id="2853a-118">**visXFormWidth**</span></span> <br/> |
   

