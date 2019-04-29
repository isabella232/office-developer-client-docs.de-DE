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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425540"
---
# <a name="alignment-cell-tabs-section"></a><span data-ttu-id="e6167-103">Zelle "Alignment" (Abschnitt "Tabs")</span><span class="sxs-lookup"><span data-stu-id="e6167-103">Alignment Cell (Tabs Section)</span></span>

<span data-ttu-id="e6167-104">Legt die Tabausrichtung fest.</span><span class="sxs-lookup"><span data-stu-id="e6167-104">Specifies the tab alignment.</span></span>
  
|<span data-ttu-id="e6167-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e6167-105">**Value**</span></span>|<span data-ttu-id="e6167-106">**Alignment**</span><span class="sxs-lookup"><span data-stu-id="e6167-106">**Alignment**</span></span>|<span data-ttu-id="e6167-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="e6167-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="e6167-108">0</span><span class="sxs-lookup"><span data-stu-id="e6167-108">0</span></span>  <br/> | <span data-ttu-id="e6167-109">Left</span><span class="sxs-lookup"><span data-stu-id="e6167-109">Left</span></span>  <br/> |<span data-ttu-id="e6167-110">**visTabStopLeft**</span><span class="sxs-lookup"><span data-stu-id="e6167-110">**visTabStopLeft**</span></span> <br/> |
| <span data-ttu-id="e6167-111">1</span><span class="sxs-lookup"><span data-stu-id="e6167-111">1</span></span>  <br/> | <span data-ttu-id="e6167-112">Zentriert</span><span class="sxs-lookup"><span data-stu-id="e6167-112">Center</span></span>  <br/> |<span data-ttu-id="e6167-113">**visTabStopCenter**</span><span class="sxs-lookup"><span data-stu-id="e6167-113">**visTabStopCenter**</span></span> <br/> |
| <span data-ttu-id="e6167-114">2</span><span class="sxs-lookup"><span data-stu-id="e6167-114">2</span></span>  <br/> | <span data-ttu-id="e6167-115">Nach rechts</span><span class="sxs-lookup"><span data-stu-id="e6167-115">Right</span></span>  <br/> |<span data-ttu-id="e6167-116">**visTabStopRight**</span><span class="sxs-lookup"><span data-stu-id="e6167-116">**visTabStopRight**</span></span> <br/> |
| <span data-ttu-id="e6167-117">3</span><span class="sxs-lookup"><span data-stu-id="e6167-117">3</span></span>  <br/> | <span data-ttu-id="e6167-118">Decimal</span><span class="sxs-lookup"><span data-stu-id="e6167-118">Decimal</span></span>  <br/> |<span data-ttu-id="e6167-119">**visTabStopDecimal**</span><span class="sxs-lookup"><span data-stu-id="e6167-119">**visTabStopDecimal**</span></span> <br/> |
| <span data-ttu-id="e6167-120">4</span><span class="sxs-lookup"><span data-stu-id="e6167-120">4</span></span>  <br/> | <span data-ttu-id="e6167-121">Komma</span><span class="sxs-lookup"><span data-stu-id="e6167-121">Comma</span></span>  <br/> |<span data-ttu-id="e6167-122">**visTabStopComma**</span><span class="sxs-lookup"><span data-stu-id="e6167-122">**visTabStopComma**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6167-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6167-123">Remarks</span></span>

<span data-ttu-id="e6167-124">Wenn Sie einen Verweis auf die Zelle Alignment aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e6167-124">To get a reference to the Alignment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e6167-125">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="e6167-125">Cell name:</span></span>  <br/> | <span data-ttu-id="e6167-126">Registerkarten.</span><span class="sxs-lookup"><span data-stu-id="e6167-126">Tabs.</span></span>  <span data-ttu-id="e6167-127">*IJ* , wobei *i und j =* <1>, 2, 3</span><span class="sxs-lookup"><span data-stu-id="e6167-127">*ij*            where  *i and j =*  <1>, 2, 3</span></span>  <br/> |
   
<span data-ttu-id="e6167-128">Wenn Sie einen Verweis auf die Zelle Alignment aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="e6167-128">To get a reference to the Alignment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e6167-129">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="e6167-129">Section index:</span></span>  <br/> |<span data-ttu-id="e6167-130">**visSectionTab**</span><span class="sxs-lookup"><span data-stu-id="e6167-130">**visSectionTab**</span></span> <br/> |
| <span data-ttu-id="e6167-131">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="e6167-131">Row index:</span></span>  <br/> |<span data-ttu-id="e6167-132">**visRowTab +** *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e6167-132">**visRowTab +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e6167-133">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="e6167-133">Cell index:</span></span>  <br/> | <span data-ttu-id="e6167-134">(*j* \* 3) **+ visTabAlign**</span><span class="sxs-lookup"><span data-stu-id="e6167-134">(*j*  \*3) **+ visTabAlign**</span></span> <br/> |
   

