---
title: Zelle "EventDrop" (Abschnitt "Events")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm350
localization_priority: Normal
ms.assetid: f84afe83-8391-0c13-f442-ea8794b38642
description: Eine Ereigniszelle, die ausgewertet wird, wenn ein Shape als Instanz auf dem Zeichenblatt abgelegt oder dupliziert oder eingefügt wird.
ms.openlocfilehash: f1433394dbd58c7c4422c6bca1e79a4f2c8e0c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408593"
---
# <a name="eventdrop-cell-events-section"></a><span data-ttu-id="52d59-103">Zelle "EventDrop" (Abschnitt "Events")</span><span class="sxs-lookup"><span data-stu-id="52d59-103">EventDrop Cell (Events Section)</span></span>

<span data-ttu-id="52d59-104">Eine Ereigniszelle, die ausgewertet wird, wenn ein Shape als Instanz auf dem Zeichenblatt abgelegt oder dupliziert oder eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="52d59-104">An event cell that is evaluated when a shape is dropped on the drawing page, either as an instance or when the shape is duplicated or pasted.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="52d59-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="52d59-105">Remarks</span></span>

<span data-ttu-id="52d59-106">Ereigniszellen werden erst beim Eintreffen des Ereignisses ausgewertet, nicht beim Eingeben der Formel.</span><span class="sxs-lookup"><span data-stu-id="52d59-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="52d59-107">Um einen Verweis auf die EventDrop-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="52d59-107">To get a reference to the EventDrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="52d59-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="52d59-108">Cell name:</span></span>  <br/> | <span data-ttu-id="52d59-109">EventDrop</span><span class="sxs-lookup"><span data-stu-id="52d59-109">EventDrop</span></span>  <br/> |
   
<span data-ttu-id="52d59-110">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die EventDrop-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="52d59-110">To get a reference to the EventDrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="52d59-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="52d59-111">Section index:</span></span>  <br/> |<span data-ttu-id="52d59-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="52d59-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="52d59-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="52d59-113">Row index:</span></span>  <br/> |<span data-ttu-id="52d59-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="52d59-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="52d59-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="52d59-115">Cell index:</span></span>  <br/> |<span data-ttu-id="52d59-116">**visEvtCellDrop**</span><span class="sxs-lookup"><span data-stu-id="52d59-116">**visEvtCellDrop**</span></span> <br/> |
   

