---
title: Zelle "TagName" (Abschnitt "Action Tags")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60088
localization_priority: Normal
ms.assetid: 28d1cd60-4fb6-9feb-1a13-0962798ac1ad
description: Der Name des Aktionstags, das als Schlüssel verwendet wird, um das Aktionstag seinen Aktionen zuzuordnen.
ms.openlocfilehash: 777d6c1098888c9835c1ad367bb70926b835180b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332396"
---
# <a name="tagname-cell-action-tags-section"></a><span data-ttu-id="3ad54-103">Zelle "TagName" (Abschnitt "Action Tags")</span><span class="sxs-lookup"><span data-stu-id="3ad54-103">TagName Cell (Action Tags Section)</span></span>

<span data-ttu-id="3ad54-104">Der Name des Aktionstags, das als Schlüssel verwendet wird, um das Aktionstag seinen Aktionen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="3ad54-104">Name of the action tag that is used as a key to associate the action tag with its actions.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3ad54-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3ad54-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3ad54-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ad54-106">Remarks</span></span>

 <span data-ttu-id="3ad54-107">Die Zelle TagName im Abschnitt Aktions Tags arbeitet zusammen mit der Zelle TagName im Abschnitt Aktionen, um den Aktionen ein Aktionstag zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="3ad54-107">The TagName cell in the Action Tags section works together with the TagName cell in the Actions section to associate an action tag with its actions.</span></span> <span data-ttu-id="3ad54-108">Zeilen im Abschnitt Actions haben auch eine Zelle TagName, und diese Zeilen mit dem gleichen TagName-Zellenwert als diese Zelle definieren Aktionen, die für dieses Aktionstag ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3ad54-108">Rows in the Actions section also have a TagName cell, and those rows with the same TagName cell value as this cell define actions to take for this action tag.</span></span> 
  
<span data-ttu-id="3ad54-109">Wenn Sie einen Verweis auf die Zelle TagName aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="3ad54-109">To get a reference to the TagName cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3ad54-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="3ad54-110">Cell name:</span></span>  <br/> | <span data-ttu-id="3ad54-111">Smarttags.</span><span class="sxs-lookup"><span data-stu-id="3ad54-111">SmartTags.</span></span>  <span data-ttu-id="3ad54-112">*Name* . TagName, wobei SmartTags.</span><span class="sxs-lookup"><span data-stu-id="3ad54-112">*name*  .TagName           where SmartTags.</span></span> <span data-ttu-id="3ad54-113">*Name* ist der Name der Zeile mit dem Aktionstag.</span><span class="sxs-lookup"><span data-stu-id="3ad54-113">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="3ad54-114">Wenn Sie einen Verweis auf die Zelle TagName aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="3ad54-114">To get a reference to the TagName cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3ad54-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="3ad54-115">Section index:</span></span>  <br/> |<span data-ttu-id="3ad54-116">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="3ad54-116">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="3ad54-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="3ad54-117">Row index:</span></span>  <br/> |<span data-ttu-id="3ad54-118">**visRowSmartTag** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3ad54-118">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3ad54-119">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="3ad54-119">Cell index:</span></span>  <br/> |<span data-ttu-id="3ad54-120">**visSmartTagName**</span><span class="sxs-lookup"><span data-stu-id="3ad54-120">**visSmartTagName**</span></span> <br/> |
   

