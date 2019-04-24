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
ms.openlocfilehash: 3eb9f5513ee3ce2f5dce96cb47c356bca29a289c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359325"
---
# <a name="lineadjustfrom-cell-page-layout-section"></a><span data-ttu-id="1f677-103">Zelle "LineAdjustFrom" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="1f677-103">LineAdjustFrom Cell (Page Layout Section)</span></span>

<span data-ttu-id="1f677-104">Bestimmt, welche dynamischen Verbinder von der Anwendung getrennt werden, wenn diese übereinander liegen.</span><span class="sxs-lookup"><span data-stu-id="1f677-104">Determines which dynamic connectors the application spaces apart if they route on top of each other.</span></span>
  
|<span data-ttu-id="1f677-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="1f677-105">**Value**</span></span>|<span data-ttu-id="1f677-106">**Anpassung**</span><span class="sxs-lookup"><span data-stu-id="1f677-106">**Adjustment**</span></span>|<span data-ttu-id="1f677-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="1f677-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1f677-108">0</span><span class="sxs-lookup"><span data-stu-id="1f677-108">0</span></span>  <br/> |<span data-ttu-id="1f677-109">Nicht verwandte Linien</span><span class="sxs-lookup"><span data-stu-id="1f677-109">Unrelated lines</span></span>  <br/> |<span data-ttu-id="1f677-110">**visPLOLineAdjustFromNotRelated**</span><span class="sxs-lookup"><span data-stu-id="1f677-110">**visPLOLineAdjustFromNotRelated**</span></span> <br/> |
|<span data-ttu-id="1f677-111">1</span><span class="sxs-lookup"><span data-stu-id="1f677-111">1</span></span>  <br/> |<span data-ttu-id="1f677-112">Alle Linien</span><span class="sxs-lookup"><span data-stu-id="1f677-112">All lines</span></span>  <br/> |<span data-ttu-id="1f677-113">**visPLOLineAdjustFromAll**</span><span class="sxs-lookup"><span data-stu-id="1f677-113">**visPLOLineAdjustFromAll**</span></span> <br/> |
|<span data-ttu-id="1f677-114">2</span><span class="sxs-lookup"><span data-stu-id="1f677-114">2</span></span>  <br/> |<span data-ttu-id="1f677-115">Keine Linien</span><span class="sxs-lookup"><span data-stu-id="1f677-115">No lines</span></span>  <br/> |<span data-ttu-id="1f677-116">**visPLOLineAdjustFromNone**</span><span class="sxs-lookup"><span data-stu-id="1f677-116">**visPLOLineAdjustFromNone**</span></span> <br/> |
|<span data-ttu-id="1f677-117">3</span><span class="sxs-lookup"><span data-stu-id="1f677-117">3</span></span>  <br/> |<span data-ttu-id="1f677-118">Standard-Umleitungsformatvorlage</span><span class="sxs-lookup"><span data-stu-id="1f677-118">Routing style default</span></span>  <br/> |<span data-ttu-id="1f677-119">**visPLOLineAdjustFromRoutingDefault**</span><span class="sxs-lookup"><span data-stu-id="1f677-119">**visPLOLineAdjustFromRoutingDefault**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f677-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f677-120">Remarks</span></span>

<span data-ttu-id="1f677-121">Sie können den Wert dieser Zelle auch im Dialogfeld **Seite einrichten** auf der Registerkarte **Layout und Routing** festlegen (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**, und klicken Sie dann auf **Layout und Routing**).</span><span class="sxs-lookup"><span data-stu-id="1f677-121">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="1f677-122">Wenn Sie einen Verweis auf die Zelle Zelle LineAdjustFrom aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1f677-122">To get a reference to the LineAdjustFrom cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1f677-123">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="1f677-123">Cell name:</span></span>  <br/> |<span data-ttu-id="1f677-124">Zelle LineAdjustFrom</span><span class="sxs-lookup"><span data-stu-id="1f677-124">LineAdjustFrom</span></span>  <br/> |
   
<span data-ttu-id="1f677-125">Wenn Sie einen Verweis auf die Zelle Zelle LineAdjustFrom aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="1f677-125">To get a reference to the LineAdjustFrom cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1f677-126">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="1f677-126">Section index:</span></span>  <br/> |<span data-ttu-id="1f677-127">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1f677-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="1f677-128">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="1f677-128">Row index:</span></span>  <br/> |<span data-ttu-id="1f677-129">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="1f677-129">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="1f677-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="1f677-130">Cell index:</span></span>  <br/> |<span data-ttu-id="1f677-131">**visPLOLineAdjustFrom**</span><span class="sxs-lookup"><span data-stu-id="1f677-131">**visPLOLineAdjustFrom**</span></span> <br/> |
   

