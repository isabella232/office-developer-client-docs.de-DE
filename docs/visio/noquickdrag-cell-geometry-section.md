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
description: Bestimmt, ob ein Shape ausgewählt oder gezogen werden, wenn der Benutzer den vom Abschnitt "Geometrie" definierten ausgefüllten Bereich klickt werden kann.
ms.openlocfilehash: 7d4ffd876d8676af885b8f750fecf6f6d0deaa9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797555"
---
# <a name="noquickdrag-cell-geometry-section"></a><span data-ttu-id="48b9c-103">NoQuickDrag Cell (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="48b9c-103">NoQuickDrag Cell (Geometry Section)</span></span>

<span data-ttu-id="48b9c-104">Bestimmt, ob ein Shape ausgewählt oder gezogen werden, wenn der Benutzer den vom Abschnitt "Geometrie" definierten ausgefüllten Bereich klickt werden kann.</span><span class="sxs-lookup"><span data-stu-id="48b9c-104">Determines whether a shape can be selected or dragged when the user clicks the filled area defined by the Geometry section.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="48b9c-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48b9c-105">Remarks</span></span>

<span data-ttu-id="48b9c-106">Wenn Sie eine Referenz auf die Zelle NoQuickDrag aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes.</span><span class="sxs-lookup"><span data-stu-id="48b9c-106">To get a reference to the NoQuickDrag cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="48b9c-107">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="48b9c-107">Cell name:</span></span>  <br/> |<span data-ttu-id="48b9c-108">Geometrie *i* . NoQuickDrag, wobei * ich * - < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="48b9c-108">Geometry  *i*  .NoQuickDrag, where  * i *  - <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="48b9c-109">Wenn Sie eine Referenz auf die Zelle NoQuickDrag aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="48b9c-109">To get a reference to the NoQuickDrag cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="48b9c-110">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="48b9c-110">Section index:</span></span>  <br/> |<span data-ttu-id="48b9c-111">**VisSectionFirstComponent** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="48b9c-111">**visSectionFirstComponent** +  *i*  , where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="48b9c-112">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="48b9c-112">Row index:</span></span>  <br/> |<span data-ttu-id="48b9c-113">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="48b9c-113">**visRowComponent**</span></span> <br/> |
|<span data-ttu-id="48b9c-114">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="48b9c-114">Cell index:</span></span>  <br/> |<span data-ttu-id="48b9c-115">**visCompNoQuickDrag**</span><span class="sxs-lookup"><span data-stu-id="48b9c-115">**visCompNoQuickDrag**</span></span> <br/> |
   

