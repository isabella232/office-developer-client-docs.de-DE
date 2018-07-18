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
description: 'Legt die y--Koordinate des Textblocks des Drehung im Verhältnis zum Ursprung des Shapes. Die Standardformel lautet:'
ms.openlocfilehash: e8101463413b177bf8ddd80ed52964d3eeae788f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798330"
---
# <a name="txtpiny-cell-text-transform-section"></a><span data-ttu-id="dc930-104">TxtPinY Cell (Text Transform Section)</span><span class="sxs-lookup"><span data-stu-id="dc930-104">TxtPinY Cell (Text Transform Section)</span></span>

<span data-ttu-id="dc930-105">Legt die *y* --Koordinate des Textblocks des Drehung im Verhältnis zum Ursprung des Shapes.</span><span class="sxs-lookup"><span data-stu-id="dc930-105">Determines the  *y*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="dc930-106">Die Standardformel lautet:</span><span class="sxs-lookup"><span data-stu-id="dc930-106">The default formula is:</span></span> 
  
<span data-ttu-id="dc930-107">= Höhe \* 0,5</span><span class="sxs-lookup"><span data-stu-id="dc930-107">= Height \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dc930-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc930-108">Remarks</span></span>

<span data-ttu-id="dc930-109">Wenn Sie einen Verweis auf die Zelle TxtPinY aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="dc930-109">To get a reference to the TxtPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dc930-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="dc930-110">Cell name:</span></span>  <br/> | <span data-ttu-id="dc930-111">TxtPinY</span><span class="sxs-lookup"><span data-stu-id="dc930-111">TxtPinY</span></span>  <br/> |
   
<span data-ttu-id="dc930-112">Wenn Sie einen Verweis auf die Zelle TxtPinY aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="dc930-112">To get a reference to the TxtPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dc930-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="dc930-113">Section index:</span></span>  <br/> |<span data-ttu-id="dc930-114">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dc930-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="dc930-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="dc930-115">Row index:</span></span>  <br/> |<span data-ttu-id="dc930-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="dc930-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="dc930-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="dc930-117">Cell index:</span></span>  <br/> |<span data-ttu-id="dc930-118">**visXFormPinY**</span><span class="sxs-lookup"><span data-stu-id="dc930-118">**visXFormPinY**</span></span> <br/> |
   

