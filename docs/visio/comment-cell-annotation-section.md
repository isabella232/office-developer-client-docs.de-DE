---
title: Zelle "Comment" (Abschnitt "Annotation")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60033
localization_priority: Normal
ms.assetid: b367841a-f31c-4b55-4491-2abab5811dbe
description: Enthält den in einem Kommentar enthaltenen Text.
ms.openlocfilehash: fd9dce2618c0b8c967b794b0beea8b772a231003
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415530"
---
# <a name="comment-cell-annotation-section"></a><span data-ttu-id="2ee8b-103">Zelle "Comment" (Abschnitt "Annotation")</span><span class="sxs-lookup"><span data-stu-id="2ee8b-103">Comment Cell (Annotation Section)</span></span>

<span data-ttu-id="2ee8b-104">Enthält den in einem Kommentar enthaltenen Text.</span><span class="sxs-lookup"><span data-stu-id="2ee8b-104">Contains the text that appears in a comment.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2ee8b-105">Diese Zelle wird nur zum Nachverfolgen von Kommentaren verwendet, wenn Sie eine VSD-Datei in Microsoft Visio 2013 öffnen oder eine VSDX-Datei im VSD-Dateiformat speichern.</span><span class="sxs-lookup"><span data-stu-id="2ee8b-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="2ee8b-106">Es wird nicht zum Nachverfolgen von Kommentaren in VSDX-Dokumenten in Visio 2013 verwendet.</span><span class="sxs-lookup"><span data-stu-id="2ee8b-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2ee8b-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2ee8b-107">Remarks</span></span>

<span data-ttu-id="2ee8b-108">Um einen Verweis auf die Zelle Comment anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="2ee8b-108">To get a reference to the Comment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2ee8b-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2ee8b-109">Cell name:</span></span>  <br/> | <span data-ttu-id="2ee8b-110">Annotation.Comment[  *i*  ] where  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="2ee8b-110">Annotation.Comment[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="2ee8b-111">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Comment nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="2ee8b-111">To get a reference to the Comment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2ee8b-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2ee8b-112">Section index:</span></span>  <br/> |<span data-ttu-id="2ee8b-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="2ee8b-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="2ee8b-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2ee8b-114">Row index:</span></span>  <br/> |<span data-ttu-id="2ee8b-115">**visRowAnnotation**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2ee8b-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="2ee8b-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2ee8b-116">Cell index:</span></span>  <br/> |<span data-ttu-id="2ee8b-117">**visAnnotationComment**</span><span class="sxs-lookup"><span data-stu-id="2ee8b-117">**visAnnotationComment**</span></span> <br/> |
   

