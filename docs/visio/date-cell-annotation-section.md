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
# <a name="date-cell-annotation-section"></a><span data-ttu-id="ed084-103">Zelle "Date" (Abschnitt "Annotation")</span><span class="sxs-lookup"><span data-stu-id="ed084-103">Date Cell (Annotation Section)</span></span>

<span data-ttu-id="ed084-104">Enthält Datum und Uhrzeit der letzten Bearbeitung des Kommentars.</span><span class="sxs-lookup"><span data-stu-id="ed084-104">Contains the date and time the comment was last edited.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ed084-105">Diese Zelle wird zum Nachverfolgen von Kommentaren nur beim Öffnen einer VSD-Datei in Microsoft Visio 2013 oder beim Speichern einer. vsdx-Datei im VSD-Dateiformat verwendet.</span><span class="sxs-lookup"><span data-stu-id="ed084-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="ed084-106">Sie wird nicht zum Nachverfolgen von Kommentaren in vsdx-Dokumenten in Visio 2013 verwendet.</span><span class="sxs-lookup"><span data-stu-id="ed084-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ed084-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed084-107">Remarks</span></span>

<span data-ttu-id="ed084-108">Auf der Benutzeroberfläche wird im Kommentarfeld nur das Datum angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ed084-108">Only the date appears in the comment box in the user interface.</span></span>
  
<span data-ttu-id="ed084-109">Wenn Sie einen Verweis auf die Zelle Date aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ed084-109">To get a reference to the Date cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ed084-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ed084-110">Cell name:</span></span>  <br/> | <span data-ttu-id="ed084-111">Annotation. Date [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="ed084-111">Annotation.Date[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="ed084-112">Wenn Sie einen Verweis auf die Zelle Date nach Index aus einem Programm abrufen möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="ed084-112">To get a reference to the Date cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ed084-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ed084-113">Section index:</span></span>  <br/> |<span data-ttu-id="ed084-114">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="ed084-114">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="ed084-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ed084-115">Row index:</span></span>  <br/> |<span data-ttu-id="ed084-116">**visRowAnnotation** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ed084-116">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="ed084-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ed084-117">Cell index:</span></span>  <br/> |<span data-ttu-id="ed084-118">**visAnnotationDate**</span><span class="sxs-lookup"><span data-stu-id="ed084-118">**visAnnotationDate**</span></span> <br/> |
   

