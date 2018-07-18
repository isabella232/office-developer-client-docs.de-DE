---
title: Zelle "Date" (Abschnitt "Annotation")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60036
localization_priority: Normal
ms.assetid: f1f11803-614b-a40d-0a2d-131093e7609e
description: Enthält Datum und Uhrzeit der letzten Bearbeitung des Kommentars.
ms.openlocfilehash: 4b6e7ea70302b10728d82f36ad0db39077af9523
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796804"
---
# <a name="date-cell-annotation-section"></a><span data-ttu-id="6b2a8-103">Date Cell (Annotation Section)</span><span class="sxs-lookup"><span data-stu-id="6b2a8-103">Date Cell (Annotation Section)</span></span>

<span data-ttu-id="6b2a8-104">Enthält Datum und Uhrzeit der letzten Bearbeitung des Kommentars.</span><span class="sxs-lookup"><span data-stu-id="6b2a8-104">Contains the date and time the comment was last edited.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6b2a8-105">Diese Zelle wird für Kommentare zur Überwachung nur, wenn eine VSD-Datei in Microsoft Visio 2013 öffnen oder eine vsdx-Datei im VSD-Format speichern.</span><span class="sxs-lookup"><span data-stu-id="6b2a8-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="6b2a8-106">Es wird nicht zum Nachverfolgen von Kommentaren in .vsdx Dokumente in Visio 2013 verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b2a8-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6b2a8-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6b2a8-107">Remarks</span></span>

<span data-ttu-id="6b2a8-108">Auf der Benutzeroberfläche wird im Kommentarfeld nur das Datum angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6b2a8-108">Only the date appears in the comment box in the user interface.</span></span>
  
<span data-ttu-id="6b2a8-109">Wenn Sie einen Verweis auf die Zelle Date aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6b2a8-109">To get a reference to the Date cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6b2a8-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="6b2a8-110">Cell name:</span></span>  <br/> | <span data-ttu-id="6b2a8-111">Annotation.Date [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="6b2a8-111">Annotation.Date[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="6b2a8-112">Wenn Sie einen Verweis auf die Zelle Date aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="6b2a8-112">To get a reference to the Date cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6b2a8-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="6b2a8-113">Section index:</span></span>  <br/> |<span data-ttu-id="6b2a8-114">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="6b2a8-114">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="6b2a8-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="6b2a8-115">Row index:</span></span>  <br/> |<span data-ttu-id="6b2a8-116">**VisRowAnnotation** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6b2a8-116">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="6b2a8-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="6b2a8-117">Cell index:</span></span>  <br/> |<span data-ttu-id="6b2a8-118">**visAnnotationDate**</span><span class="sxs-lookup"><span data-stu-id="6b2a8-118">**visAnnotationDate**</span></span> <br/> |
   

