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
ms.openlocfilehash: ad3744ae8deb4ffb4dd2282e50590439c4b218a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433752"
---
# <a name="noline-cell-geometry-section"></a><span data-ttu-id="5067a-103">Zelle "NoLine" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="5067a-103">NoLine Cell (Geometry Section)</span></span>

<span data-ttu-id="5067a-104">Legt fest, ob eine Linie um die Grenze des Pfads gezogen wird.</span><span class="sxs-lookup"><span data-stu-id="5067a-104">Determines whether a line is drawn around the boundary of the path.</span></span>
  
|<span data-ttu-id="5067a-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="5067a-105">**Value**</span></span>|<span data-ttu-id="5067a-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5067a-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5067a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="5067a-107">TRUE</span></span>  <br/> | <span data-ttu-id="5067a-108">Es wird keine Linie um die Grenze eines Pfads gezogen, bei der es sich um die Grenze eines ausgefüllten Bereichs handelt.</span><span class="sxs-lookup"><span data-stu-id="5067a-108">A line is not drawn around the boundary of the path that is the boundary of a filled region.</span></span>  <br/> |
| <span data-ttu-id="5067a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="5067a-109">FALSE</span></span>  <br/> | <span data-ttu-id="5067a-110">Es wird eine Linie um die Grenze eines Pfades gezogen.</span><span class="sxs-lookup"><span data-stu-id="5067a-110">A line is drawn around the boundary of a path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5067a-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5067a-111">Remarks</span></span>

<span data-ttu-id="5067a-p101">Wenn Sie die Farbe einer Linie in weiß ändern, ist diese Linie immer noch vorhanden, auch wenn sie vor einem weißen Hintergrund nicht mehr angezeigt wird. Wenn Sie in diese Zelle den Wert WAHR einsetzen, wird keine Linie gezogen.</span><span class="sxs-lookup"><span data-stu-id="5067a-p101">When you change the color of a line to white, the line still exists even though you can't see it on a white background. When you set the value of this cell to TRUE, no line is drawn.</span></span>
  
<span data-ttu-id="5067a-114">Um einen Verweis auf die Zelle NoLine anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="5067a-114">To get a reference to the NoLine cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5067a-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="5067a-115">Cell name:</span></span>  <br/> | <span data-ttu-id="5067a-116">Geometry  *i*  . NoLine,  *wobei i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="5067a-116">Geometry  *i*  .NoLine            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="5067a-117">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle NoLine nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="5067a-117">To get a reference to the NoLine cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5067a-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="5067a-118">Section index:</span></span>  <br/> |<span data-ttu-id="5067a-119">**visSectionFirstComponent**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="5067a-119">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="5067a-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="5067a-120">Row index:</span></span>  <br/> |<span data-ttu-id="5067a-121">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="5067a-121">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="5067a-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="5067a-122">Cell index:</span></span>  <br/> |<span data-ttu-id="5067a-123">**visCompNoLine**</span><span class="sxs-lookup"><span data-stu-id="5067a-123">**visCompNoLine**</span></span> <br/> |
   

