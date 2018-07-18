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
description: 'Legt die X--Koordinate des Textblocks des Drehung im Verhältnis zum Ursprung des Shapes. Die Standardformel lautet:'
ms.openlocfilehash: df103557d103dbde7e4a1c8d67cabe37a0af9311
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798324"
---
# <a name="txtpinx-cell-text-transform-section"></a><span data-ttu-id="2b7c9-104">TxtPinX Cell (Text Transform Section)</span><span class="sxs-lookup"><span data-stu-id="2b7c9-104">TxtPinX Cell (Text Transform Section)</span></span>

<span data-ttu-id="2b7c9-105">Legt die *X* --Koordinate des Textblocks des Drehung im Verhältnis zum Ursprung des Shapes.</span><span class="sxs-lookup"><span data-stu-id="2b7c9-105">Determines the  *x*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="2b7c9-106">Die Standardformel lautet:</span><span class="sxs-lookup"><span data-stu-id="2b7c9-106">The default formula is:</span></span> 
  
<span data-ttu-id="2b7c9-107">= Breite \* 0,5</span><span class="sxs-lookup"><span data-stu-id="2b7c9-107">= Width \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2b7c9-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b7c9-108">Remarks</span></span>

<span data-ttu-id="2b7c9-109">Wenn Sie einen Verweis auf die Zelle TxtPinX aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2b7c9-109">To get a reference to the TxtPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2b7c9-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2b7c9-110">Cell name:</span></span>  <br/> | <span data-ttu-id="2b7c9-111">TxtPinX</span><span class="sxs-lookup"><span data-stu-id="2b7c9-111">TxtPinX</span></span>  <br/> |
   
<span data-ttu-id="2b7c9-112">Wenn Sie einen Verweis auf die Zelle TxtPinX aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="2b7c9-112">To get a reference to the TxtPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2b7c9-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2b7c9-113">Section index:</span></span>  <br/> |<span data-ttu-id="2b7c9-114">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2b7c9-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2b7c9-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2b7c9-115">Row index:</span></span>  <br/> |<span data-ttu-id="2b7c9-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="2b7c9-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="2b7c9-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="2b7c9-117">Cell index:</span></span>  <br/> |<span data-ttu-id="2b7c9-118">**visXFormPinX**</span><span class="sxs-lookup"><span data-stu-id="2b7c9-118">**visXFormPinX**</span></span> <br/> |
   

