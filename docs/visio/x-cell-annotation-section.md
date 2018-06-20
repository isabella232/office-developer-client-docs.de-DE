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
description: Die x - Koordinate des kommentarmarkers in Seitenkoordinaten.
ms.openlocfilehash: 454c28c6f15c705148155751d533a516aae7d2d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798422"
---
# <a name="x-cell-annotation-section"></a><span data-ttu-id="af447-103">Zelle "X" (Abschnitt "Annotation")</span><span class="sxs-lookup"><span data-stu-id="af447-103">X Cell (Annotation Section)</span></span>

<span data-ttu-id="af447-104">Die *X* -Koordinate des kommentarmarkers in Seitenkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="af447-104">The  *x*  -coordinate of the comment marker in page coordinates.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="af447-105">Diese Zelle wird für Kommentare zur Überwachung nur, wenn eine VSD-Datei in Microsoft Visio 2013 öffnen oder eine vsdx-Datei im VSD-Format speichern.</span><span class="sxs-lookup"><span data-stu-id="af447-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="af447-106">Es wird nicht zum Nachverfolgen von Kommentaren in .vsdx Dokumente in Visio 2013 verwendet.</span><span class="sxs-lookup"><span data-stu-id="af447-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="af447-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="af447-107">Remarks</span></span>

<span data-ttu-id="af447-108">Wenn Sie einen Verweis auf die Zelle X nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="af447-108">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="af447-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="af447-109">Cell name:</span></span>  <br/> | <span data-ttu-id="af447-110">Annotation.X [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="af447-110">Annotation.X[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="af447-111">Wenn Sie einen Verweis auf die Zelle X aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="af447-111">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="af447-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="af447-112">Section index:</span></span>  <br/> |<span data-ttu-id="af447-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="af447-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="af447-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="af447-114">Row index:</span></span>  <br/> |<span data-ttu-id="af447-115">**VisRowAnnotation** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="af447-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="af447-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="af447-116">Cell index:</span></span>  <br/> |<span data-ttu-id="af447-117">**visAnnotationX**</span><span class="sxs-lookup"><span data-stu-id="af447-117">**visAnnotationX**</span></span> <br/> |
   

