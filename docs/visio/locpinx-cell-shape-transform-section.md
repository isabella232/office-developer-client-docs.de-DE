---
title: Zelle "LocPinX" (Abschnitt "Shape Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm680
localization_priority: Normal
ms.assetid: b82feade-5793-8a6e-3ff4-69a4cbdd2cf9
description: 'Stellt die X--Koordinate der Drehbezugspunkts (Drehmittelpunkts) im Verhältnis zum Ursprung des Shapes. Die Standardformel zum Bestimmen von LocPinX lautet:'
ms.openlocfilehash: 17f7b0fde9a54f6596f2f87f866d30b908e062b5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797425"
---
# <a name="locpinx-cell-shape-transform-section"></a><span data-ttu-id="5c50a-104">Zelle "LocPinX" (Abschnitt "Shape Transform")</span><span class="sxs-lookup"><span data-stu-id="5c50a-104">LocPinX Cell (Shape Transform Section)</span></span>

<span data-ttu-id="5c50a-105">Stellt die *X* --Koordinate der Drehbezugspunkts (Drehmittelpunkts) im Verhältnis zum Ursprung des Shapes.</span><span class="sxs-lookup"><span data-stu-id="5c50a-105">Represents the  *x*  -coordinate of the shape's pin (center of rotation) in relation to the origin of the shape.</span></span> <span data-ttu-id="5c50a-106">Die Standardformel zum Bestimmen von LocPinX lautet:</span><span class="sxs-lookup"><span data-stu-id="5c50a-106">The default formula for determining LocPinX is:</span></span> 
  
<span data-ttu-id="5c50a-107">= Breite \* 0,5</span><span class="sxs-lookup"><span data-stu-id="5c50a-107">= Width \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5c50a-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5c50a-108">Remarks</span></span>

<span data-ttu-id="5c50a-109">Wenn Sie einen Verweis auf die Zelle LocPinX nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="5c50a-109">To get a reference to the LocPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5c50a-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="5c50a-110">Cell name:</span></span>  <br/> | <span data-ttu-id="5c50a-111">LocPinX</span><span class="sxs-lookup"><span data-stu-id="5c50a-111">LocPinX</span></span>  <br/> |
   
<span data-ttu-id="5c50a-112">Wenn Sie einen Verweis auf die Zelle LocPinX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="5c50a-112">To get a reference to the LocPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5c50a-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="5c50a-113">Section index:</span></span>  <br/> |<span data-ttu-id="5c50a-114">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5c50a-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5c50a-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="5c50a-115">Row index:</span></span>  <br/> |<span data-ttu-id="5c50a-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="5c50a-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="5c50a-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="5c50a-117">Cell index:</span></span>  <br/> |<span data-ttu-id="5c50a-118">**visXFormLocPinX**</span><span class="sxs-lookup"><span data-stu-id="5c50a-118">**visXFormLocPinX**</span></span> <br/> |
   

