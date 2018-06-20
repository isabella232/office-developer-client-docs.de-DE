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
ms.openlocfilehash: 13540f9dc5e6e6861d3f3679bcf49204d553397a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797324"
---
# <a name="lineadjustto-cell-page-layout-section"></a><span data-ttu-id="ff7fb-103">LineAdjustTo Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="ff7fb-103">LineAdjustTo Cell (Page Layout Section)</span></span>

<span data-ttu-id="ff7fb-104">Legt fest, welche dynamischen Verbinder übereinander liegen.</span><span class="sxs-lookup"><span data-stu-id="ff7fb-104">Determines which dynamic connectors line up on top of one another.</span></span>
  
|<span data-ttu-id="ff7fb-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ff7fb-105">**Value**</span></span>|<span data-ttu-id="ff7fb-106">**Anpassung**</span><span class="sxs-lookup"><span data-stu-id="ff7fb-106">**Adjustment**</span></span>|<span data-ttu-id="ff7fb-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="ff7fb-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ff7fb-108">0</span><span class="sxs-lookup"><span data-stu-id="ff7fb-108">0</span></span>  <br/> |<span data-ttu-id="ff7fb-109">Standard-Umleitungsformatvorlage</span><span class="sxs-lookup"><span data-stu-id="ff7fb-109">Routing style default</span></span>  <br/> |<span data-ttu-id="ff7fb-110">**visPLOLineAdjustToDefault**</span><span class="sxs-lookup"><span data-stu-id="ff7fb-110">**visPLOLineAdjustToDefault**</span></span> <br/> |
|<span data-ttu-id="ff7fb-111">1</span><span class="sxs-lookup"><span data-stu-id="ff7fb-111">1</span></span>  <br/> |<span data-ttu-id="ff7fb-112">Linien, die nahe beieinander liegen.</span><span class="sxs-lookup"><span data-stu-id="ff7fb-112">Lines that are close to each other</span></span>  <br/> |<span data-ttu-id="ff7fb-113">**visPLOLineAdjustToAll**</span><span class="sxs-lookup"><span data-stu-id="ff7fb-113">**visPLOLineAdjustToAll**</span></span> <br/> |
|<span data-ttu-id="ff7fb-114">2</span><span class="sxs-lookup"><span data-stu-id="ff7fb-114">2</span></span>  <br/> |<span data-ttu-id="ff7fb-115">Keine Linien</span><span class="sxs-lookup"><span data-stu-id="ff7fb-115">No lines</span></span>  <br/> |<span data-ttu-id="ff7fb-116">**visPLOLineAdjustToNone**</span><span class="sxs-lookup"><span data-stu-id="ff7fb-116">**visPLOLineAdjustToNone**</span></span> <br/> |
|<span data-ttu-id="ff7fb-117">3</span><span class="sxs-lookup"><span data-stu-id="ff7fb-117">3</span></span>  <br/> |<span data-ttu-id="ff7fb-118">Verwandte Linien</span><span class="sxs-lookup"><span data-stu-id="ff7fb-118">Related lines</span></span>  <br/> |<span data-ttu-id="ff7fb-119">**visPLOLineAdjustToRelated**</span><span class="sxs-lookup"><span data-stu-id="ff7fb-119">**visPLOLineAdjustToRelated**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff7fb-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ff7fb-120">Remarks</span></span>

<span data-ttu-id="ff7fb-121">Sie können den Wert dieser Zelle auch festlegen, auf der Registerkarte **Layout und Routing** im Dialogfeld **Seite einrichten** (klicken Sie auf der Registerkarte **Entwurf** , klicken Sie auf den Pfeil neben **Seite einrichten** , und klicken Sie dann auf **Layout und Routing**).</span><span class="sxs-lookup"><span data-stu-id="ff7fb-121">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="ff7fb-122">Wenn Sie einen Verweis auf die Zelle LineAdjustTo nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ff7fb-122">To get a reference to the LineAdjustTo cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff7fb-123">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ff7fb-123">Cell name:</span></span>  <br/> |<span data-ttu-id="ff7fb-124">LineAdjustTo</span><span class="sxs-lookup"><span data-stu-id="ff7fb-124">LineAdjustTo</span></span>  <br/> |
   
<span data-ttu-id="ff7fb-125">Wenn Sie einen Verweis auf die Zelle LineAdjustTo aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="ff7fb-125">To get a reference to the LineAdjustTo cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff7fb-126">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ff7fb-126">Section index:</span></span>  <br/> |<span data-ttu-id="ff7fb-127">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ff7fb-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ff7fb-128">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ff7fb-128">Row index:</span></span>  <br/> |<span data-ttu-id="ff7fb-129">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="ff7fb-129">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="ff7fb-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="ff7fb-130">Cell index:</span></span>  <br/> |<span data-ttu-id="ff7fb-131">**visPLOLineAdjustTo**</span><span class="sxs-lookup"><span data-stu-id="ff7fb-131">**visPLOLineAdjustTo**</span></span> <br/> |
   

