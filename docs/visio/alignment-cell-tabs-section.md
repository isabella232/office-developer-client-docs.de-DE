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
ms.openlocfilehash: a2178c63d0005ee8b2f0c8ebcfbc25854a5b1567
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796385"
---
# <a name="alignment-cell-tabs-section"></a><span data-ttu-id="93f1c-103">Alignment Cell (Tabs Section)</span><span class="sxs-lookup"><span data-stu-id="93f1c-103">Alignment Cell (Tabs Section)</span></span>

<span data-ttu-id="93f1c-104">Legt die Tabausrichtung fest.</span><span class="sxs-lookup"><span data-stu-id="93f1c-104">Specifies the tab alignment.</span></span>
  
|<span data-ttu-id="93f1c-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="93f1c-105">**Value**</span></span>|<span data-ttu-id="93f1c-106">**Ausrichtung**</span><span class="sxs-lookup"><span data-stu-id="93f1c-106">**Alignment**</span></span>|<span data-ttu-id="93f1c-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="93f1c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="93f1c-108">0</span><span class="sxs-lookup"><span data-stu-id="93f1c-108">0</span></span>  <br/> | <span data-ttu-id="93f1c-109">Links</span><span class="sxs-lookup"><span data-stu-id="93f1c-109">Left</span></span>  <br/> |<span data-ttu-id="93f1c-110">**visTabStopLeft**</span><span class="sxs-lookup"><span data-stu-id="93f1c-110">**visTabStopLeft**</span></span> <br/> |
| <span data-ttu-id="93f1c-111">1</span><span class="sxs-lookup"><span data-stu-id="93f1c-111">1</span></span>  <br/> | <span data-ttu-id="93f1c-112">Mittig</span><span class="sxs-lookup"><span data-stu-id="93f1c-112">Center</span></span>  <br/> |<span data-ttu-id="93f1c-113">**visTabStopCenter**</span><span class="sxs-lookup"><span data-stu-id="93f1c-113">**visTabStopCenter**</span></span> <br/> |
| <span data-ttu-id="93f1c-114">2</span><span class="sxs-lookup"><span data-stu-id="93f1c-114">2</span></span>  <br/> | <span data-ttu-id="93f1c-115">Nach rechts</span><span class="sxs-lookup"><span data-stu-id="93f1c-115">Right</span></span>  <br/> |<span data-ttu-id="93f1c-116">**visTabStopRight**</span><span class="sxs-lookup"><span data-stu-id="93f1c-116">**visTabStopRight**</span></span> <br/> |
| <span data-ttu-id="93f1c-117">3</span><span class="sxs-lookup"><span data-stu-id="93f1c-117">3</span></span>  <br/> | <span data-ttu-id="93f1c-118">Dezimalwert</span><span class="sxs-lookup"><span data-stu-id="93f1c-118">Decimal</span></span>  <br/> |<span data-ttu-id="93f1c-119">**visTabStopDecimal**</span><span class="sxs-lookup"><span data-stu-id="93f1c-119">**visTabStopDecimal**</span></span> <br/> |
| <span data-ttu-id="93f1c-120">4</span><span class="sxs-lookup"><span data-stu-id="93f1c-120">4</span></span>  <br/> | <span data-ttu-id="93f1c-121">Komma</span><span class="sxs-lookup"><span data-stu-id="93f1c-121">Comma</span></span>  <br/> |<span data-ttu-id="93f1c-122">**visTabStopComma**</span><span class="sxs-lookup"><span data-stu-id="93f1c-122">**visTabStopComma**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93f1c-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="93f1c-123">Remarks</span></span>

<span data-ttu-id="93f1c-124">Wenn Sie einen Verweis auf die Zelle Alignment aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="93f1c-124">To get a reference to the Alignment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="93f1c-125">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="93f1c-125">Cell name:</span></span>  <br/> | <span data-ttu-id="93f1c-126">Registerkarten.</span><span class="sxs-lookup"><span data-stu-id="93f1c-126">Tabs.</span></span>  <span data-ttu-id="93f1c-127">*Ij* , in dem *i und j =* < 1 >, 2, 3</span><span class="sxs-lookup"><span data-stu-id="93f1c-127">*ij*            where  *i and j =*  <1>, 2, 3</span></span>  <br/> |
   
<span data-ttu-id="93f1c-128">Wenn Sie einen Verweis auf die Zelle Alignment aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="93f1c-128">To get a reference to the Alignment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="93f1c-129">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="93f1c-129">Section index:</span></span>  <br/> |<span data-ttu-id="93f1c-130">**visSectionTab**</span><span class="sxs-lookup"><span data-stu-id="93f1c-130">**visSectionTab**</span></span> <br/> |
| <span data-ttu-id="93f1c-131">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="93f1c-131">Row index:</span></span>  <br/> |<span data-ttu-id="93f1c-132">**VisRowTab +** *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="93f1c-132">**visRowTab +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="93f1c-133">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="93f1c-133">Cell index:</span></span>  <br/> | <span data-ttu-id="93f1c-134">(*j* \* 3) **+ VisTabAlign**</span><span class="sxs-lookup"><span data-stu-id="93f1c-134">(*j*  \*3) **+ visTabAlign**</span></span> <br/> |
   

