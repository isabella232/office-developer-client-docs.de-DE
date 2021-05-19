---
title: Zelle "TxtPinX" (Abschnitt "Text Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1040
localization_priority: Normal
ms.assetid: d0c0fe52-6a9e-e40e-394e-83a851db55a4
description: 'Bestimmt die x-Koordinate der Drehmitte des Textblocks im Verhältnis zum Ursprung der Form. Die Standardformel lautet:'
ms.openlocfilehash: 836f5c807d0c0e53efc825f62f60429274282165
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423496"
---
# <a name="txtpinx-cell-text-transform-section"></a><span data-ttu-id="87c62-104">Zelle "TxtPinX" (Abschnitt "Text Transform")</span><span class="sxs-lookup"><span data-stu-id="87c62-104">TxtPinX Cell (Text Transform Section)</span></span>

<span data-ttu-id="87c62-105">Bestimmt  die x-Koordinate der Drehmitte des Textblocks im Verhältnis zum Ursprung der Form.</span><span class="sxs-lookup"><span data-stu-id="87c62-105">Determines the  *x*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="87c62-106">Die Standardformel lautet:</span><span class="sxs-lookup"><span data-stu-id="87c62-106">The default formula is:</span></span> 
  
<span data-ttu-id="87c62-107">= Breite \* 0,5</span><span class="sxs-lookup"><span data-stu-id="87c62-107">= Width \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="87c62-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="87c62-108">Remarks</span></span>

<span data-ttu-id="87c62-109">Um einen Verweis auf die Zelle TxtPinX anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="87c62-109">To get a reference to the TxtPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="87c62-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="87c62-110">Cell name:</span></span>  <br/> | <span data-ttu-id="87c62-111">TxtPinX</span><span class="sxs-lookup"><span data-stu-id="87c62-111">TxtPinX</span></span>  <br/> |
   
<span data-ttu-id="87c62-112">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle TxtPinX nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="87c62-112">To get a reference to the TxtPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="87c62-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="87c62-113">Section index:</span></span>  <br/> |<span data-ttu-id="87c62-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="87c62-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="87c62-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="87c62-115">Row index:</span></span>  <br/> |<span data-ttu-id="87c62-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="87c62-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="87c62-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="87c62-117">Cell index:</span></span>  <br/> |<span data-ttu-id="87c62-118">**visXFormPinX**</span><span class="sxs-lookup"><span data-stu-id="87c62-118">**visXFormPinX**</span></span> <br/> |
   

