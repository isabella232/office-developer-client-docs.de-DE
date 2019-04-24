---
title: Zelle "ButtonFace" (Abschnitt "Action Tags")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60026
localization_priority: Normal
ms.assetid: 26f370e1-5193-f47d-7b60-3597975be650
description: Enthält die ID der Schaltflächenoberseite, die auf der Schaltfläche Aktionstag angezeigt wird.
ms.openlocfilehash: e74b3281d894cebd8491112181198d427f0d337f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337538"
---
# <a name="buttonface-cell-action-tags-section"></a><span data-ttu-id="968f2-103">Zelle "ButtonFace" (Abschnitt "Action Tags")</span><span class="sxs-lookup"><span data-stu-id="968f2-103">ButtonFace Cell (Action Tags Section)</span></span>

<span data-ttu-id="968f2-104">Enthält die ID der Schaltflächenoberseite, die auf der Schaltfläche Aktionstag angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="968f2-104">Contains the ID of the button face image that appears on the action tag button.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="968f2-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="968f2-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="968f2-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="968f2-106">Remarks</span></span>

<span data-ttu-id="968f2-107">Die Zeichenfolge in einer ButtonFace-Zelle stellt die ID einer Microsoft Office-Schaltflächenoberseite dar.</span><span class="sxs-lookup"><span data-stu-id="968f2-107">The string contained in the ButtonFace cell represents the ID of a Microsoft Office button face image.</span></span> <span data-ttu-id="968f2-108">Der Wert 0 (null) oder leer ist standardmäßig auf die Schaltfläche "i" Info.</span><span class="sxs-lookup"><span data-stu-id="968f2-108">A value of 0 (zero) or blank defaults to the standard action tag "i" info button</span></span> ![Standard Aktionstag "i" Info-Schaltfläche](media/InfoPS_ZA10180114.gif)<span data-ttu-id="968f2-110">.</span><span class="sxs-lookup"><span data-stu-id="968f2-110"></span></span>
  
<span data-ttu-id="968f2-111">Die IDs, die in der "ButtonFace-Zelle verwendet werden können, sind identisch mit den IDs, die mit der **Face** -ID-Eigenschaft eines **CommandBarButton** -Objekts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="968f2-111">The IDs that can be used in the ButtonFace cell are the same as the IDs used with the **FaceID** property of a **CommandBarButton** object.</span></span> <span data-ttu-id="968f2-112">Weitere Informationen zu diesen IDs finden Sie unter "Working with Command Bar Button Images" auf MSDN.</span><span class="sxs-lookup"><span data-stu-id="968f2-112">For more details about these IDs, search for "working with command bar button images" on MSDN.</span></span> 
  
<span data-ttu-id="968f2-113">Wenn Sie einen Verweis auf die Zelle "ButtonFace aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="968f2-113">To get a reference to the ButtonFace cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="968f2-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="968f2-114">Cell name:</span></span>  <br/> | <span data-ttu-id="968f2-115">Smarttags.</span><span class="sxs-lookup"><span data-stu-id="968f2-115">SmartTags.</span></span>  <span data-ttu-id="968f2-116">*Name* . "ButtonFace, wobei SmartTags.</span><span class="sxs-lookup"><span data-stu-id="968f2-116">*name*  .ButtonFace           where SmartTags.</span></span> <span data-ttu-id="968f2-117">*Name* ist der Name der Zeile mit dem Aktionstag.</span><span class="sxs-lookup"><span data-stu-id="968f2-117">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="968f2-118">Wenn Sie einen Verweis auf die Zelle "ButtonFace aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="968f2-118">To get a reference to the ButtonFace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="968f2-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="968f2-119">Section index:</span></span>  <br/> |<span data-ttu-id="968f2-120">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="968f2-120">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="968f2-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="968f2-121">Row index:</span></span>  <br/> |<span data-ttu-id="968f2-122">**visRowSmartTag** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="968f2-122">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="968f2-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="968f2-123">Cell index:</span></span>  <br/> |<span data-ttu-id="968f2-124">**visSmartTagButtonFace**</span><span class="sxs-lookup"><span data-stu-id="968f2-124">**visSmartTagButtonFace**</span></span> <br/> |
   

