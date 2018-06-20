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
ms.openlocfilehash: ca6be0a95b33e173219f4bdc1ba042c7162941b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796561"
---
# <a name="buttonface-cell-action-tags-section"></a><span data-ttu-id="67a5d-103">ButtonFace Cell (Action Tags Section)</span><span class="sxs-lookup"><span data-stu-id="67a5d-103">ButtonFace Cell (Action Tags Section)</span></span>

<span data-ttu-id="67a5d-104">Enthält die ID der Schaltflächenoberseite, die auf der Schaltfläche Aktionstag angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="67a5d-104">Contains the ID of the button face image that appears on the action tag button.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="67a5d-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="67a5d-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="67a5d-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="67a5d-106">Remarks</span></span>

<span data-ttu-id="67a5d-107">Die Zeichenfolge in die Zelle ButtonFace stellt die ID einer Microsoft Office-Schaltflächenoberseite dar.</span><span class="sxs-lookup"><span data-stu-id="67a5d-107">The string contained in the ButtonFace cell represents the ID of a Microsoft Office button face image.</span></span> <span data-ttu-id="67a5d-108">Der Wert 0 (null) oder kein Eintrag ergibt die standard "i" Infoschaltfläche Aktionstag ![](media/InfoPS_ZA10180114.gif).</span><span class="sxs-lookup"><span data-stu-id="67a5d-108">A value of 0 (zero) or blank defaults to the standard action tag "i" info button ![](media/InfoPS_ZA10180114.gif).</span></span>
  
<span data-ttu-id="67a5d-109">Die IDs, die in die Zelle ButtonFace verwendet werden können, sind identisch mit den IDs, die mit der **FaceID** -Eigenschaft eines **CommandBarButton** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="67a5d-109">The IDs that can be used in the ButtonFace cell are the same as the IDs used with the **FaceID** property of a **CommandBarButton** object.</span></span> <span data-ttu-id="67a5d-110">Weitere Informationen zu diesen IDs auf MSDN nach "Working with Schaltflächensymbolen an Leiste Befehl" suchen.</span><span class="sxs-lookup"><span data-stu-id="67a5d-110">For more details about these IDs, search for "working with command bar button images" on MSDN.</span></span> 
  
<span data-ttu-id="67a5d-111">Wenn Sie einen Verweis auf die Zelle ButtonFace nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="67a5d-111">To get a reference to the ButtonFace cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="67a5d-112">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="67a5d-112">Cell name:</span></span>  <br/> | <span data-ttu-id="67a5d-113">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="67a5d-113">SmartTags.</span></span>  <span data-ttu-id="67a5d-114">*Name* . ButtonFace wobei SmartTags.</span><span class="sxs-lookup"><span data-stu-id="67a5d-114">*name*  .ButtonFace           where SmartTags.</span></span> <span data-ttu-id="67a5d-115">*Name* ist der Name der Zeile Aktionstag</span><span class="sxs-lookup"><span data-stu-id="67a5d-115">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="67a5d-116">Wenn Sie einen Verweis auf die Zelle ButtonFace aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="67a5d-116">To get a reference to the ButtonFace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="67a5d-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="67a5d-117">Section index:</span></span>  <br/> |<span data-ttu-id="67a5d-118">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="67a5d-118">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="67a5d-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="67a5d-119">Row index:</span></span>  <br/> |<span data-ttu-id="67a5d-120">**VisRowSmartTag** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="67a5d-120">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="67a5d-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="67a5d-121">Cell index:</span></span>  <br/> |<span data-ttu-id="67a5d-122">**visSmartTagButtonFace**</span><span class="sxs-lookup"><span data-stu-id="67a5d-122">**visSmartTagButtonFace**</span></span> <br/> |
   

