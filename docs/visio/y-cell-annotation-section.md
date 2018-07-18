---
title: Zelle "Y" (Abschnitt "Annotation")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60095
localization_priority: Normal
ms.assetid: 527a4615-2013-a4b4-81cd-7f5d71c1803c
description: Die y-Koordinate des kommentarmarkers in Seitenkoordinaten.
ms.openlocfilehash: cc2399de7919512796a39ca39c705c214f4c51a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798448"
---
# <a name="y-cell-annotation-section"></a><span data-ttu-id="50479-103">Y Cell (Annotation Section)</span><span class="sxs-lookup"><span data-stu-id="50479-103">Y Cell (Annotation Section)</span></span>

<span data-ttu-id="50479-104">Die *y* -Koordinate des kommentarmarkers in Seitenkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="50479-104">The  *y*  -coordinate of the comment marker in page coordinates.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="50479-105">Diese Zelle wird für Kommentare zur Überwachung nur, wenn eine VSD-Datei in Microsoft Visio 2013 öffnen oder eine vsdx-Datei im VSD-Format speichern.</span><span class="sxs-lookup"><span data-stu-id="50479-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="50479-106">Es wird nicht zum Nachverfolgen von Kommentaren in .vsdx Dokumente in Visio 2013 verwendet.</span><span class="sxs-lookup"><span data-stu-id="50479-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="50479-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50479-107">Remarks</span></span>

<span data-ttu-id="50479-108">Wenn Sie einen Verweis auf die Zelle Y aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="50479-108">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="50479-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="50479-109">Cell name:</span></span>  <br/> | <span data-ttu-id="50479-110">Annotation.Y [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="50479-110">Annotation.Y [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="50479-111">Wenn Sie einen Verweis auf die Zelle Y aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="50479-111">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="50479-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="50479-112">Section index:</span></span>  <br/> |<span data-ttu-id="50479-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="50479-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="50479-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="50479-114">Row index:</span></span>  <br/> |<span data-ttu-id="50479-115">**VisRowAnnotation** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="50479-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="50479-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="50479-116">Cell index:</span></span>  <br/> |<span data-ttu-id="50479-117">**visAnnotationY**</span><span class="sxs-lookup"><span data-stu-id="50479-117">**visAnnotationY**</span></span> <br/> |
   

