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
# <a name="eventmultidrop-cell-events-section"></a><span data-ttu-id="bc857-102">Zelle "EventMultiDrop" (Abschnitt "Events")</span><span class="sxs-lookup"><span data-stu-id="bc857-102">EventMultiDrop Cell (Events Section)</span></span>

<span data-ttu-id="bc857-103">Eine Ereignis Zelle, die ausgewertet wird, wenn mehrere Shapes auf dem Zeichenblatt abgelegt werden, entweder als Instanzen oder beim Duplizieren oder Einfügen von Shapes.</span><span class="sxs-lookup"><span data-stu-id="bc857-103">An event cell that is evaluated when multiple shapes are dropped on the drawing page, either as instances or when shapes are duplicated or pasted.</span></span>
  
<span data-ttu-id="bc857-104">Ereigniszellen werden erst beim Eintreffen des Ereignisses ausgewertet, nicht beim Eingeben der Formel.</span><span class="sxs-lookup"><span data-stu-id="bc857-104">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="bc857-105">Wenn Sie auf die Zelle EventMultiDrop aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen verweisen möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="bc857-105">To refer to the EventMultiDrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bc857-106">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="bc857-106">Cell name:</span></span>  <br/> |<span data-ttu-id="bc857-107">EventMultiDrop</span><span class="sxs-lookup"><span data-stu-id="bc857-107">EventMultiDrop</span></span>  <br/> |
   
<span data-ttu-id="bc857-108">Wenn Sie aus einem Programm aus nach Index auf die Zelle EventMultiDrop verweisen möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="bc857-108">To refer to the EventMultiDrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bc857-109">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="bc857-109">Section index:</span></span>  <br/> |<span data-ttu-id="bc857-110">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bc857-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="bc857-111">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="bc857-111">Row index:</span></span>  <br/> |<span data-ttu-id="bc857-112">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="bc857-112">**visRowEvent**</span></span> <br/> |
|<span data-ttu-id="bc857-113">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="bc857-113">Cell index:</span></span>  <br/> |<span data-ttu-id="bc857-114">**visEvtCellMultiDrop**</span><span class="sxs-lookup"><span data-stu-id="bc857-114">**visEvtCellMultiDrop**</span></span> <br/> |
   

