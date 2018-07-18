---
title: Zelle "LocPinY" (Abschnitt "Shape Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm685
localization_priority: Normal
ms.assetid: a29c5d4e-d3d6-d984-495a-4b0b130352ef
description: 'Stellt die y--Koordinate der Drehbezugspunkts (Drehmittelpunkts) im Verhältnis zum Ursprung des Shapes. Die Standardformel zum Bestimmen von LocPinY lautet:'
ms.openlocfilehash: 8d98906e8082af0fc54bc01fe3a8537b66ac56b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797412"
---
# <a name="locpiny-cell-shape-transform-section"></a><span data-ttu-id="9ca0c-104">LocPinY Cell (Shape Transform Section)</span><span class="sxs-lookup"><span data-stu-id="9ca0c-104">LocPinY Cell (Shape Transform Section)</span></span>

<span data-ttu-id="9ca0c-105">Stellt die *y* --Koordinate der Drehbezugspunkts (Drehmittelpunkts) im Verhältnis zum Ursprung des Shapes.</span><span class="sxs-lookup"><span data-stu-id="9ca0c-105">Represents the  *y*  -coordinate of the shape's pin (center of rotation) in relation to the origin of the shape.</span></span> <span data-ttu-id="9ca0c-106">Die Standardformel zum Bestimmen von LocPinY lautet:</span><span class="sxs-lookup"><span data-stu-id="9ca0c-106">The default formula for determining LocPinY is:</span></span> 
  
<span data-ttu-id="9ca0c-107">= Höhe \* 0,5</span><span class="sxs-lookup"><span data-stu-id="9ca0c-107">= Height \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9ca0c-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ca0c-108">Remarks</span></span>

<span data-ttu-id="9ca0c-109">Wenn Sie einen Verweis auf die Zelle LocPinY aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9ca0c-109">To get a reference to the LocPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9ca0c-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9ca0c-110">Cell name:</span></span>  <br/> | <span data-ttu-id="9ca0c-111">LocPinY</span><span class="sxs-lookup"><span data-stu-id="9ca0c-111">LocPinY</span></span>  <br/> |
   
<span data-ttu-id="9ca0c-112">Wenn Sie einen Verweis auf die Zelle LocPinY aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="9ca0c-112">To get a reference to the LocPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9ca0c-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9ca0c-113">Section index:</span></span>  <br/> |<span data-ttu-id="9ca0c-114">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9ca0c-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9ca0c-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9ca0c-115">Row index:</span></span>  <br/> |<span data-ttu-id="9ca0c-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="9ca0c-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="9ca0c-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9ca0c-117">Cell index:</span></span>  <br/> |<span data-ttu-id="9ca0c-118">**visXFormLocPinY**</span><span class="sxs-lookup"><span data-stu-id="9ca0c-118">**visXFormLocPinY**</span></span> <br/> |
   

