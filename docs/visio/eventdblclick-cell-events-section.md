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
ms.openlocfilehash: 623d1d095d3269cd9c82fa8d0d6601933a163f92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796946"
---
# <a name="eventdblclick-cell-events-section"></a><span data-ttu-id="a4d11-103">Zelle "EventDblClick" (Abschnitt "Events")</span><span class="sxs-lookup"><span data-stu-id="a4d11-103">EventDblClick Cell (Events Section)</span></span>

<span data-ttu-id="a4d11-104">Eine Ereigniszelle, die ausgewertet wird, wenn Sie auf ein Shape doppelklicken.</span><span class="sxs-lookup"><span data-stu-id="a4d11-104">An event cell that is evaluated when a shape is double-clicked.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a4d11-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a4d11-105">Remarks</span></span>

<span data-ttu-id="a4d11-106">Ereigniszellen werden erst beim Eintreffen des Ereignisses ausgewertet, nicht beim Eingeben der Formel.</span><span class="sxs-lookup"><span data-stu-id="a4d11-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="a4d11-107">Wenn Sie einen Verweis auf die Zelle EventDblClick nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a4d11-107">To get a reference to the EventDblClick cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a4d11-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a4d11-108">Cell name:</span></span>  <br/> | <span data-ttu-id="a4d11-109">EventDblClick</span><span class="sxs-lookup"><span data-stu-id="a4d11-109">EventDblClick</span></span>  <br/> |
   
<span data-ttu-id="a4d11-110">Wenn Sie einen Verweis auf die Zelle EventDblClick aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a4d11-110">To get a reference to the EventDblClick cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a4d11-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a4d11-111">Section index:</span></span>  <br/> |<span data-ttu-id="a4d11-112">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a4d11-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a4d11-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a4d11-113">Row index:</span></span>  <br/> |<span data-ttu-id="a4d11-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="a4d11-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="a4d11-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a4d11-115">Cell index:</span></span>  <br/> |<span data-ttu-id="a4d11-116">**visEvtCellDblClick**</span><span class="sxs-lookup"><span data-stu-id="a4d11-116">**visEvtCellDblClick**</span></span> <br/> |
   

