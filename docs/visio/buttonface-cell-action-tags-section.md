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
# <a name="buttonface-cell-action-tags-section"></a><span data-ttu-id="4982a-103">Zelle "ButtonFace" (Abschnitt "Action Tags")</span><span class="sxs-lookup"><span data-stu-id="4982a-103">ButtonFace Cell (Action Tags Section)</span></span>

<span data-ttu-id="4982a-104">Enthält die ID der Schaltflächenoberseite, die auf der Schaltfläche Aktionstag angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4982a-104">Contains the ID of the button face image that appears on the action tag button.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4982a-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4982a-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4982a-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4982a-106">Remarks</span></span>

<span data-ttu-id="4982a-107">Die Zeichenfolge in einer ButtonFace-Zelle stellt die ID einer Microsoft Office-Schaltflächenoberseite dar.</span><span class="sxs-lookup"><span data-stu-id="4982a-107">The string contained in the ButtonFace cell represents the ID of a Microsoft Office button face image.</span></span> <span data-ttu-id="4982a-108">Der Wert 0 (Null) oder leer ist standardmäßig auf die Standard-Aktionstag-Infoschaltfläche "i" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4982a-108">A value of 0 (zero) or blank defaults to the standard action tag "i" info button</span></span> ![Standardaktionstag "i"-Infoschaltfläche](media/InfoPS_ZA10180114.gif)<span data-ttu-id="4982a-110">.</span><span class="sxs-lookup"><span data-stu-id="4982a-110">.</span></span>
  
<span data-ttu-id="4982a-111">Die IDs, die in der Zelle ButtonFace verwendet werden können, sind identisch mit den IDs, die mit der **FaceID-Eigenschaft** eines **CommandBarButton-Objekts verwendet** werden.</span><span class="sxs-lookup"><span data-stu-id="4982a-111">The IDs that can be used in the ButtonFace cell are the same as the IDs used with the **FaceID** property of a **CommandBarButton** object.</span></span> <span data-ttu-id="4982a-112">Weitere Informationen zu diesen IDs finden Sie unter "Arbeiten mit Befehlsleistenschaltflächebildern" auf MSDN.</span><span class="sxs-lookup"><span data-stu-id="4982a-112">For more details about these IDs, search for "working with command bar button images" on MSDN.</span></span> 
  
<span data-ttu-id="4982a-113">Verwenden Sie zum Erhalten eines Verweises auf die Zelle ButtonFace anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="4982a-113">To get a reference to the ButtonFace cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4982a-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="4982a-114">Cell name:</span></span>  <br/> | <span data-ttu-id="4982a-115">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="4982a-115">SmartTags.</span></span>  <span data-ttu-id="4982a-116">*Name*  . ButtonFace, wo SmartTags.</span><span class="sxs-lookup"><span data-stu-id="4982a-116">*name*  .ButtonFace           where SmartTags.</span></span> <span data-ttu-id="4982a-117">*Name*  ist der Name der Aktionstagzeile</span><span class="sxs-lookup"><span data-stu-id="4982a-117">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="4982a-118">Um einen Verweis auf die ButtonFace-Zelle nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="4982a-118">To get a reference to the ButtonFace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4982a-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="4982a-119">Section index:</span></span>  <br/> |<span data-ttu-id="4982a-120">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="4982a-120">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="4982a-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="4982a-121">Row index:</span></span>  <br/> |<span data-ttu-id="4982a-122">**visRowSmartTag**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4982a-122">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="4982a-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="4982a-123">Cell index:</span></span>  <br/> |<span data-ttu-id="4982a-124">**visSmartTagButtonFace**</span><span class="sxs-lookup"><span data-stu-id="4982a-124">**visSmartTagButtonFace**</span></span> <br/> |
   

