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
description: 'Stellt die x-Koordinate der PIN des Shapes (Drehmittelpunkt) im Verhältnis zum Ursprung der Form dar. Die Standardformel für die Bestimmung von Zelle LocPinX lautet:'
ms.openlocfilehash: 2eb5c328eed3c97652173670c426b83b8c358833
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358051"
---
# <a name="locpinx-cell-shape-transform-section"></a><span data-ttu-id="bf214-104">Zelle "LocPinX" (Abschnitt "Shape Transform")</span><span class="sxs-lookup"><span data-stu-id="bf214-104">LocPinX Cell (Shape Transform Section)</span></span>

<span data-ttu-id="bf214-105">Stellt die *x* -Koordinate der PIN des Shapes (Drehmittelpunkt) im Verhältnis zum Ursprung der Form dar.</span><span class="sxs-lookup"><span data-stu-id="bf214-105">Represents the  *x*  -coordinate of the shape's pin (center of rotation) in relation to the origin of the shape.</span></span> <span data-ttu-id="bf214-106">Die Standardformel für die Bestimmung von Zelle LocPinX lautet:</span><span class="sxs-lookup"><span data-stu-id="bf214-106">The default formula for determining LocPinX is:</span></span> 
  
<span data-ttu-id="bf214-107">= Breite \* 0,5</span><span class="sxs-lookup"><span data-stu-id="bf214-107">= Width \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bf214-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf214-108">Remarks</span></span>

<span data-ttu-id="bf214-109">Wenn Sie einen Verweis auf die Zelle Zelle LocPinX aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="bf214-109">To get a reference to the LocPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bf214-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="bf214-110">Cell name:</span></span>  <br/> | <span data-ttu-id="bf214-111">Zelle LocPinX</span><span class="sxs-lookup"><span data-stu-id="bf214-111">LocPinX</span></span>  <br/> |
   
<span data-ttu-id="bf214-112">Wenn Sie einen Verweis auf die Zelle Zelle LocPinX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="bf214-112">To get a reference to the LocPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bf214-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="bf214-113">Section index:</span></span>  <br/> |<span data-ttu-id="bf214-114">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bf214-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bf214-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="bf214-115">Row index:</span></span>  <br/> |<span data-ttu-id="bf214-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="bf214-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="bf214-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="bf214-117">Cell index:</span></span>  <br/> |<span data-ttu-id="bf214-118">**visXFormLocPinX**</span><span class="sxs-lookup"><span data-stu-id="bf214-118">**visXFormLocPinX**</span></span> <br/> |
   

