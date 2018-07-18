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
description: 'Legt die X--Koordinate des Textblocks des Drehung im Verhältnis zum Ursprung des Textblocks. Die Standardformel lautet:'
ms.openlocfilehash: 6eb48532bb19bce5b0d22ed2cd0997014721df88
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798313"
---
# <a name="txtlocpinx-cell-text-transform-section"></a><span data-ttu-id="6ea2a-104">TxtLocPinX Cell (Text Transform Section)</span><span class="sxs-lookup"><span data-stu-id="6ea2a-104">TxtLocPinX Cell (Text Transform Section)</span></span>

<span data-ttu-id="6ea2a-105">Legt die *X* --Koordinate des Textblocks des Drehung im Verhältnis zum Ursprung des Textblocks.</span><span class="sxs-lookup"><span data-stu-id="6ea2a-105">Determines the  *x*  -coordinate of the text block's center of rotation in relation to the origin of the text block.</span></span> <span data-ttu-id="6ea2a-106">Die Standardformel lautet:</span><span class="sxs-lookup"><span data-stu-id="6ea2a-106">The default formula is:</span></span> 
  
<span data-ttu-id="6ea2a-107">= TxtWidth \* 0,5</span><span class="sxs-lookup"><span data-stu-id="6ea2a-107">= TxtWidth \* 0.5</span></span>
  
<span data-ttu-id="6ea2a-108">Diese Formel berechnet die horizontale Mitte des Textblocks.</span><span class="sxs-lookup"><span data-stu-id="6ea2a-108">This formula evaluates to the horizontal center of the text block.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6ea2a-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6ea2a-109">Remarks</span></span>

<span data-ttu-id="6ea2a-110">Wenn Sie einen Verweis auf die Zelle TxtLocPinX aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6ea2a-110">To get a reference to the TxtLocPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6ea2a-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="6ea2a-111">Cell name:</span></span>  <br/> | <span data-ttu-id="6ea2a-112">TxtLocPinX</span><span class="sxs-lookup"><span data-stu-id="6ea2a-112">TxtLocPinX</span></span>  <br/> |
   
<span data-ttu-id="6ea2a-113">Wenn Sie einen Verweis auf die Zelle TxtLocPinX aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="6ea2a-113">To get a reference to the TxtLocPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6ea2a-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="6ea2a-114">Section index:</span></span>  <br/> |<span data-ttu-id="6ea2a-115">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6ea2a-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6ea2a-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="6ea2a-116">Row index:</span></span>  <br/> |<span data-ttu-id="6ea2a-117">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="6ea2a-117">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="6ea2a-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="6ea2a-118">Cell index:</span></span>  <br/> |<span data-ttu-id="6ea2a-119">**visXFormLocPinX**</span><span class="sxs-lookup"><span data-stu-id="6ea2a-119">**visXFormLocPinX**</span></span> <br/> |
   

