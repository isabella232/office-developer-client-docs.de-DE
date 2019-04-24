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
description: Die y-Koordinate des Kommentarmarkers in Seitenkoordinaten.
ms.openlocfilehash: 48a37c261078cd1000331920b33549cee2c1da03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360123"
---
# <a name="y-cell-annotation-section"></a><span data-ttu-id="0fffb-103">Zelle "Y" (Abschnitt "Annotation")</span><span class="sxs-lookup"><span data-stu-id="0fffb-103">Y Cell (Annotation Section)</span></span>

<span data-ttu-id="0fffb-104">Die *y* -Koordinate des Kommentarmarkers in Seitenkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="0fffb-104">The  *y*  -coordinate of the comment marker in page coordinates.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0fffb-105">Diese Zelle wird zum Nachverfolgen von Kommentaren nur beim Öffnen einer VSD-Datei in Microsoft Visio 2013 oder beim Speichern einer. vsdx-Datei im VSD-Dateiformat verwendet.</span><span class="sxs-lookup"><span data-stu-id="0fffb-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="0fffb-106">Sie wird nicht zum Nachverfolgen von Kommentaren in vsdx-Dokumenten in Visio 2013 verwendet.</span><span class="sxs-lookup"><span data-stu-id="0fffb-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0fffb-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0fffb-107">Remarks</span></span>

<span data-ttu-id="0fffb-108">Wenn Sie einen Verweis auf die Zelle Y aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="0fffb-108">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0fffb-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="0fffb-109">Cell name:</span></span>  <br/> | <span data-ttu-id="0fffb-110">Annotation. Y [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="0fffb-110">Annotation.Y [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="0fffb-111">Wenn Sie einen Verweis auf die Zelle Y nach Index aus einem Programm erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="0fffb-111">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0fffb-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="0fffb-112">Section index:</span></span>  <br/> |<span data-ttu-id="0fffb-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="0fffb-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="0fffb-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="0fffb-114">Row index:</span></span>  <br/> |<span data-ttu-id="0fffb-115">**visRowAnnotation** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="0fffb-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="0fffb-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="0fffb-116">Cell index:</span></span>  <br/> |<span data-ttu-id="0fffb-117">**visAnnotationY**</span><span class="sxs-lookup"><span data-stu-id="0fffb-117">**visAnnotationY**</span></span> <br/> |
   

