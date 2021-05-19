---
title: Zelle "PlowCode" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251660
localization_priority: Normal
ms.assetid: e43f3d29-7def-d36e-ac64-62f0a389d415
description: Legt fest, ob platzierbare Shapes verschoben werden, wenn Sie ein platzierbares Shape in der Nähe eines anderen auf dem Zeichenblatt ablegen.
ms.openlocfilehash: 4ea85ddbaf7662305a2a82fc7f0b814019624841
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420353"
---
# <a name="plowcode-cell-page-layout-section"></a><span data-ttu-id="41466-103">Zelle "PlowCode" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="41466-103">PlowCode Cell (Page Layout Section)</span></span>

<span data-ttu-id="41466-104">Legt fest, ob platzierbare Shapes verschoben werden, wenn Sie ein platzierbares Shape in der Nähe eines anderen auf dem Zeichenblatt ablegen.</span><span class="sxs-lookup"><span data-stu-id="41466-104">Determines whether placeable shapes move away when you drop a placeable shape near another placeable shape on the drawing page.</span></span>
  
|<span data-ttu-id="41466-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="41466-105">**Value**</span></span>|<span data-ttu-id="41466-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="41466-106">**Description**</span></span>|<span data-ttu-id="41466-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="41466-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="41466-108">0</span><span class="sxs-lookup"><span data-stu-id="41466-108">0</span></span>  <br/> |<span data-ttu-id="41466-109">Shapes nicht verschieben</span><span class="sxs-lookup"><span data-stu-id="41466-109">Don't move shapes</span></span>  <br/> |<span data-ttu-id="41466-110">**visPLOPlowNone**</span><span class="sxs-lookup"><span data-stu-id="41466-110">**visPLOPlowNone**</span></span> <br/> |
|<span data-ttu-id="41466-111">1</span><span class="sxs-lookup"><span data-stu-id="41466-111">1</span></span>  <br/> |<span data-ttu-id="41466-112">Shapes verschieben</span><span class="sxs-lookup"><span data-stu-id="41466-112">Move shapes</span></span>  <br/> |<span data-ttu-id="41466-113">**visPLOPlowAll**</span><span class="sxs-lookup"><span data-stu-id="41466-113">**visPLOPlowAll**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41466-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="41466-114">Remarks</span></span>

<span data-ttu-id="41466-115">Sie können den Wert dieser Zelle auch auf der  Registerkarte **Layout** und  Routing im Dialogfeld Seiteneinrichtung festlegen (klicken Sie auf der Registerkarte Entwurf auf den Pfeil Seite **einrichten),** indem Sie das Kontrollkästchen Andere Shapes beim Ablegen weg verschieben aktivieren. </span><span class="sxs-lookup"><span data-stu-id="41466-115">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) by using the **Move other shapes away on drop** check box.</span></span> 
  
<span data-ttu-id="41466-116">Um einen Verweis auf die PlowCode-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="41466-116">To get a reference to the PlowCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="41466-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="41466-117">Cell name:</span></span>  <br/> |<span data-ttu-id="41466-118">PlowCode</span><span class="sxs-lookup"><span data-stu-id="41466-118">PlowCode</span></span>  <br/> |
   
<span data-ttu-id="41466-119">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die PlowCode-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="41466-119">To get a reference to the PlowCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="41466-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="41466-120">Section index:</span></span>  <br/> |<span data-ttu-id="41466-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="41466-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="41466-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="41466-122">Row index:</span></span>  <br/> |<span data-ttu-id="41466-123">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="41466-123">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="41466-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="41466-124">Cell index:</span></span>  <br/> |<span data-ttu-id="41466-125">**visPLOPlowCode**</span><span class="sxs-lookup"><span data-stu-id="41466-125">**visPLOPlowCode**</span></span> <br/> |
   

