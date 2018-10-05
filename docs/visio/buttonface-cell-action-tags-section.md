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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385480"
---
# <a name="buttonface-cell-action-tags-section"></a><span data-ttu-id="49e99-103">ButtonFace Cell (Action Tags Section)</span><span class="sxs-lookup"><span data-stu-id="49e99-103">ButtonFace Cell (Action Tags Section)</span></span>

<span data-ttu-id="49e99-104">Enthält die ID der Schaltflächenoberseite, die auf der Schaltfläche Aktionstag angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="49e99-104">Contains the ID of the button face image that appears on the action tag button.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="49e99-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="49e99-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="49e99-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="49e99-106">Remarks</span></span>

<span data-ttu-id="49e99-p101">Die Zeichenfolge in einer ButtonFace-Zelle stellt die ID einer Microsoft Office-Schaltflächenoberseite dar. Der Wert 0 (Null) oder kein Eintrag ergibt die Standardaktionstag-Infoschaltfläche "i"</span><span class="sxs-lookup"><span data-stu-id="49e99-p101">The string contained in the ButtonFace cell represents the ID of a Microsoft Office button face image. A value of 0 (zero) or blank defaults to the standard action tag "i" info button</span></span> ![Standard Aktionstag "i" Info-Schaltfläche](media/InfoPS_ZA10180114.gif)<span data-ttu-id="49e99-110">.</span><span class="sxs-lookup"><span data-stu-id="49e99-110"></span></span>
  
<span data-ttu-id="49e99-111">Die IDs, die in die Zelle ButtonFace verwendet werden können, sind identisch mit den IDs, die mit der **FaceID** -Eigenschaft eines **CommandBarButton** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="49e99-111">The IDs that can be used in the ButtonFace cell are the same as the IDs used with the **FaceID** property of a **CommandBarButton** object.</span></span> <span data-ttu-id="49e99-112">Weitere Informationen zu diesen IDs auf MSDN nach "Working with Schaltflächensymbolen an Leiste Befehl" suchen.</span><span class="sxs-lookup"><span data-stu-id="49e99-112">For more details about these IDs, search for "working with command bar button images" on MSDN.</span></span> 
  
<span data-ttu-id="49e99-113">Wenn Sie einen Verweis auf die Zelle ButtonFace aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="49e99-113">To get a reference to the ButtonFace cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="49e99-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="49e99-114">Cell name:</span></span>  <br/> | <span data-ttu-id="49e99-115">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="49e99-115">SmartTags.</span></span>  <span data-ttu-id="49e99-116">*Name* . ButtonFace wobei SmartTags.</span><span class="sxs-lookup"><span data-stu-id="49e99-116">*name*  .ButtonFace           where SmartTags.</span></span> <span data-ttu-id="49e99-117">*Name* ist der Name der Zeile Aktionstag</span><span class="sxs-lookup"><span data-stu-id="49e99-117">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="49e99-118">Wenn Sie einen Verweis auf die Zelle ButtonFace aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="49e99-118">To get a reference to the ButtonFace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="49e99-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="49e99-119">Section index:</span></span>  <br/> |<span data-ttu-id="49e99-120">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="49e99-120">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="49e99-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="49e99-121">Row index:</span></span>  <br/> |<span data-ttu-id="49e99-122">**VisRowSmartTag** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="49e99-122">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="49e99-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="49e99-123">Cell index:</span></span>  <br/> |<span data-ttu-id="49e99-124">**visSmartTagButtonFace**</span><span class="sxs-lookup"><span data-stu-id="49e99-124">**visSmartTagButtonFace**</span></span> <br/> |
   

