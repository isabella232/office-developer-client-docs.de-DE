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
# <a name="lineadjustfrom-cell-page-layout-section"></a><span data-ttu-id="a7252-103">LineAdjustFrom Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="a7252-103">LineAdjustFrom Cell (Page Layout Section)</span></span>

<span data-ttu-id="a7252-104">Bestimmt, welche dynamischen Verbinder von der Anwendung getrennt werden, wenn diese übereinander liegen.</span><span class="sxs-lookup"><span data-stu-id="a7252-104">Determines which dynamic connectors the application spaces apart if they route on top of each other.</span></span>
  
|<span data-ttu-id="a7252-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a7252-105">**Value**</span></span>|<span data-ttu-id="a7252-106">**Anpassung**</span><span class="sxs-lookup"><span data-stu-id="a7252-106">**Adjustment**</span></span>|<span data-ttu-id="a7252-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="a7252-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a7252-108">0</span><span class="sxs-lookup"><span data-stu-id="a7252-108">0</span></span>  <br/> |<span data-ttu-id="a7252-109">Nicht verwandte Linien</span><span class="sxs-lookup"><span data-stu-id="a7252-109">Unrelated lines</span></span>  <br/> |<span data-ttu-id="a7252-110">**visPLOLineAdjustFromNotRelated**</span><span class="sxs-lookup"><span data-stu-id="a7252-110">**visPLOLineAdjustFromNotRelated**</span></span> <br/> |
|<span data-ttu-id="a7252-111">1</span><span class="sxs-lookup"><span data-stu-id="a7252-111">1</span></span>  <br/> |<span data-ttu-id="a7252-112">Alle Linien</span><span class="sxs-lookup"><span data-stu-id="a7252-112">All lines</span></span>  <br/> |<span data-ttu-id="a7252-113">**visPLOLineAdjustFromAll**</span><span class="sxs-lookup"><span data-stu-id="a7252-113">**visPLOLineAdjustFromAll**</span></span> <br/> |
|<span data-ttu-id="a7252-114">2</span><span class="sxs-lookup"><span data-stu-id="a7252-114">2</span></span>  <br/> |<span data-ttu-id="a7252-115">Keine Linien</span><span class="sxs-lookup"><span data-stu-id="a7252-115">No lines</span></span>  <br/> |<span data-ttu-id="a7252-116">**visPLOLineAdjustFromNone**</span><span class="sxs-lookup"><span data-stu-id="a7252-116">**visPLOLineAdjustFromNone**</span></span> <br/> |
|<span data-ttu-id="a7252-117">3</span><span class="sxs-lookup"><span data-stu-id="a7252-117">3</span></span>  <br/> |<span data-ttu-id="a7252-118">Standard-Umleitungsformatvorlage</span><span class="sxs-lookup"><span data-stu-id="a7252-118">Routing style default</span></span>  <br/> |<span data-ttu-id="a7252-119">**visPLOLineAdjustFromRoutingDefault**</span><span class="sxs-lookup"><span data-stu-id="a7252-119">**visPLOLineAdjustFromRoutingDefault**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7252-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a7252-120">Remarks</span></span>

<span data-ttu-id="a7252-121">Sie können den Wert dieser Zelle auch festlegen, auf der Registerkarte **Layout und Routing** im Dialogfeld **Seite einrichten** (klicken Sie auf der Registerkarte **Entwurf** , klicken Sie auf den Pfeil neben **Seite einrichten** , und klicken Sie dann auf **Layout und Routing**).</span><span class="sxs-lookup"><span data-stu-id="a7252-121">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="a7252-122">Wenn Sie einen Verweis auf die Zelle LineAdjustFrom nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a7252-122">To get a reference to the LineAdjustFrom cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a7252-123">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a7252-123">Cell name:</span></span>  <br/> |<span data-ttu-id="a7252-124">LineAdjustFrom</span><span class="sxs-lookup"><span data-stu-id="a7252-124">LineAdjustFrom</span></span>  <br/> |
   
<span data-ttu-id="a7252-125">Wenn Sie einen Verweis auf die Zelle LineAdjustFrom aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a7252-125">To get a reference to the LineAdjustFrom cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a7252-126">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a7252-126">Section index:</span></span>  <br/> |<span data-ttu-id="a7252-127">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a7252-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a7252-128">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a7252-128">Row index:</span></span>  <br/> |<span data-ttu-id="a7252-129">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="a7252-129">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="a7252-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a7252-130">Cell index:</span></span>  <br/> |<span data-ttu-id="a7252-131">**visPLOLineAdjustFrom**</span><span class="sxs-lookup"><span data-stu-id="a7252-131">**visPLOLineAdjustFrom**</span></span> <br/> |
   

