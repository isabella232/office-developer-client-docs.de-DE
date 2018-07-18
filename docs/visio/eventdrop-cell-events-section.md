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
ms.openlocfilehash: e2624c50896de061727003a48f7dc1559c6a72c4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796944"
---
# <a name="eventdrop-cell-events-section"></a><span data-ttu-id="afa10-103">EventDrop Cell (Events Section)</span><span class="sxs-lookup"><span data-stu-id="afa10-103">EventDrop Cell (Events Section)</span></span>

<span data-ttu-id="afa10-104">Eine Ereigniszelle, die ausgewertet wird, wenn ein Shape als Instanz auf dem Zeichenblatt abgelegt oder dupliziert oder eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="afa10-104">An event cell that is evaluated when a shape is dropped on the drawing page, either as an instance or when the shape is duplicated or pasted.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="afa10-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="afa10-105">Remarks</span></span>

<span data-ttu-id="afa10-106">Ereigniszellen werden erst beim Eintreffen des Ereignisses ausgewertet, nicht beim Eingeben der Formel.</span><span class="sxs-lookup"><span data-stu-id="afa10-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="afa10-107">Wenn Sie einen Verweis auf die Zelle EventDrop aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="afa10-107">To get a reference to the EventDrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="afa10-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="afa10-108">Cell name:</span></span>  <br/> | <span data-ttu-id="afa10-109">EventDrop</span><span class="sxs-lookup"><span data-stu-id="afa10-109">EventDrop</span></span>  <br/> |
   
<span data-ttu-id="afa10-110">Wenn Sie einen Verweis auf die Zelle EventDrop aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="afa10-110">To get a reference to the EventDrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="afa10-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="afa10-111">Section index:</span></span>  <br/> |<span data-ttu-id="afa10-112">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="afa10-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="afa10-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="afa10-113">Row index:</span></span>  <br/> |<span data-ttu-id="afa10-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="afa10-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="afa10-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="afa10-115">Cell index:</span></span>  <br/> |<span data-ttu-id="afa10-116">**visEvtCellDrop**</span><span class="sxs-lookup"><span data-stu-id="afa10-116">**visEvtCellDrop**</span></span> <br/> |
   

