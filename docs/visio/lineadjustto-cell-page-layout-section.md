---
title: Zelle "LineAdjustTo" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm525
localization_priority: Normal
ms.assetid: 81cd9670-8a6f-824b-528c-e9b88c86f525
description: Legt fest, welche dynamischen Verbinder übereinander liegen.
ms.openlocfilehash: e4fb32c0fcb488173324ea597edc2c9d13f6bfca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414025"
---
# <a name="lineadjustto-cell-page-layout-section"></a><span data-ttu-id="7423e-103">Zelle "LineAdjustTo" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="7423e-103">LineAdjustTo Cell (Page Layout Section)</span></span>

<span data-ttu-id="7423e-104">Legt fest, welche dynamischen Verbinder übereinander liegen.</span><span class="sxs-lookup"><span data-stu-id="7423e-104">Determines which dynamic connectors line up on top of one another.</span></span>
  
|<span data-ttu-id="7423e-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="7423e-105">**Value**</span></span>|<span data-ttu-id="7423e-106">**Anpassung**</span><span class="sxs-lookup"><span data-stu-id="7423e-106">**Adjustment**</span></span>|<span data-ttu-id="7423e-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="7423e-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7423e-108">0</span><span class="sxs-lookup"><span data-stu-id="7423e-108">0</span></span>  <br/> |<span data-ttu-id="7423e-109">Standard-Umleitungsformatvorlage</span><span class="sxs-lookup"><span data-stu-id="7423e-109">Routing style default</span></span>  <br/> |<span data-ttu-id="7423e-110">**visPLOLineAdjustToDefault**</span><span class="sxs-lookup"><span data-stu-id="7423e-110">**visPLOLineAdjustToDefault**</span></span> <br/> |
|<span data-ttu-id="7423e-111">1</span><span class="sxs-lookup"><span data-stu-id="7423e-111">1</span></span>  <br/> |<span data-ttu-id="7423e-112">Linien, die nahe beieinander liegen.</span><span class="sxs-lookup"><span data-stu-id="7423e-112">Lines that are close to each other</span></span>  <br/> |<span data-ttu-id="7423e-113">**visPLOLineAdjustToAll**</span><span class="sxs-lookup"><span data-stu-id="7423e-113">**visPLOLineAdjustToAll**</span></span> <br/> |
|<span data-ttu-id="7423e-114">2</span><span class="sxs-lookup"><span data-stu-id="7423e-114">2</span></span>  <br/> |<span data-ttu-id="7423e-115">Keine Linien</span><span class="sxs-lookup"><span data-stu-id="7423e-115">No lines</span></span>  <br/> |<span data-ttu-id="7423e-116">**visPLOLineAdjustToNone**</span><span class="sxs-lookup"><span data-stu-id="7423e-116">**visPLOLineAdjustToNone**</span></span> <br/> |
|<span data-ttu-id="7423e-117">3</span><span class="sxs-lookup"><span data-stu-id="7423e-117">3</span></span>  <br/> |<span data-ttu-id="7423e-118">Verwandte Linien</span><span class="sxs-lookup"><span data-stu-id="7423e-118">Related lines</span></span>  <br/> |<span data-ttu-id="7423e-119">**visPLOLineAdjustToRelated**</span><span class="sxs-lookup"><span data-stu-id="7423e-119">**visPLOLineAdjustToRelated**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7423e-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7423e-120">Remarks</span></span>

<span data-ttu-id="7423e-121">Sie können den Wert dieser Zelle auch im Dialogfeld **Seite einrichten** auf der Registerkarte **Layout und Routing** festlegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**, und klicken Sie dann auf **Layout und Routing**).</span><span class="sxs-lookup"><span data-stu-id="7423e-121">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="7423e-122">Um einen Verweis auf die Zelle LineAdjustTo anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="7423e-122">To get a reference to the LineAdjustTo cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7423e-123">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="7423e-123">Cell name:</span></span>  <br/> |<span data-ttu-id="7423e-124">LineAdjustTo</span><span class="sxs-lookup"><span data-stu-id="7423e-124">LineAdjustTo</span></span>  <br/> |
   
<span data-ttu-id="7423e-125">Um einen Verweis auf die LineAdjustTo-Zelle nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="7423e-125">To get a reference to the LineAdjustTo cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7423e-126">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="7423e-126">Section index:</span></span>  <br/> |<span data-ttu-id="7423e-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7423e-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="7423e-128">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="7423e-128">Row index:</span></span>  <br/> |<span data-ttu-id="7423e-129">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="7423e-129">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="7423e-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="7423e-130">Cell index:</span></span>  <br/> |<span data-ttu-id="7423e-131">**visPLOLineAdjustTo**</span><span class="sxs-lookup"><span data-stu-id="7423e-131">**visPLOLineAdjustTo**</span></span> <br/> |
   

