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
ms.openlocfilehash: 60fd726db1056075f96519050cffa67c76977126
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423881"
---
# <a name="date-cell-annotation-section"></a><span data-ttu-id="c9997-103">Zelle "Date" (Abschnitt "Annotation")</span><span class="sxs-lookup"><span data-stu-id="c9997-103">Date Cell (Annotation Section)</span></span>

<span data-ttu-id="c9997-104">Enthält Datum und Uhrzeit der letzten Bearbeitung des Kommentars.</span><span class="sxs-lookup"><span data-stu-id="c9997-104">Contains the date and time the comment was last edited.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c9997-105">Diese Zelle wird nur zum Nachverfolgen von Kommentaren verwendet, wenn Sie eine VSD-Datei in Microsoft Visio 2013 öffnen oder eine VSDX-Datei im VSD-Dateiformat speichern.</span><span class="sxs-lookup"><span data-stu-id="c9997-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="c9997-106">Es wird nicht zum Nachverfolgen von Kommentaren in VSDX-Dokumenten in Visio 2013 verwendet.</span><span class="sxs-lookup"><span data-stu-id="c9997-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c9997-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c9997-107">Remarks</span></span>

<span data-ttu-id="c9997-108">Auf der Benutzeroberfläche wird im Kommentarfeld nur das Datum angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c9997-108">Only the date appears in the comment box in the user interface.</span></span>
  
<span data-ttu-id="c9997-109">Um einen Verweis auf die Zelle Date anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="c9997-109">To get a reference to the Date cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c9997-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="c9997-110">Cell name:</span></span>  <br/> | <span data-ttu-id="c9997-111">Annotation.Date[  *i*  ] where  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="c9997-111">Annotation.Date[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c9997-112">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Date nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="c9997-112">To get a reference to the Date cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c9997-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="c9997-113">Section index:</span></span>  <br/> |<span data-ttu-id="c9997-114">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="c9997-114">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="c9997-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="c9997-115">Row index:</span></span>  <br/> |<span data-ttu-id="c9997-116">**visRowAnnotation**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c9997-116">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c9997-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="c9997-117">Cell index:</span></span>  <br/> |<span data-ttu-id="c9997-118">**visAnnotationDate**</span><span class="sxs-lookup"><span data-stu-id="c9997-118">**visAnnotationDate**</span></span> <br/> |
   

