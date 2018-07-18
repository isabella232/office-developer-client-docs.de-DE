---
title: Zelle "NoLine" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm715
localization_priority: Normal
ms.assetid: f9624af2-c087-3dde-9140-339c438b3652
description: Legt fest, ob eine Linie um die Grenze des Pfads gezogen wird.
ms.openlocfilehash: 1e43072363461e6b8fcd511c70512f3bfef4504f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797541"
---
# <a name="noline-cell-geometry-section"></a><span data-ttu-id="10b89-103">NoLine Cell (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="10b89-103">NoLine Cell (Geometry Section)</span></span>

<span data-ttu-id="10b89-104">Legt fest, ob eine Linie um die Grenze des Pfads gezogen wird.</span><span class="sxs-lookup"><span data-stu-id="10b89-104">Determines whether a line is drawn around the boundary of the path.</span></span>
  
|<span data-ttu-id="10b89-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="10b89-105">**Value**</span></span>|<span data-ttu-id="10b89-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="10b89-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="10b89-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="10b89-107">TRUE</span></span>  <br/> | <span data-ttu-id="10b89-108">Es wird keine Linie um die Grenze eines Pfads gezogen, bei der es sich um die Grenze eines ausgefüllten Bereichs handelt.</span><span class="sxs-lookup"><span data-stu-id="10b89-108">A line is not drawn around the boundary of the path that is the boundary of a filled region.</span></span>  <br/> |
| <span data-ttu-id="10b89-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="10b89-109">FALSE</span></span>  <br/> | <span data-ttu-id="10b89-110">Es wird eine Linie um die Grenze eines Pfades gezogen.</span><span class="sxs-lookup"><span data-stu-id="10b89-110">A line is drawn around the boundary of a path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10b89-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="10b89-111">Remarks</span></span>

<span data-ttu-id="10b89-p101">Wenn Sie die Farbe einer Linie in weiß ändern, ist diese Linie immer noch vorhanden, auch wenn sie vor einem weißen Hintergrund nicht mehr angezeigt wird. Wenn Sie in diese Zelle den Wert WAHR einsetzen, wird keine Linie gezogen.</span><span class="sxs-lookup"><span data-stu-id="10b89-p101">When you change the color of a line to white, the line still exists even though you can't see it on a white background. When you set the value of this cell to TRUE, no line is drawn.</span></span>
  
<span data-ttu-id="10b89-114">Wenn Sie einen Verweis auf die Zelle NoLine aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="10b89-114">To get a reference to the NoLine cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="10b89-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="10b89-115">Cell name:</span></span>  <br/> | <span data-ttu-id="10b89-116">Geometrie *i* . NoLine wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="10b89-116">Geometry  *i*  .NoLine            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="10b89-117">Wenn Sie einen Verweis auf die Zelle NoLine aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="10b89-117">To get a reference to the NoLine cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="10b89-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="10b89-118">Section index:</span></span>  <br/> |<span data-ttu-id="10b89-119">**VisSectionFirstComponent** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="10b89-119">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="10b89-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="10b89-120">Row index:</span></span>  <br/> |<span data-ttu-id="10b89-121">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="10b89-121">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="10b89-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="10b89-122">Cell index:</span></span>  <br/> |<span data-ttu-id="10b89-123">**visCompNoLine**</span><span class="sxs-lookup"><span data-stu-id="10b89-123">**visCompNoLine**</span></span> <br/> |
   

