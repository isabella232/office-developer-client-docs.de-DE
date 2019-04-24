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
description: 'Stellt die y-Koordinate der PIN des Shapes (Drehmittelpunkt) im Verhältnis zum Ursprung der Form dar. Die Standardformel für die Bestimmung von Zelle LocPinY lautet:'
ms.openlocfilehash: e65bfec8fdcf2be1ee92c23b7afcb183c95ea9fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358044"
---
# <a name="locpiny-cell-shape-transform-section"></a><span data-ttu-id="aad09-104">Zelle "LocPinY" (Abschnitt "Shape Transform")</span><span class="sxs-lookup"><span data-stu-id="aad09-104">LocPinY Cell (Shape Transform Section)</span></span>

<span data-ttu-id="aad09-105">Stellt die *y* -Koordinate der PIN des Shapes (Drehmittelpunkt) im Verhältnis zum Ursprung der Form dar.</span><span class="sxs-lookup"><span data-stu-id="aad09-105">Represents the  *y*  -coordinate of the shape's pin (center of rotation) in relation to the origin of the shape.</span></span> <span data-ttu-id="aad09-106">Die Standardformel für die Bestimmung von Zelle LocPinY lautet:</span><span class="sxs-lookup"><span data-stu-id="aad09-106">The default formula for determining LocPinY is:</span></span> 
  
<span data-ttu-id="aad09-107">= Höhe \* 0,5</span><span class="sxs-lookup"><span data-stu-id="aad09-107">= Height \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aad09-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aad09-108">Remarks</span></span>

<span data-ttu-id="aad09-109">Wenn Sie einen Verweis auf die Zelle Zelle LocPinY aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="aad09-109">To get a reference to the LocPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aad09-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="aad09-110">Cell name:</span></span>  <br/> | <span data-ttu-id="aad09-111">Zelle LocPinY</span><span class="sxs-lookup"><span data-stu-id="aad09-111">LocPinY</span></span>  <br/> |
   
<span data-ttu-id="aad09-112">Wenn Sie einen Verweis auf die Zelle Zelle LocPinY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="aad09-112">To get a reference to the LocPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aad09-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="aad09-113">Section index:</span></span>  <br/> |<span data-ttu-id="aad09-114">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="aad09-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="aad09-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="aad09-115">Row index:</span></span>  <br/> |<span data-ttu-id="aad09-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="aad09-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="aad09-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="aad09-117">Cell index:</span></span>  <br/> |<span data-ttu-id="aad09-118">**visXFormLocPinY**</span><span class="sxs-lookup"><span data-stu-id="aad09-118">**visXFormLocPinY**</span></span> <br/> |
   

