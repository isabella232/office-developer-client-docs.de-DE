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
description: 'Legt die y--Koordinate des Textblocks des Drehung relativ zum Ursprung des Textblocks. Die Standardformel lautet:'
ms.openlocfilehash: 7d43f63b8560df5fc5daf09a429ce30ec976d131
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798322"
---
# <a name="txtlocpiny-cell-text-transform-section"></a><span data-ttu-id="9f99e-104">TxtLocPinY Cell (Text Transform Section)</span><span class="sxs-lookup"><span data-stu-id="9f99e-104">TxtLocPinY Cell (Text Transform Section)</span></span>

<span data-ttu-id="9f99e-105">Legt die *y* --Koordinate des Textblocks des Drehung relativ zum Ursprung des Textblocks.</span><span class="sxs-lookup"><span data-stu-id="9f99e-105">Determines the  *y*  -coordinate of the text block's center of rotation relative to the origin of the text block.</span></span> <span data-ttu-id="9f99e-106">Die Standardformel lautet:</span><span class="sxs-lookup"><span data-stu-id="9f99e-106">The default formula is:</span></span> 
  
<span data-ttu-id="9f99e-107">= TxtHeight \* 0,5</span><span class="sxs-lookup"><span data-stu-id="9f99e-107">= TxtHeight \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9f99e-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f99e-108">Remarks</span></span>

<span data-ttu-id="9f99e-109">Wenn Sie einen Verweis auf die Zelle TxtLocPinY aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9f99e-109">To get a reference to the TxtLocPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9f99e-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9f99e-110">Cell name:</span></span>  <br/> | <span data-ttu-id="9f99e-111">TxtLocPinY</span><span class="sxs-lookup"><span data-stu-id="9f99e-111">TxtLocPinY</span></span>  <br/> |
   
<span data-ttu-id="9f99e-112">Wenn Sie einen Verweis auf die Zelle TxtLocPinY aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="9f99e-112">To get a reference to the TxtLocPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9f99e-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9f99e-113">Section index:</span></span>  <br/> |<span data-ttu-id="9f99e-114">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9f99e-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9f99e-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9f99e-115">Row index:</span></span>  <br/> |<span data-ttu-id="9f99e-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="9f99e-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="9f99e-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9f99e-117">Cell index:</span></span>  <br/> |<span data-ttu-id="9f99e-118">**visXFormLocPinY**</span><span class="sxs-lookup"><span data-stu-id="9f99e-118">**visXFormLocPinY**</span></span> <br/> |
   

