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
description: Die x-Koordinate der Kommentarmarkierung in Seitenkoordinaten.
ms.openlocfilehash: fdd9e2850a3285a2fcf4cc05fa056accd71052a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434480"
---
# <a name="x-cell-annotation-section"></a><span data-ttu-id="2c7ae-103">Zelle "X" (Abschnitt "Annotation")</span><span class="sxs-lookup"><span data-stu-id="2c7ae-103">X Cell (Annotation Section)</span></span>

<span data-ttu-id="2c7ae-104">Die  x-Koordinate der Kommentarmarkierung in Seitenkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="2c7ae-104">The  *x*  -coordinate of the comment marker in page coordinates.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2c7ae-105">Diese Zelle wird nur zum Nachverfolgen von Kommentaren verwendet, wenn Sie eine VSD-Datei in Microsoft Visio 2013 öffnen oder eine VSDX-Datei im VSD-Dateiformat speichern.</span><span class="sxs-lookup"><span data-stu-id="2c7ae-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="2c7ae-106">Es wird nicht zum Nachverfolgen von Kommentaren in VSDX-Dokumenten in Visio 2013 verwendet.</span><span class="sxs-lookup"><span data-stu-id="2c7ae-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2c7ae-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2c7ae-107">Remarks</span></span>

<span data-ttu-id="2c7ae-108">Um einen Verweis auf die Zelle X anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="2c7ae-108">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2c7ae-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2c7ae-109">Cell name:</span></span>  <br/> | <span data-ttu-id="2c7ae-110">Annotation.X[  *i*  ] wobei  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="2c7ae-110">Annotation.X[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="2c7ae-111">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die X-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="2c7ae-111">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2c7ae-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2c7ae-112">Section index:</span></span>  <br/> |<span data-ttu-id="2c7ae-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="2c7ae-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="2c7ae-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2c7ae-114">Row index:</span></span>  <br/> |<span data-ttu-id="2c7ae-115">**visRowAnnotation**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2c7ae-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="2c7ae-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2c7ae-116">Cell index:</span></span>  <br/> |<span data-ttu-id="2c7ae-117">**visAnnotationX**</span><span class="sxs-lookup"><span data-stu-id="2c7ae-117">**visAnnotationX**</span></span> <br/> |
   

