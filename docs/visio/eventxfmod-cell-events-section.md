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
description: Eine Ereigniszelle, die ausgewertet wird, wenn ein Shape Position oder Ausrichtung auf der Seite transformiert ("XF").
ms.openlocfilehash: 5884aabc11798ae0440fbfa024b9cc2f2418b9cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796973"
---
# <a name="eventxfmod-cell-events-section"></a><span data-ttu-id="282b8-103">EventXFMod Cell (Events Section)</span><span class="sxs-lookup"><span data-stu-id="282b8-103">EventXFMod Cell (Events Section)</span></span>

<span data-ttu-id="282b8-104">Eine Ereigniszelle, die ausgewertet wird, wenn die Position oder Ausrichtung eines Shapes auf dem Blatt transformiert wird ("XF").</span><span class="sxs-lookup"><span data-stu-id="282b8-104">An event cell that is evaluated when a shape's position or orientation on the page is transformed ("XF").</span></span>
  
## <a name="remarks"></a><span data-ttu-id="282b8-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="282b8-105">Remarks</span></span>

<span data-ttu-id="282b8-106">Ereigniszellen werden erst beim Eintreffen des Ereignisses ausgewertet, nicht beim Eingeben der Formel.</span><span class="sxs-lookup"><span data-stu-id="282b8-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="282b8-107">Wenn Sie einen Verweis auf die Zelle EventXFMod aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="282b8-107">To get a reference to the EventXFMod cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="282b8-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="282b8-108">Cell name:</span></span>  <br/> | <span data-ttu-id="282b8-109">EventXFMod</span><span class="sxs-lookup"><span data-stu-id="282b8-109">EventXFMod</span></span>  <br/> |
   
<span data-ttu-id="282b8-110">Wenn Sie einen Verweis auf die Zelle EventXFMod aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="282b8-110">To get a reference to the EventXFMod cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="282b8-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="282b8-111">Section index:</span></span>  <br/> |<span data-ttu-id="282b8-112">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="282b8-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="282b8-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="282b8-113">Row index:</span></span>  <br/> |<span data-ttu-id="282b8-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="282b8-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="282b8-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="282b8-115">Cell index:</span></span>  <br/> |<span data-ttu-id="282b8-116">**visEvtCellXFMod**</span><span class="sxs-lookup"><span data-stu-id="282b8-116">**visEvtCellXFMod**</span></span> <br/> |
   

