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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351009"
---
# <a name="eventdrop-cell-events-section"></a><span data-ttu-id="2b979-103">Zelle "EventDrop" (Abschnitt "Events")</span><span class="sxs-lookup"><span data-stu-id="2b979-103">EventDrop Cell (Events Section)</span></span>

<span data-ttu-id="2b979-104">Eine Ereigniszelle, die ausgewertet wird, wenn ein Shape als Instanz auf dem Zeichenblatt abgelegt oder dupliziert oder eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="2b979-104">An event cell that is evaluated when a shape is dropped on the drawing page, either as an instance or when the shape is duplicated or pasted.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2b979-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b979-105">Remarks</span></span>

<span data-ttu-id="2b979-106">Ereigniszellen werden erst beim Eintreffen des Ereignisses ausgewertet, nicht beim Eingeben der Formel.</span><span class="sxs-lookup"><span data-stu-id="2b979-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="2b979-107">Wenn Sie einen Verweis auf die Zelle "EventDrop aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2b979-107">To get a reference to the EventDrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2b979-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2b979-108">Cell name:</span></span>  <br/> | <span data-ttu-id="2b979-109">"EventDrop</span><span class="sxs-lookup"><span data-stu-id="2b979-109">EventDrop</span></span>  <br/> |
   
<span data-ttu-id="2b979-110">Wenn Sie einen Verweis auf die Zelle "EventDrop aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="2b979-110">To get a reference to the EventDrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2b979-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2b979-111">Section index:</span></span>  <br/> |<span data-ttu-id="2b979-112">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2b979-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2b979-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2b979-113">Row index:</span></span>  <br/> |<span data-ttu-id="2b979-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="2b979-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="2b979-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2b979-115">Cell index:</span></span>  <br/> |<span data-ttu-id="2b979-116">**visEvtCellDrop**</span><span class="sxs-lookup"><span data-stu-id="2b979-116">**visEvtCellDrop**</span></span> <br/> |
   

