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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338584"
---
# <a name="dontmovechildren-cell-group-properties-section"></a><span data-ttu-id="54093-103">Zelle "DontMoveChildren" (Abschnitt "Group Properties")</span><span class="sxs-lookup"><span data-stu-id="54093-103">DontMoveChildren Cell (Group Properties Section)</span></span>

<span data-ttu-id="54093-104">Legt fest, ob Shapes in einer Gruppe mithilfe der Maus verschoben werden können.</span><span class="sxs-lookup"><span data-stu-id="54093-104">Determines whether you can drag shapes in a group using the mouse.</span></span>
  
|<span data-ttu-id="54093-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="54093-105">**Value**</span></span>|<span data-ttu-id="54093-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="54093-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="54093-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="54093-107">TRUE</span></span>  <br/> | <span data-ttu-id="54093-108">Shapes in einer Gruppe können mit der Maus nicht verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="54093-108">Don't allow shapes in a group to be dragged using the mouse.</span></span>  <br/> |
| <span data-ttu-id="54093-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="54093-109">FALSE</span></span>  <br/> | <span data-ttu-id="54093-110">Shapes in einer Gruppe können mit der Maus verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="54093-110">Allow shapes in a group to be dragged using the mouse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54093-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54093-111">Remarks</span></span>

<span data-ttu-id="54093-112">Wenn diese Zelle den Wert TRUE enthält, können Sie Shapes in Gruppen mithilfe anderer Methoden weiterhin kippen, drehen, größenmäßig anpassen oder neu positionieren.</span><span class="sxs-lookup"><span data-stu-id="54093-112">When the value of this cell is TRUE, you can still flip, rotate, resize, or reposition shapes in groups using other methods.</span></span>
  
<span data-ttu-id="54093-113">Der Wert dieser Zelle ist TRUE bei Gruppen in Master-Shapes und Gruppen in Instanzen von Master-Shapes, die mit früheren Versionen von Microsoft Visio 2000 erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="54093-113">The value of this cell is TRUE for groups in masters and groups in instances of masters that were created in versions of Visio earlier than version 2000.</span></span>
  
<span data-ttu-id="54093-114">Wenn Sie einen Verweis auf die Zelle "DontMoveChildren aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="54093-114">To get a reference to the DontMoveChildren cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="54093-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="54093-115">Cell name:</span></span>  <br/> | <span data-ttu-id="54093-116">"DontMoveChildren</span><span class="sxs-lookup"><span data-stu-id="54093-116">DontMoveChildren</span></span>  <br/> |
   
<span data-ttu-id="54093-117">Wenn Sie einen Verweis auf die Zelle "DontMoveChildren aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="54093-117">To get a reference to the DontMoveChildren cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="54093-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="54093-118">Section index:</span></span>  <br/> |<span data-ttu-id="54093-119">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="54093-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="54093-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="54093-120">Row index:</span></span>  <br/> |<span data-ttu-id="54093-121">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="54093-121">**visRowGroup**</span></span> <br/> |
| <span data-ttu-id="54093-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="54093-122">Cell index:</span></span>  <br/> |<span data-ttu-id="54093-123">**visGroupDontMoveChildren**</span><span class="sxs-lookup"><span data-stu-id="54093-123">**visGroupDontMoveChildren**</span></span> <br/> |
   

