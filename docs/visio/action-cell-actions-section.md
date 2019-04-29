---
title: Zelle "Action" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm5
localization_priority: Normal
ms.assetid: 435e49ee-0b51-8ce3-0589-3f0717026f4a
description: Enthält die Formel, die ausgeführt werden soll, wenn ein Benutzer einen Befehl in einem Kontext- oder Aktionstagmenü auswählt.
ms.openlocfilehash: e6bc576982cad871804cbcbc5f3d9c6bceb558c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407613"
---
# <a name="action-cell-actions-section"></a><span data-ttu-id="a1893-103">Zelle "Action" (Abschnitt "Actions")</span><span class="sxs-lookup"><span data-stu-id="a1893-103">Action Cell (Actions Section)</span></span>

<span data-ttu-id="a1893-104">Enthält die Formel, die ausgeführt werden soll, wenn ein Benutzer einen Befehl in einem Kontext- oder Aktionstagmenü auswählt.</span><span class="sxs-lookup"><span data-stu-id="a1893-104">Contains the formula to be executed when a user chooses a command on a shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a1893-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a1893-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a1893-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1893-106">Remarks</span></span>

<span data-ttu-id="a1893-107">Die Zelle Action wird nur ausgewertet, wenn die Aktion stattfindet und nicht bei Eingabe der Formel.</span><span class="sxs-lookup"><span data-stu-id="a1893-107">An Action cell is evaluated only when the action occurs, not when the formula is entered.</span></span>
  
<span data-ttu-id="a1893-108">Wenn Sie einen Verweis auf die Zelle Action aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a1893-108">To get a reference to the the Action cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a1893-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a1893-109">Cell name:</span></span>  <br/> | <span data-ttu-id="a1893-110">Aktionen.</span><span class="sxs-lookup"><span data-stu-id="a1893-110">Actions.</span></span>  <span data-ttu-id="a1893-111">*Name* . Aktion, bei der Aktionen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a1893-111">*name*  .Action           where Actions.</span></span> <span data-ttu-id="a1893-112">*Name* ist der Name der Zeile Actions.</span><span class="sxs-lookup"><span data-stu-id="a1893-112">*name*  is the name of the actions row</span></span>  <br/> |
   
<span data-ttu-id="a1893-113">Wenn Sie einen Verweis auf die Zelle thethe-Aktion aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a1893-113">To get a reference to thethe Action cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a1893-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a1893-114">Section index:</span></span>  <br/> |<span data-ttu-id="a1893-115">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="a1893-115">**visSectionAction**</span></span> <br/> |
| <span data-ttu-id="a1893-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a1893-116">Row index:</span></span>  <br/> |<span data-ttu-id="a1893-117">**visRowAction** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a1893-117">**visRowAction** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a1893-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a1893-118">Cell index:</span></span>  <br/> |<span data-ttu-id="a1893-119">**visActionAction**</span><span class="sxs-lookup"><span data-stu-id="a1893-119">**visActionAction**</span></span> <br/> |
   

