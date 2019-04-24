---
title: Zelle "X" (Abschnitt "Annotation")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1028735
localization_priority: Normal
ms.assetid: f9db8623-9fcf-7037-2d11-d509f463025d
description: Die x-Koordinate des Kommentarmarkers in Seitenkoordinaten.
ms.openlocfilehash: fdd9e2850a3285a2fcf4cc05fa056accd71052a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341308"
---
# <a name="x-cell-annotation-section"></a><span data-ttu-id="8dcb6-103">Zelle "X" (Abschnitt "Annotation")</span><span class="sxs-lookup"><span data-stu-id="8dcb6-103">X Cell (Annotation Section)</span></span>

<span data-ttu-id="8dcb6-104">Die *x* -Koordinate des Kommentarmarkers in Seitenkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="8dcb6-104">The  *x*  -coordinate of the comment marker in page coordinates.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8dcb6-105">Diese Zelle wird zum Nachverfolgen von Kommentaren nur beim Öffnen einer VSD-Datei in Microsoft Visio 2013 oder beim Speichern einer. vsdx-Datei im VSD-Dateiformat verwendet.</span><span class="sxs-lookup"><span data-stu-id="8dcb6-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="8dcb6-106">Sie wird nicht zum Nachverfolgen von Kommentaren in vsdx-Dokumenten in Visio 2013 verwendet.</span><span class="sxs-lookup"><span data-stu-id="8dcb6-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8dcb6-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8dcb6-107">Remarks</span></span>

<span data-ttu-id="8dcb6-108">Wenn Sie einen Verweis auf die Zelle X aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="8dcb6-108">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8dcb6-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="8dcb6-109">Cell name:</span></span>  <br/> | <span data-ttu-id="8dcb6-110">Annotation. X [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="8dcb6-110">Annotation.X[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="8dcb6-111">Wenn Sie einen Verweis auf die Zelle X aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="8dcb6-111">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8dcb6-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="8dcb6-112">Section index:</span></span>  <br/> |<span data-ttu-id="8dcb6-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="8dcb6-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="8dcb6-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="8dcb6-114">Row index:</span></span>  <br/> |<span data-ttu-id="8dcb6-115">**visRowAnnotation** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="8dcb6-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="8dcb6-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="8dcb6-116">Cell index:</span></span>  <br/> |<span data-ttu-id="8dcb6-117">**visAnnotationX**</span><span class="sxs-lookup"><span data-stu-id="8dcb6-117">**visAnnotationX**</span></span> <br/> |
   

