---
title: Zelle "NoFill" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm710
localization_priority: Normal
ms.assetid: 0ba7f6da-681b-b749-fe72-afbca23d7e16
description: Gibt an, ob ein Pfad gefüllt werden kann.
ms.openlocfilehash: 301f30b644e338ff9e597a7a7d8226b9c8a4462f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415019"
---
# <a name="nofill-cell-geometry-section"></a><span data-ttu-id="ed97a-103">Zelle "NoFill" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="ed97a-103">NoFill Cell (Geometry Section)</span></span>

<span data-ttu-id="ed97a-104">Gibt an, ob ein Pfad gefüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ed97a-104">Indicates whether a path can be filled.</span></span>
  
|<span data-ttu-id="ed97a-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ed97a-105">**Value**</span></span>|<span data-ttu-id="ed97a-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ed97a-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ed97a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="ed97a-107">TRUE</span></span>  <br/> | <span data-ttu-id="ed97a-108">Der Pfad ist nicht gefüllt, auch wenn andere Pfade im Shape gefüllt sind.</span><span class="sxs-lookup"><span data-stu-id="ed97a-108">The path is not filled even if other paths in the shape are filled.</span></span>  <br/> |
| <span data-ttu-id="ed97a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="ed97a-109">FALSE</span></span>  <br/> | <span data-ttu-id="ed97a-110">Die Füllung des Shapes gilt für den Pfad, auch wenn dieser nicht geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="ed97a-110">The shape's fill applies to the path, even if it isn't closed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed97a-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ed97a-111">Remarks</span></span>

<span data-ttu-id="ed97a-p101">Wenn Sie das Füllmuster eines Shapes auf Null (=) setzen, wird keiner der Pfade gefüllt. Diese Zelle wird verwendet, um die Füllung für einen Pfad in einem Shape bei Bedarf auszuschalten.</span><span class="sxs-lookup"><span data-stu-id="ed97a-p101">If you set a shape's fill pattern to none (0), none of its paths are filled. This cell is used to turn the fill off selectively for a path within a shape.</span></span>
  
<span data-ttu-id="ed97a-114">Um einen Verweis auf die Zelle NoFill anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="ed97a-114">To get a reference to the NoFill cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ed97a-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ed97a-115">Cell name:</span></span>  <br/> | <span data-ttu-id="ed97a-116">Geometry  *i*  . NoFill,  *wobei i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="ed97a-116">Geometry  *i*  .NoFill            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="ed97a-117">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die NoFill-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="ed97a-117">To get a reference to the NoFill cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ed97a-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ed97a-118">Section index:</span></span>  <br/> |<span data-ttu-id="ed97a-119">**visSectionFirstComponent**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ed97a-119">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="ed97a-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ed97a-120">Row index:</span></span>  <br/> |<span data-ttu-id="ed97a-121">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="ed97a-121">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="ed97a-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="ed97a-122">Cell index:</span></span>  <br/> |<span data-ttu-id="ed97a-123">**visCompNoFill**</span><span class="sxs-lookup"><span data-stu-id="ed97a-123">**visCompNoFill**</span></span> <br/> |
   

