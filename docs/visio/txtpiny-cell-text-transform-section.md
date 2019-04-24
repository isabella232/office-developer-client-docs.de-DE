---
title: Zelle "TxtPinY" (Abschnitt "Text Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1045
localization_priority: Normal
ms.assetid: 88ddf4b5-8248-8c1a-c387-09a607639d26
description: 'Bestimmt die y-Koordinate des Drehmittelpunkts des Textblocks im Verhältnis zum Ursprung der Form. Die Standardformel lautet:'
ms.openlocfilehash: fc62ac76aa24a698d956690df6e5d1e7cff3fb5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316422"
---
# <a name="txtpiny-cell-text-transform-section"></a><span data-ttu-id="9e9d9-104">Zelle "TxtPinY" (Abschnitt "Text Transform")</span><span class="sxs-lookup"><span data-stu-id="9e9d9-104">TxtPinY Cell (Text Transform Section)</span></span>

<span data-ttu-id="9e9d9-105">Bestimmt die *y* -Koordinate des Drehmittelpunkts des Textblocks im Verhältnis zum Ursprung der Form.</span><span class="sxs-lookup"><span data-stu-id="9e9d9-105">Determines the  *y*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="9e9d9-106">Die Standardformel lautet:</span><span class="sxs-lookup"><span data-stu-id="9e9d9-106">The default formula is:</span></span> 
  
<span data-ttu-id="9e9d9-107">= Höhe \* 0,5</span><span class="sxs-lookup"><span data-stu-id="9e9d9-107">= Height \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9e9d9-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e9d9-108">Remarks</span></span>

<span data-ttu-id="9e9d9-109">Wenn Sie einen Verweis auf die Zelle Zelle TxtPinY aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9e9d9-109">To get a reference to the TxtPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9e9d9-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9e9d9-110">Cell name:</span></span>  <br/> | <span data-ttu-id="9e9d9-111">Zelle TxtPinY</span><span class="sxs-lookup"><span data-stu-id="9e9d9-111">TxtPinY</span></span>  <br/> |
   
<span data-ttu-id="9e9d9-112">Wenn Sie einen Verweis auf die Zelle Zelle TxtPinY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="9e9d9-112">To get a reference to the TxtPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9e9d9-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9e9d9-113">Section index:</span></span>  <br/> |<span data-ttu-id="9e9d9-114">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9e9d9-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9e9d9-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9e9d9-115">Row index:</span></span>  <br/> |<span data-ttu-id="9e9d9-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="9e9d9-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="9e9d9-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9e9d9-117">Cell index:</span></span>  <br/> |<span data-ttu-id="9e9d9-118">**visXFormPinY**</span><span class="sxs-lookup"><span data-stu-id="9e9d9-118">**visXFormPinY**</span></span> <br/> |
   

