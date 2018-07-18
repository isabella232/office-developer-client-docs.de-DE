---
title: Zelle "LineAdjustFrom" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251887
localization_priority: Normal
ms.assetid: 6949c717-dc69-1d17-5215-eb6efce56fcb
description: Bestimmt, welche dynamischen Verbinder von der Anwendung getrennt werden, wenn diese übereinander liegen.
ms.openlocfilehash: ee3a107f7e19b53017c2ea24c94babceb49620d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797313"
---
# <a name="lineadjustfrom-cell-page-layout-section"></a><span data-ttu-id="dd3ed-103">LineAdjustFrom Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="dd3ed-103">LineAdjustFrom Cell (Page Layout Section)</span></span>

<span data-ttu-id="dd3ed-104">Bestimmt, welche dynamischen Verbinder von der Anwendung getrennt werden, wenn diese übereinander liegen.</span><span class="sxs-lookup"><span data-stu-id="dd3ed-104">Determines which dynamic connectors the application spaces apart if they route on top of each other.</span></span>
  
|<span data-ttu-id="dd3ed-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="dd3ed-105">**Value**</span></span>|<span data-ttu-id="dd3ed-106">**Ausrichtung**</span><span class="sxs-lookup"><span data-stu-id="dd3ed-106">**Adjustment**</span></span>|<span data-ttu-id="dd3ed-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="dd3ed-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dd3ed-108">0</span><span class="sxs-lookup"><span data-stu-id="dd3ed-108">0</span></span>  <br/> |<span data-ttu-id="dd3ed-109">Nicht verwandte Linien</span><span class="sxs-lookup"><span data-stu-id="dd3ed-109">Unrelated lines</span></span>  <br/> |<span data-ttu-id="dd3ed-110">**visPLOLineAdjustFromNotRelated**</span><span class="sxs-lookup"><span data-stu-id="dd3ed-110">**visPLOLineAdjustFromNotRelated**</span></span> <br/> |
|<span data-ttu-id="dd3ed-111">1</span><span class="sxs-lookup"><span data-stu-id="dd3ed-111">1</span></span>  <br/> |<span data-ttu-id="dd3ed-112">Alle Linien</span><span class="sxs-lookup"><span data-stu-id="dd3ed-112">All lines</span></span>  <br/> |<span data-ttu-id="dd3ed-113">**visPLOLineAdjustFromAll**</span><span class="sxs-lookup"><span data-stu-id="dd3ed-113">**visPLOLineAdjustFromAll**</span></span> <br/> |
|<span data-ttu-id="dd3ed-114">2</span><span class="sxs-lookup"><span data-stu-id="dd3ed-114">2</span></span>  <br/> |<span data-ttu-id="dd3ed-115">Keine Linien</span><span class="sxs-lookup"><span data-stu-id="dd3ed-115">No lines</span></span>  <br/> |<span data-ttu-id="dd3ed-116">**visPLOLineAdjustFromNone**</span><span class="sxs-lookup"><span data-stu-id="dd3ed-116">**visPLOLineAdjustFromNone**</span></span> <br/> |
|<span data-ttu-id="dd3ed-117">3</span><span class="sxs-lookup"><span data-stu-id="dd3ed-117">3</span></span>  <br/> |<span data-ttu-id="dd3ed-118">Standard-Umleitungsformatvorlage</span><span class="sxs-lookup"><span data-stu-id="dd3ed-118">Routing style default</span></span>  <br/> |<span data-ttu-id="dd3ed-119">**visPLOLineAdjustFromRoutingDefault**</span><span class="sxs-lookup"><span data-stu-id="dd3ed-119">**visPLOLineAdjustFromRoutingDefault**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd3ed-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd3ed-120">Remarks</span></span>

<span data-ttu-id="dd3ed-121">Sie können den Wert dieser Zelle auch im Dialogfeld **Seite einrichten** auf der Registerkarte **Layout und Routing** festlegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**, und klicken Sie dann auf **Layout und Routing**).</span><span class="sxs-lookup"><span data-stu-id="dd3ed-121">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="dd3ed-122">Wenn Sie einen Verweis auf die Zelle LineAdjustFrom aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="dd3ed-122">To get a reference to the LineAdjustFrom cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd3ed-123">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="dd3ed-123">Cell name:</span></span>  <br/> |<span data-ttu-id="dd3ed-124">LineAdjustFrom</span><span class="sxs-lookup"><span data-stu-id="dd3ed-124">LineAdjustFrom</span></span>  <br/> |
   
<span data-ttu-id="dd3ed-125">Wenn Sie einen Verweis auf die Zelle LineAdjustFrom aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="dd3ed-125">To get a reference to the LineAdjustFrom cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd3ed-126">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="dd3ed-126">Section index:</span></span>  <br/> |<span data-ttu-id="dd3ed-127">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dd3ed-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="dd3ed-128">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="dd3ed-128">Row index:</span></span>  <br/> |<span data-ttu-id="dd3ed-129">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="dd3ed-129">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="dd3ed-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="dd3ed-130">Cell index:</span></span>  <br/> |<span data-ttu-id="dd3ed-131">**visPLOLineAdjustFrom**</span><span class="sxs-lookup"><span data-stu-id="dd3ed-131">**visPLOLineAdjustFrom**</span></span> <br/> |
   

