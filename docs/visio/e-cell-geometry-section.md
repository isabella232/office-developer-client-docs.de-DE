---
title: Zelle "E" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251761
localization_priority: Normal
ms.assetid: bc0154b1-6930-1fe0-655c-05eab2d60230
description: Enthält die Formel eines nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-Spline, NURBS).
ms.openlocfilehash: 000c4864c6ae98bfcd9e9cfdb16ff68396f63e44
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796918"
---
# <a name="e-cell-geometry-section"></a><span data-ttu-id="049c2-103">Zelle "E" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="049c2-103">E Cell (Geometry Section)</span></span>

<span data-ttu-id="049c2-104">Enthält die Formel eines nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-Spline, NURBS).</span><span class="sxs-lookup"><span data-stu-id="049c2-104">Contains a nonuniform rational B-spline (NURBS) formula.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="049c2-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="049c2-105">Remarks</span></span>

<span data-ttu-id="049c2-106">Wenn Sie einen Verweis auf die Zelle E nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="049c2-106">To get a reference to the E cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="049c2-107">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="049c2-107">Cell name:</span></span>  <br/> | <span data-ttu-id="049c2-108">Geometrie *i* . E *j* wobei *i* und *j* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="049c2-108">Geometry  *i*  .E  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="049c2-109">Wenn Sie einen Verweis auf die Zelle E aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="049c2-109">To get a reference to the E cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="049c2-110">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="049c2-110">Section index:</span></span>  <br/> |<span data-ttu-id="049c2-111">**VisSectionFirstComponent** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="049c2-111">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="049c2-112">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="049c2-112">Row index:</span></span>  <br/> |<span data-ttu-id="049c2-113">**VisRowVertex** +  *j* wobei *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="049c2-113">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="049c2-114">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="049c2-114">Cell index:</span></span>  <br/> |<span data-ttu-id="049c2-115">**visNURBSData**</span><span class="sxs-lookup"><span data-stu-id="049c2-115">**visNURBSData**</span></span> <br/> |
   

