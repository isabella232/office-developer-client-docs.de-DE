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
ms.openlocfilehash: 3c365d24170f912624a2abdeeadd75140bea9a85
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796846"
---
# <a name="description-cell-action-tags-section"></a><span data-ttu-id="24757-103">Description Cell (Action Tags Section)</span><span class="sxs-lookup"><span data-stu-id="24757-103">Description Cell (Action Tags Section)</span></span>

<span data-ttu-id="24757-104">Enthält eine Zeichenfolge als Beschreibung des Aktionstags, die als QuickInfo angezeigt wird, wenn der Zeiger über dem Tag platziert wird.</span><span class="sxs-lookup"><span data-stu-id="24757-104">Contains a string that describes the action tag, which appears as a tool tip when users place their pointer over the tag.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="24757-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="24757-105">Remarks</span></span>

<span data-ttu-id="24757-106">Wenn Sie einen Verweis auf die Zelle Description aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="24757-106">To get a reference to the Description cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="24757-107">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="24757-107">Cell name:</span></span>  <br/> | <span data-ttu-id="24757-108">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="24757-108">SmartTags.</span></span>  <span data-ttu-id="24757-109">*Name* . Beschreibung, in dem SmartTags.</span><span class="sxs-lookup"><span data-stu-id="24757-109">*name*  .Description           where SmartTags.</span></span> <span data-ttu-id="24757-110">*Name* ist der Name der Zeile Aktionstag</span><span class="sxs-lookup"><span data-stu-id="24757-110">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="24757-111">Wenn Sie einen Verweis auf die Zelle Description aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="24757-111">To get a reference to the Description cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="24757-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="24757-112">Section index:</span></span>  <br/> |<span data-ttu-id="24757-113">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="24757-113">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="24757-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="24757-114">Row index:</span></span>  <br/> |<span data-ttu-id="24757-115">**VisRowSmartTag** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="24757-115">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="24757-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="24757-116">Cell index:</span></span>  <br/> |<span data-ttu-id="24757-117">**visSmartTagDescription**</span><span class="sxs-lookup"><span data-stu-id="24757-117">**visSmartTagDescription**</span></span> <br/> |
   

