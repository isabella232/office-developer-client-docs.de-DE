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
ms.openlocfilehash: dbac3d4dff9d2ffd18bba75db56cafc08f5e0ee8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798226"
---
# <a name="tagname-cell-action-tags-section"></a><span data-ttu-id="a6528-103">TagName Cell (Action Tags Section)</span><span class="sxs-lookup"><span data-stu-id="a6528-103">TagName Cell (Action Tags Section)</span></span>

<span data-ttu-id="a6528-104">Der Name des Aktionstags, das als Schlüssel verwendet wird, um das Aktionstag seinen Aktionen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="a6528-104">Name of the action tag that is used as a key to associate the action tag with its actions.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a6528-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a6528-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a6528-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6528-106">Remarks</span></span>

 <span data-ttu-id="a6528-107">Die Zelle TagName im Abschnitt Action Tags kann zusammen mit der Zelle TagName im Abschnitt Aktionen auf ein Aktionstag seinen Aktionen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="a6528-107">The TagName cell in the Action Tags section works together with the TagName cell in the Actions section to associate an action tag with its actions.</span></span> <span data-ttu-id="a6528-108">Zeilen im Abschnitt Aktionen auch eine Zelle TagName, und die Zeilen mit denselben Zelle TagName-Wert wie diese Zelle Aktionen an, die für diese Aktionstag definieren.</span><span class="sxs-lookup"><span data-stu-id="a6528-108">Rows in the Actions section also have a TagName cell, and those rows with the same TagName cell value as this cell define actions to take for this action tag.</span></span> 
  
<span data-ttu-id="a6528-109">Wenn Sie einen Verweis auf die Zelle TagName aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a6528-109">To get a reference to the TagName cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a6528-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a6528-110">Cell name:</span></span>  <br/> | <span data-ttu-id="a6528-111">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="a6528-111">SmartTags.</span></span>  <span data-ttu-id="a6528-112">*Name* . TagName wobei SmartTags.</span><span class="sxs-lookup"><span data-stu-id="a6528-112">*name*  .TagName           where SmartTags.</span></span> <span data-ttu-id="a6528-113">*Name* ist der Name der Zeile Aktionstag</span><span class="sxs-lookup"><span data-stu-id="a6528-113">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="a6528-114">Wenn Sie einen Verweis auf die Zelle TagName aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a6528-114">To get a reference to the TagName cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a6528-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a6528-115">Section index:</span></span>  <br/> |<span data-ttu-id="a6528-116">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="a6528-116">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="a6528-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a6528-117">Row index:</span></span>  <br/> |<span data-ttu-id="a6528-118">**VisRowSmartTag** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a6528-118">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a6528-119">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a6528-119">Cell index:</span></span>  <br/> |<span data-ttu-id="a6528-120">**visSmartTagName**</span><span class="sxs-lookup"><span data-stu-id="a6528-120">**visSmartTagName**</span></span> <br/> |
   

