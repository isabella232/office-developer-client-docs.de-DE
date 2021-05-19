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
ms.openlocfilehash: 5c9b3cbf96e2a218a8ed790d3a5615843360c95e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423566"
---
# <a name="e-cell-geometry-section"></a><span data-ttu-id="66bb5-103">Zelle "E" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="66bb5-103">E Cell (Geometry Section)</span></span>

<span data-ttu-id="66bb5-104">Enthält die Formel eines nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-Spline, NURBS).</span><span class="sxs-lookup"><span data-stu-id="66bb5-104">Contains a nonuniform rational B-spline (NURBS) formula.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="66bb5-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="66bb5-105">Remarks</span></span>

<span data-ttu-id="66bb5-106">Um einen Verweis auf die Zelle E anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="66bb5-106">To get a reference to the E cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="66bb5-107">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="66bb5-107">Cell name:</span></span>  <br/> | <span data-ttu-id="66bb5-108">Geometry  *i*  . E  *j,*            *wobei i*  und  *j*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="66bb5-108">Geometry  *i*  .E  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="66bb5-109">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle E nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="66bb5-109">To get a reference to the E cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="66bb5-110">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="66bb5-110">Section index:</span></span>  <br/> |<span data-ttu-id="66bb5-111">**visSectionFirstComponent**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="66bb5-111">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="66bb5-112">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="66bb5-112">Row index:</span></span>  <br/> |<span data-ttu-id="66bb5-113">**visRowVertex**  +   *j,* *wobei j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="66bb5-113">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="66bb5-114">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="66bb5-114">Cell index:</span></span>  <br/> |<span data-ttu-id="66bb5-115">**visNURBSData**</span><span class="sxs-lookup"><span data-stu-id="66bb5-115">**visNURBSData**</span></span> <br/> |
   

