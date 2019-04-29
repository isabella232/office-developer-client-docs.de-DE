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
description: 'Bestimmt die x-Koordinate des Drehmittelpunkts des Textblocks im Verhältnis zum Ursprung der Form. Die Standardformel lautet:'
ms.openlocfilehash: 836f5c807d0c0e53efc825f62f60429274282165
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423496"
---
# <a name="txtpinx-cell-text-transform-section"></a><span data-ttu-id="37194-104">Zelle "TxtPinX" (Abschnitt "Text Transform")</span><span class="sxs-lookup"><span data-stu-id="37194-104">TxtPinX Cell (Text Transform Section)</span></span>

<span data-ttu-id="37194-105">Bestimmt die *x* -Koordinate des Drehmittelpunkts des Textblocks im Verhältnis zum Ursprung der Form.</span><span class="sxs-lookup"><span data-stu-id="37194-105">Determines the  *x*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="37194-106">Die Standardformel lautet:</span><span class="sxs-lookup"><span data-stu-id="37194-106">The default formula is:</span></span> 
  
<span data-ttu-id="37194-107">= Breite \* 0,5</span><span class="sxs-lookup"><span data-stu-id="37194-107">= Width \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="37194-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37194-108">Remarks</span></span>

<span data-ttu-id="37194-109">Wenn Sie einen Verweis auf die Zelle Zelle TxtPinX aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="37194-109">To get a reference to the TxtPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="37194-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="37194-110">Cell name:</span></span>  <br/> | <span data-ttu-id="37194-111">Zelle TxtPinX</span><span class="sxs-lookup"><span data-stu-id="37194-111">TxtPinX</span></span>  <br/> |
   
<span data-ttu-id="37194-112">Wenn Sie einen Verweis auf die Zelle Zelle TxtPinX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="37194-112">To get a reference to the TxtPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="37194-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="37194-113">Section index:</span></span>  <br/> |<span data-ttu-id="37194-114">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="37194-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="37194-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="37194-115">Row index:</span></span>  <br/> |<span data-ttu-id="37194-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="37194-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="37194-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="37194-117">Cell index:</span></span>  <br/> |<span data-ttu-id="37194-118">**visXFormPinX**</span><span class="sxs-lookup"><span data-stu-id="37194-118">**visXFormPinX**</span></span> <br/> |
   

