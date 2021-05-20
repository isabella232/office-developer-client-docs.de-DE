---
title: Zelle "EventDblClick" (Abschnitt "Events")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251312
localization_priority: Normal
ms.assetid: ca949013-f998-1bce-39e5-ac6f68ab2392
description: Eine Ereigniszelle, die ausgewertet wird, wenn Sie auf ein Shape doppelklicken.
ms.openlocfilehash: a50e88ecd8e432629e246f7038dfcc9626725cc5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438218"
---
# <a name="eventdblclick-cell-events-section"></a><span data-ttu-id="3e650-103">Zelle "EventDblClick" (Abschnitt "Events")</span><span class="sxs-lookup"><span data-stu-id="3e650-103">EventDblClick Cell (Events Section)</span></span>

<span data-ttu-id="3e650-104">Eine Ereigniszelle, die ausgewertet wird, wenn Sie auf ein Shape doppelklicken.</span><span class="sxs-lookup"><span data-stu-id="3e650-104">An event cell that is evaluated when a shape is double-clicked.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3e650-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3e650-105">Remarks</span></span>

<span data-ttu-id="3e650-106">Ereigniszellen werden erst beim Eintreffen des Ereignisses ausgewertet, nicht beim Eingeben der Formel.</span><span class="sxs-lookup"><span data-stu-id="3e650-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="3e650-107">Um einen Verweis auf die Zelle EventDblClick anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="3e650-107">To get a reference to the EventDblClick cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3e650-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="3e650-108">Cell name:</span></span>  <br/> | <span data-ttu-id="3e650-109">EventDblClick</span><span class="sxs-lookup"><span data-stu-id="3e650-109">EventDblClick</span></span>  <br/> |
   
<span data-ttu-id="3e650-110">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die EventDblClick-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="3e650-110">To get a reference to the EventDblClick cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3e650-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="3e650-111">Section index:</span></span>  <br/> |<span data-ttu-id="3e650-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3e650-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3e650-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="3e650-113">Row index:</span></span>  <br/> |<span data-ttu-id="3e650-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="3e650-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="3e650-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="3e650-115">Cell index:</span></span>  <br/> |<span data-ttu-id="3e650-116">**visEvtCellDblClick**</span><span class="sxs-lookup"><span data-stu-id="3e650-116">**visEvtCellDblClick**</span></span> <br/> |
   

