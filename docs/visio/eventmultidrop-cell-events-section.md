---
title: Zelle "EventMultiDrop" (Abschnitt "Events")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: e44cd18c3f7673761f457db9cd4bfe00a8ab89bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796961"
---
# <a name="eventmultidrop-cell-events-section"></a><span data-ttu-id="b10cb-102">Zelle "EventMultiDrop" (Abschnitt "Events")</span><span class="sxs-lookup"><span data-stu-id="b10cb-102">EventMultiDrop Cell (Events Section)</span></span>

<span data-ttu-id="b10cb-103">Eine Ereigniszelle, die ausgewertet wird, wenn mehrere Shapes auf dem Zeichenblatt abgelegt werden, entweder als Instanzen oder dupliziert oder eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b10cb-103">An event cell that is evaluated when multiple shapes are dropped on the drawing page, either as instances or when shapes are duplicated or pasted.</span></span>
  
<span data-ttu-id="b10cb-104">Ereigniszellen werden erst beim Eintreffen des Ereignisses ausgewertet, nicht beim Eingeben der Formel.</span><span class="sxs-lookup"><span data-stu-id="b10cb-104">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="b10cb-105">Wenn Sie auf die Zelle EventMultiDrop nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft verweisen möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b10cb-105">To refer to the EventMultiDrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b10cb-106">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b10cb-106">Cell name:</span></span>  <br/> |<span data-ttu-id="b10cb-107">EventMultiDrop</span><span class="sxs-lookup"><span data-stu-id="b10cb-107">EventMultiDrop</span></span>  <br/> |
   
<span data-ttu-id="b10cb-108">Wenn Sie auf die Zelle EventMultiDrop durch Index aus einem Programm verweisen möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="b10cb-108">To refer to the EventMultiDrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b10cb-109">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b10cb-109">Section index:</span></span>  <br/> |<span data-ttu-id="b10cb-110">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b10cb-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b10cb-111">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b10cb-111">Row index:</span></span>  <br/> |<span data-ttu-id="b10cb-112">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="b10cb-112">**visRowEvent**</span></span> <br/> |
|<span data-ttu-id="b10cb-113">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b10cb-113">Cell index:</span></span>  <br/> |<span data-ttu-id="b10cb-114">**visEvtCellMultiDrop**</span><span class="sxs-lookup"><span data-stu-id="b10cb-114">**visEvtCellMultiDrop**</span></span> <br/> |
   

