---
title: Zelle "Alignment" (Abschnitt "Tabs")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm35
localization_priority: Normal
ms.assetid: 84234177-a2df-6acc-2761-230bc5d12627
description: Legt die Tabausrichtung fest.
ms.openlocfilehash: 461357c9c838fb4c0e5b0159bf027dd6adce26f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341538"
---
# <a name="alignment-cell-tabs-section"></a><span data-ttu-id="c534b-103">Zelle "Alignment" (Abschnitt "Tabs")</span><span class="sxs-lookup"><span data-stu-id="c534b-103">Alignment Cell (Tabs Section)</span></span>

<span data-ttu-id="c534b-104">Legt die Tabausrichtung fest.</span><span class="sxs-lookup"><span data-stu-id="c534b-104">Specifies the tab alignment.</span></span>
  
|<span data-ttu-id="c534b-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="c534b-105">**Value**</span></span>|<span data-ttu-id="c534b-106">**Alignment**</span><span class="sxs-lookup"><span data-stu-id="c534b-106">**Alignment**</span></span>|<span data-ttu-id="c534b-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="c534b-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="c534b-108">0</span><span class="sxs-lookup"><span data-stu-id="c534b-108">0</span></span>  <br/> | <span data-ttu-id="c534b-109">Left</span><span class="sxs-lookup"><span data-stu-id="c534b-109">Left</span></span>  <br/> |<span data-ttu-id="c534b-110">**visTabStopLeft**</span><span class="sxs-lookup"><span data-stu-id="c534b-110">**visTabStopLeft**</span></span> <br/> |
| <span data-ttu-id="c534b-111">1</span><span class="sxs-lookup"><span data-stu-id="c534b-111">1</span></span>  <br/> | <span data-ttu-id="c534b-112">Zentriert</span><span class="sxs-lookup"><span data-stu-id="c534b-112">Center</span></span>  <br/> |<span data-ttu-id="c534b-113">**visTabStopCenter**</span><span class="sxs-lookup"><span data-stu-id="c534b-113">**visTabStopCenter**</span></span> <br/> |
| <span data-ttu-id="c534b-114">2</span><span class="sxs-lookup"><span data-stu-id="c534b-114">2</span></span>  <br/> | <span data-ttu-id="c534b-115">Nach rechts</span><span class="sxs-lookup"><span data-stu-id="c534b-115">Right</span></span>  <br/> |<span data-ttu-id="c534b-116">**visTabStopRight**</span><span class="sxs-lookup"><span data-stu-id="c534b-116">**visTabStopRight**</span></span> <br/> |
| <span data-ttu-id="c534b-117">3</span><span class="sxs-lookup"><span data-stu-id="c534b-117">3</span></span>  <br/> | <span data-ttu-id="c534b-118">Dezimal</span><span class="sxs-lookup"><span data-stu-id="c534b-118">Decimal</span></span>  <br/> |<span data-ttu-id="c534b-119">**visTabStopDecimal**</span><span class="sxs-lookup"><span data-stu-id="c534b-119">**visTabStopDecimal**</span></span> <br/> |
| <span data-ttu-id="c534b-120">4</span><span class="sxs-lookup"><span data-stu-id="c534b-120">4</span></span>  <br/> | <span data-ttu-id="c534b-121">Komma</span><span class="sxs-lookup"><span data-stu-id="c534b-121">Comma</span></span>  <br/> |<span data-ttu-id="c534b-122">**visTabStopComma**</span><span class="sxs-lookup"><span data-stu-id="c534b-122">**visTabStopComma**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c534b-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c534b-123">Remarks</span></span>

<span data-ttu-id="c534b-124">Wenn Sie einen Verweis auf die Zelle Alignment aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c534b-124">To get a reference to the Alignment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c534b-125">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="c534b-125">Cell name:</span></span>  <br/> | <span data-ttu-id="c534b-126">Registerkarten.</span><span class="sxs-lookup"><span data-stu-id="c534b-126">Tabs.</span></span>  <span data-ttu-id="c534b-127">*IJ* , wobei *i und j =* <1>, 2, 3</span><span class="sxs-lookup"><span data-stu-id="c534b-127">*ij*            where  *i and j =*  <1>, 2, 3</span></span>  <br/> |
   
<span data-ttu-id="c534b-128">Wenn Sie einen Verweis auf die Zelle Alignment aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="c534b-128">To get a reference to the Alignment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c534b-129">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="c534b-129">Section index:</span></span>  <br/> |<span data-ttu-id="c534b-130">**visSectionTab**</span><span class="sxs-lookup"><span data-stu-id="c534b-130">**visSectionTab**</span></span> <br/> |
| <span data-ttu-id="c534b-131">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="c534b-131">Row index:</span></span>  <br/> |<span data-ttu-id="c534b-132">**visRowTab +** *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c534b-132">**visRowTab +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c534b-133">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="c534b-133">Cell index:</span></span>  <br/> | <span data-ttu-id="c534b-134">(*j* \* 3) **+ visTabAlign**</span><span class="sxs-lookup"><span data-stu-id="c534b-134">(*j*  \*3) **+ visTabAlign**</span></span> <br/> |
   

