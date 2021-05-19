---
title: Zelle "EventXFMod" (Abschnitt "Events")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251313
localization_priority: Normal
ms.assetid: b88588a2-c651-7eab-9c7a-ed78f20d1ba3
description: Eine Ereigniszelle, die ausgewertet wird, wenn die Position oder Ausrichtung eines Shapes auf der Seite transformiert wird (XF).
ms.openlocfilehash: c4ed4ddd9b255a9a52fc81349b514dbd25772c98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418533"
---
# <a name="eventxfmod-cell-events-section"></a><span data-ttu-id="b1a7a-103">Zelle "EventXFMod" (Abschnitt "Events")</span><span class="sxs-lookup"><span data-stu-id="b1a7a-103">EventXFMod Cell (Events Section)</span></span>

<span data-ttu-id="b1a7a-104">Eine Ereigniszelle, die ausgewertet wird, wenn die Position oder Ausrichtung eines Shapes auf dem Blatt transformiert wird ("XF").</span><span class="sxs-lookup"><span data-stu-id="b1a7a-104">An event cell that is evaluated when a shape's position or orientation on the page is transformed ("XF").</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b1a7a-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b1a7a-105">Remarks</span></span>

<span data-ttu-id="b1a7a-106">Ereigniszellen werden erst beim Eintreffen des Ereignisses ausgewertet, nicht beim Eingeben der Formel.</span><span class="sxs-lookup"><span data-stu-id="b1a7a-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="b1a7a-107">Um einen Verweis auf die EventXFMod-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="b1a7a-107">To get a reference to the EventXFMod cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b1a7a-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b1a7a-108">Cell name:</span></span>  <br/> | <span data-ttu-id="b1a7a-109">EventXFMod</span><span class="sxs-lookup"><span data-stu-id="b1a7a-109">EventXFMod</span></span>  <br/> |
   
<span data-ttu-id="b1a7a-110">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die EventXFMod-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="b1a7a-110">To get a reference to the EventXFMod cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b1a7a-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b1a7a-111">Section index:</span></span>  <br/> |<span data-ttu-id="b1a7a-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b1a7a-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b1a7a-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b1a7a-113">Row index:</span></span>  <br/> |<span data-ttu-id="b1a7a-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="b1a7a-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="b1a7a-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b1a7a-115">Cell index:</span></span>  <br/> |<span data-ttu-id="b1a7a-116">**visEvtCellXFMod**</span><span class="sxs-lookup"><span data-stu-id="b1a7a-116">**visEvtCellXFMod**</span></span> <br/> |
   

