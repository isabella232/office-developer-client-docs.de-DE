---
title: Zelle "NoQuickDrag" (Abschnitt "Geometrie")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80004
localization_priority: Normal
ms.assetid: 8491f459-9de2-8e75-5532-7d3bd0986734
description: Bestimmt, ob ein Shape ausgewählt oder gezogen werden kann, wenn der Benutzer auf den durch den Abschnitt Geometrie definierten gefüllten Bereich klickt.
ms.openlocfilehash: d60268685d93ae88abb2840f62b093db1e688c2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417721"
---
# <a name="noquickdrag-cell-geometry-section"></a><span data-ttu-id="95012-103">Zelle "NoQuickDrag" (Abschnitt "Geometrie")</span><span class="sxs-lookup"><span data-stu-id="95012-103">NoQuickDrag Cell (Geometry Section)</span></span>

<span data-ttu-id="95012-104">Bestimmt, ob ein Shape ausgewählt oder gezogen werden kann, wenn der Benutzer auf den durch den Abschnitt Geometrie definierten gefüllten Bereich klickt.</span><span class="sxs-lookup"><span data-stu-id="95012-104">Determines whether a shape can be selected or dragged when the user clicks the filled area defined by the Geometry section.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="95012-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95012-105">Remarks</span></span>

<span data-ttu-id="95012-106">Wenn Sie einen Verweis auf die Zelle NoQuickDrag aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="95012-106">To get a reference to the NoQuickDrag cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="95012-107">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="95012-107">Cell name:</span></span>  <br/> |<span data-ttu-id="95012-108">Geometrie *i* . NoQuickDrag, wobei \* i \*-<1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="95012-108">Geometry  *i*  .NoQuickDrag, where  \* i \*  - <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="95012-109">Wenn Sie einen Verweis auf die Zelle NoQuickDrag aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="95012-109">To get a reference to the NoQuickDrag cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="95012-110">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="95012-110">Section index:</span></span>  <br/> |<span data-ttu-id="95012-111">**visSectionFirstComponent** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="95012-111">**visSectionFirstComponent** +  *i*  , where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="95012-112">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="95012-112">Row index:</span></span>  <br/> |<span data-ttu-id="95012-113">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="95012-113">**visRowComponent**</span></span> <br/> |
|<span data-ttu-id="95012-114">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="95012-114">Cell index:</span></span>  <br/> |<span data-ttu-id="95012-115">**visCompNoQuickDrag**</span><span class="sxs-lookup"><span data-stu-id="95012-115">**visCompNoQuickDrag**</span></span> <br/> |
   

