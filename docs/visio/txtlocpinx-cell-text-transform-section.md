---
title: Zelle "TxtLocPinX" (Abschnitt "Text Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251275
localization_priority: Normal
ms.assetid: cbfc4e91-10d1-d50e-3e8a-f269f7123276
description: 'Bestimmt die x-Koordinate des Drehzentrums des Textblocks im Verhältnis zum Ursprung des Textblocks. Die Standardformel lautet:'
ms.openlocfilehash: 390f8129e8000a043969eda0ab1c8e4ef62515ef
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425855"
---
# <a name="txtlocpinx-cell-text-transform-section"></a><span data-ttu-id="bd503-104">Zelle "TxtLocPinX" (Abschnitt "Text Transform")</span><span class="sxs-lookup"><span data-stu-id="bd503-104">TxtLocPinX Cell (Text Transform Section)</span></span>

<span data-ttu-id="bd503-105">Bestimmt  die x-Koordinate des Drehzentrums des Textblocks im Verhältnis zum Ursprung des Textblocks.</span><span class="sxs-lookup"><span data-stu-id="bd503-105">Determines the  *x*  -coordinate of the text block's center of rotation in relation to the origin of the text block.</span></span> <span data-ttu-id="bd503-106">Die Standardformel lautet:</span><span class="sxs-lookup"><span data-stu-id="bd503-106">The default formula is:</span></span> 
  
<span data-ttu-id="bd503-107">= TxtWidth \* 0,5</span><span class="sxs-lookup"><span data-stu-id="bd503-107">= TxtWidth \* 0.5</span></span>
  
<span data-ttu-id="bd503-108">Diese Formel berechnet die horizontale Mitte des Textblocks.</span><span class="sxs-lookup"><span data-stu-id="bd503-108">This formula evaluates to the horizontal center of the text block.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bd503-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bd503-109">Remarks</span></span>

<span data-ttu-id="bd503-110">Um einen Verweis auf die Zelle TxtLocPinX anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="bd503-110">To get a reference to the TxtLocPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bd503-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="bd503-111">Cell name:</span></span>  <br/> | <span data-ttu-id="bd503-112">TxtLocPinX</span><span class="sxs-lookup"><span data-stu-id="bd503-112">TxtLocPinX</span></span>  <br/> |
   
<span data-ttu-id="bd503-113">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle TxtLocPinX nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="bd503-113">To get a reference to the TxtLocPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bd503-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="bd503-114">Section index:</span></span>  <br/> |<span data-ttu-id="bd503-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bd503-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bd503-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="bd503-116">Row index:</span></span>  <br/> |<span data-ttu-id="bd503-117">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="bd503-117">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="bd503-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="bd503-118">Cell index:</span></span>  <br/> |<span data-ttu-id="bd503-119">**visXFormLocPinX**</span><span class="sxs-lookup"><span data-stu-id="bd503-119">**visXFormLocPinX**</span></span> <br/> |
   

