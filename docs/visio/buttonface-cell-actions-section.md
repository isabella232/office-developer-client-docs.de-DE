---
title: Zelle "ButtonFace" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60025
localization_priority: Normal
ms.assetid: cf15b879-a47e-a5a5-bfdd-1d7ea423742f
description: Bestimmt das Symbol, das neben einem Element in einem Kontext- oder Aktionstagmenü angezeigt wird.
ms.openlocfilehash: 7ee9c4e7e857acb34ce75429aa0aaf679320b0e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407375"
---
# <a name="buttonface-cell-actions-section"></a><span data-ttu-id="5d523-103">Zelle "ButtonFace" (Abschnitt "Actions")</span><span class="sxs-lookup"><span data-stu-id="5d523-103">ButtonFace Cell (Actions Section)</span></span>

<span data-ttu-id="5d523-104">Bestimmt das Symbol, das neben einem Element in einem Kontext- oder Aktionstagmenü angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5d523-104">Identifies the icon that appears next to an item on a shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5d523-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="5d523-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5d523-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d523-106">Remarks</span></span>

<span data-ttu-id="5d523-p101">Die Zeichenfolge in einer ButtonFace-Zelle stellt die ID einer Microsoft Office-Schaltflächenoberseite dar. Der Wert Null (0) oder ein Leerzeichen bedeutet, dass kein Symbol angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5d523-p101">The string contained in the ButtonFace cell represents the ID of a Microsoft Office button face image. A value of zero (0) or blank means no icon appears.</span></span> 
  
<span data-ttu-id="5d523-109">Die IDs, die in der "ButtonFace-Zelle verwendet werden können, sind identisch mit den IDs, die mit der **Face** -ID-Eigenschaft eines **CommandBarButton** -Objekts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5d523-109">The IDs that can be used in the ButtonFace cell are the same as the IDs used with the **FaceID** property of a **CommandBarButton** object.</span></span> <span data-ttu-id="5d523-110">Weitere Informationen zu diesen IDs finden Sie unter "Working with Command Bar Button Images" auf MSDN.</span><span class="sxs-lookup"><span data-stu-id="5d523-110">For more details about these IDs, search for "working with command bar button images" on MSDN.</span></span> 
  
<span data-ttu-id="5d523-111">Wenn Sie einen Verweis auf die Zelle "ButtonFace aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="5d523-111">To get a reference to the ButtonFace cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5d523-112">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="5d523-112">Cell name:</span></span>  <br/> |<span data-ttu-id="5d523-113">**Aktionen**.</span><span class="sxs-lookup"><span data-stu-id="5d523-113">**Actions**.</span></span>  <span data-ttu-id="5d523-114">*Name* .</span><span class="sxs-lookup"><span data-stu-id="5d523-114">*name*  .</span></span> <span data-ttu-id="5d523-115">**"ButtonFace** , wobei **Aktionen**.</span><span class="sxs-lookup"><span data-stu-id="5d523-115">**ButtonFace**         where **Actions**.</span></span>  <span data-ttu-id="5d523-116">*Name* ist der Name der Zeile Actions.</span><span class="sxs-lookup"><span data-stu-id="5d523-116">*name*  is the name of the actions row</span></span>  <br/> |
   
<span data-ttu-id="5d523-117">Wenn Sie einen Verweis auf die Zelle "ButtonFace aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="5d523-117">To get a reference to the ButtonFace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5d523-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="5d523-118">Section index:</span></span>  <br/> |<span data-ttu-id="5d523-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="5d523-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="5d523-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="5d523-120">Row index:</span></span>  <br/> |<span data-ttu-id="5d523-121">**visRowAction** +  *i* , wobei **i** = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="5d523-121">**visRowAction** +  *i*           where **i** = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="5d523-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="5d523-122">Cell index:</span></span>  <br/> |<span data-ttu-id="5d523-123">**visActionButtonFace**</span><span class="sxs-lookup"><span data-stu-id="5d523-123">**visActionButtonFace**</span></span> <br/> |
   

