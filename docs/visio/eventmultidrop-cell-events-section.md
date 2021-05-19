---
title: Zelle "EventMultiDrop" (Abschnitt "Events")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: caa86e33d0d7aa9ca31cbbf8939e17b581877669
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416720"
---
# <a name="eventmultidrop-cell-events-section"></a><span data-ttu-id="90592-102">Zelle "EventMultiDrop" (Abschnitt "Events")</span><span class="sxs-lookup"><span data-stu-id="90592-102">EventMultiDrop Cell (Events Section)</span></span>

<span data-ttu-id="90592-103">Eine Ereigniszelle, die ausgewertet wird, wenn mehrere Shapes auf dem Zeichenblatt abgelegt werden, entweder als Instanzen oder wenn Shapes dupliziert oder eingelassen werden.</span><span class="sxs-lookup"><span data-stu-id="90592-103">An event cell that is evaluated when multiple shapes are dropped on the drawing page, either as instances or when shapes are duplicated or pasted.</span></span>
  
<span data-ttu-id="90592-104">Ereigniszellen werden erst beim Eintreffen des Ereignisses ausgewertet, nicht beim Eingeben der Formel.</span><span class="sxs-lookup"><span data-stu-id="90592-104">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="90592-105">Verwenden Sie zum Verweisen auf die EventMultiDrop-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="90592-105">To refer to the EventMultiDrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="90592-106">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="90592-106">Cell name:</span></span>  <br/> |<span data-ttu-id="90592-107">EventMultiDrop</span><span class="sxs-lookup"><span data-stu-id="90592-107">EventMultiDrop</span></span>  <br/> |
   
<span data-ttu-id="90592-108">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um auf die EventMultiDrop-Zelle nach Index aus einem Programm zu verweisen:</span><span class="sxs-lookup"><span data-stu-id="90592-108">To refer to the EventMultiDrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="90592-109">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="90592-109">Section index:</span></span>  <br/> |<span data-ttu-id="90592-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="90592-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="90592-111">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="90592-111">Row index:</span></span>  <br/> |<span data-ttu-id="90592-112">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="90592-112">**visRowEvent**</span></span> <br/> |
|<span data-ttu-id="90592-113">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="90592-113">Cell index:</span></span>  <br/> |<span data-ttu-id="90592-114">**visEvtCellMultiDrop**</span><span class="sxs-lookup"><span data-stu-id="90592-114">**visEvtCellMultiDrop**</span></span> <br/> |
   

