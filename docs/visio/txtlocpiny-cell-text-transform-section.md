---
title: Zelle "TxtLocPinY" (Abschnitt "Text Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251276
localization_priority: Normal
ms.assetid: 3f46cfcf-7eac-4a37-e782-39f4e7f8fc43
description: 'Bestimmt die y-Koordinate der Drehmitte des Textblocks relativ zum Ursprung des Textblocks. Die Standardformel lautet:'
ms.openlocfilehash: 937c4e9928d32d55e8336d192b1ecc6140fd8381
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414060"
---
# <a name="txtlocpiny-cell-text-transform-section"></a><span data-ttu-id="664a3-104">Zelle "TxtLocPinY" (Abschnitt "Text Transform")</span><span class="sxs-lookup"><span data-stu-id="664a3-104">TxtLocPinY Cell (Text Transform Section)</span></span>

<span data-ttu-id="664a3-105">Bestimmt  die y-Koordinate der Drehmitte des Textblocks relativ zum Ursprung des Textblocks.</span><span class="sxs-lookup"><span data-stu-id="664a3-105">Determines the  *y*  -coordinate of the text block's center of rotation relative to the origin of the text block.</span></span> <span data-ttu-id="664a3-106">Die Standardformel lautet:</span><span class="sxs-lookup"><span data-stu-id="664a3-106">The default formula is:</span></span> 
  
<span data-ttu-id="664a3-107">= TxtHeight \* 0,5</span><span class="sxs-lookup"><span data-stu-id="664a3-107">= TxtHeight \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="664a3-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="664a3-108">Remarks</span></span>

<span data-ttu-id="664a3-109">Um einen Verweis auf die Zelle TxtLocPinY anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="664a3-109">To get a reference to the TxtLocPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="664a3-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="664a3-110">Cell name:</span></span>  <br/> | <span data-ttu-id="664a3-111">TxtLocPinY</span><span class="sxs-lookup"><span data-stu-id="664a3-111">TxtLocPinY</span></span>  <br/> |
   
<span data-ttu-id="664a3-112">Um einen Verweis auf die Zelle TxtLocPinY nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="664a3-112">To get a reference to the TxtLocPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="664a3-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="664a3-113">Section index:</span></span>  <br/> |<span data-ttu-id="664a3-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="664a3-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="664a3-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="664a3-115">Row index:</span></span>  <br/> |<span data-ttu-id="664a3-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="664a3-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="664a3-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="664a3-117">Cell index:</span></span>  <br/> |<span data-ttu-id="664a3-118">**visXFormLocPinY**</span><span class="sxs-lookup"><span data-stu-id="664a3-118">**visXFormLocPinY**</span></span> <br/> |
   

