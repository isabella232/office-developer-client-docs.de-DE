---
title: Zelle "Description" (Abschnitt "Action Tags")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60037
localization_priority: Normal
ms.assetid: feb29b91-0f6e-6353-3dd0-7a280843a517
description: Enthält eine Zeichenfolge als Beschreibung des Aktionstags, die als QuickInfo angezeigt wird, wenn der Zeiger über dem Tag platziert wird.
ms.openlocfilehash: 00c7a4c1547927b8d1a979b8ae074f96f26dc17c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360230"
---
# <a name="description-cell-action-tags-section"></a><span data-ttu-id="72189-103">Zelle "Description" (Abschnitt "Action Tags")</span><span class="sxs-lookup"><span data-stu-id="72189-103">Description Cell (Action Tags Section)</span></span>

<span data-ttu-id="72189-104">Enthält eine Zeichenfolge als Beschreibung des Aktionstags, die als QuickInfo angezeigt wird, wenn der Zeiger über dem Tag platziert wird.</span><span class="sxs-lookup"><span data-stu-id="72189-104">Contains a string that describes the action tag, which appears as a tool tip when users place their pointer over the tag.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="72189-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72189-105">Remarks</span></span>

<span data-ttu-id="72189-106">Wenn Sie einen Verweis auf die Zelle Description aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="72189-106">To get a reference to the Description cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="72189-107">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="72189-107">Cell name:</span></span>  <br/> | <span data-ttu-id="72189-108">Smarttags.</span><span class="sxs-lookup"><span data-stu-id="72189-108">SmartTags.</span></span>  <span data-ttu-id="72189-109">*Name* . Beschreibung, in der SmartTags.</span><span class="sxs-lookup"><span data-stu-id="72189-109">*name*  .Description           where SmartTags.</span></span> <span data-ttu-id="72189-110">*Name* ist der Name der Zeile mit dem Aktionstag.</span><span class="sxs-lookup"><span data-stu-id="72189-110">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="72189-111">Wenn Sie einen Verweis auf die Zelle Description aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="72189-111">To get a reference to the Description cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="72189-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="72189-112">Section index:</span></span>  <br/> |<span data-ttu-id="72189-113">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="72189-113">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="72189-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="72189-114">Row index:</span></span>  <br/> |<span data-ttu-id="72189-115">**visRowSmartTag** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="72189-115">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="72189-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="72189-116">Cell index:</span></span>  <br/> |<span data-ttu-id="72189-117">**visSmartTagDescription**</span><span class="sxs-lookup"><span data-stu-id="72189-117">**visSmartTagDescription**</span></span> <br/> |
   

