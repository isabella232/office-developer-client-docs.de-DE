---
title: Zelle "DontMoveChildren" (Abschnitt "Group Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm255
localization_priority: Normal
ms.assetid: ff5bbf05-4851-30ce-7ee1-f0ce7b2781ab
description: Legt fest, ob Shapes in einer Gruppe mithilfe der Maus verschoben werden können.
ms.openlocfilehash: 2b15d75a98b5f5a72bce8b80758d27b197a346ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416594"
---
# <a name="dontmovechildren-cell-group-properties-section"></a><span data-ttu-id="01159-103">Zelle "DontMoveChildren" (Abschnitt "Group Properties")</span><span class="sxs-lookup"><span data-stu-id="01159-103">DontMoveChildren Cell (Group Properties Section)</span></span>

<span data-ttu-id="01159-104">Legt fest, ob Shapes in einer Gruppe mithilfe der Maus verschoben werden können.</span><span class="sxs-lookup"><span data-stu-id="01159-104">Determines whether you can drag shapes in a group using the mouse.</span></span>
  
|<span data-ttu-id="01159-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="01159-105">**Value**</span></span>|<span data-ttu-id="01159-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="01159-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="01159-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="01159-107">TRUE</span></span>  <br/> | <span data-ttu-id="01159-108">Shapes in einer Gruppe können mit der Maus nicht verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="01159-108">Don't allow shapes in a group to be dragged using the mouse.</span></span>  <br/> |
| <span data-ttu-id="01159-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="01159-109">FALSE</span></span>  <br/> | <span data-ttu-id="01159-110">Shapes in einer Gruppe können mit der Maus verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="01159-110">Allow shapes in a group to be dragged using the mouse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01159-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="01159-111">Remarks</span></span>

<span data-ttu-id="01159-112">Wenn diese Zelle den Wert TRUE enthält, können Sie Shapes in Gruppen mithilfe anderer Methoden weiterhin kippen, drehen, größenmäßig anpassen oder neu positionieren.</span><span class="sxs-lookup"><span data-stu-id="01159-112">When the value of this cell is TRUE, you can still flip, rotate, resize, or reposition shapes in groups using other methods.</span></span>
  
<span data-ttu-id="01159-113">Der Wert dieser Zelle ist TRUE bei Gruppen in Master-Shapes und Gruppen in Instanzen von Master-Shapes, die mit früheren Versionen von Microsoft Visio 2000 erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="01159-113">The value of this cell is TRUE for groups in masters and groups in instances of masters that were created in versions of Visio earlier than version 2000.</span></span>
  
<span data-ttu-id="01159-114">Um einen Verweis auf die Zelle DontMoveChildren anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="01159-114">To get a reference to the DontMoveChildren cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="01159-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="01159-115">Cell name:</span></span>  <br/> | <span data-ttu-id="01159-116">DontMoveChildren</span><span class="sxs-lookup"><span data-stu-id="01159-116">DontMoveChildren</span></span>  <br/> |
   
<span data-ttu-id="01159-117">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die DontMoveChildren-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="01159-117">To get a reference to the DontMoveChildren cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="01159-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="01159-118">Section index:</span></span>  <br/> |<span data-ttu-id="01159-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="01159-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="01159-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="01159-120">Row index:</span></span>  <br/> |<span data-ttu-id="01159-121">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="01159-121">**visRowGroup**</span></span> <br/> |
| <span data-ttu-id="01159-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="01159-122">Cell index:</span></span>  <br/> |<span data-ttu-id="01159-123">**visGroupDontMoveChildren**</span><span class="sxs-lookup"><span data-stu-id="01159-123">**visGroupDontMoveChildren**</span></span> <br/> |
   

