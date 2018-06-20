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
ms.openlocfilehash: 443a229058a9ca910ba5b38b093706c9c2e3e95b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796651"
---
# <a name="comment-cell-annotation-section"></a><span data-ttu-id="e8849-103">Zelle "Comment" (Abschnitt "Annotation")</span><span class="sxs-lookup"><span data-stu-id="e8849-103">Comment Cell (Annotation Section)</span></span>

<span data-ttu-id="e8849-104">Enthält den in einem Kommentar enthaltenen Text.</span><span class="sxs-lookup"><span data-stu-id="e8849-104">Contains the text that appears in a comment.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e8849-105">Diese Zelle wird für Kommentare zur Überwachung nur, wenn eine VSD-Datei in Microsoft Visio 2013 öffnen oder eine vsdx-Datei im VSD-Format speichern.</span><span class="sxs-lookup"><span data-stu-id="e8849-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="e8849-106">Es wird nicht zum Nachverfolgen von Kommentaren in .vsdx Dokumente in Visio 2013 verwendet.</span><span class="sxs-lookup"><span data-stu-id="e8849-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e8849-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e8849-107">Remarks</span></span>

<span data-ttu-id="e8849-108">Wenn Sie einen Verweis auf die Zelle Comment nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e8849-108">To get a reference to the Comment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e8849-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="e8849-109">Cell name:</span></span>  <br/> | <span data-ttu-id="e8849-110">Annotation.Comment [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="e8849-110">Annotation.Comment[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="e8849-111">Wenn Sie einen Verweis auf die Zelle Comment aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="e8849-111">To get a reference to the Comment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e8849-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="e8849-112">Section index:</span></span>  <br/> |<span data-ttu-id="e8849-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="e8849-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="e8849-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="e8849-114">Row index:</span></span>  <br/> |<span data-ttu-id="e8849-115">**VisRowAnnotation** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e8849-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e8849-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="e8849-116">Cell index:</span></span>  <br/> |<span data-ttu-id="e8849-117">**visAnnotationComment**</span><span class="sxs-lookup"><span data-stu-id="e8849-117">**visAnnotationComment**</span></span> <br/> |
   

