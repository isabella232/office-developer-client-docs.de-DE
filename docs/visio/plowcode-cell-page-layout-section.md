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
ms.openlocfilehash: e180ce679f280cbccbda80b67170f2f26473bd8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797650"
---
# <a name="plowcode-cell-page-layout-section"></a><span data-ttu-id="d45aa-103">Zelle "PlowCode" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="d45aa-103">PlowCode Cell (Page Layout Section)</span></span>

<span data-ttu-id="d45aa-104">Legt fest, ob platzierbare Shapes verschoben werden, wenn Sie ein platzierbares Shape in der Nähe eines anderen auf dem Zeichenblatt ablegen.</span><span class="sxs-lookup"><span data-stu-id="d45aa-104">Determines whether placeable shapes move away when you drop a placeable shape near another placeable shape on the drawing page.</span></span>
  
|<span data-ttu-id="d45aa-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d45aa-105">**Value**</span></span>|<span data-ttu-id="d45aa-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d45aa-106">**Description**</span></span>|<span data-ttu-id="d45aa-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="d45aa-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d45aa-108">0</span><span class="sxs-lookup"><span data-stu-id="d45aa-108">0</span></span>  <br/> |<span data-ttu-id="d45aa-109">Shapes nicht verschieben</span><span class="sxs-lookup"><span data-stu-id="d45aa-109">Don't move shapes</span></span>  <br/> |<span data-ttu-id="d45aa-110">**visPLOPlowNone**</span><span class="sxs-lookup"><span data-stu-id="d45aa-110">**visPLOPlowNone**</span></span> <br/> |
|<span data-ttu-id="d45aa-111">1</span><span class="sxs-lookup"><span data-stu-id="d45aa-111">1</span></span>  <br/> |<span data-ttu-id="d45aa-112">Shapes verschieben</span><span class="sxs-lookup"><span data-stu-id="d45aa-112">Move shapes</span></span>  <br/> |<span data-ttu-id="d45aa-113">**visPLOPlowAll**</span><span class="sxs-lookup"><span data-stu-id="d45aa-113">**visPLOPlowAll**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d45aa-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d45aa-114">Remarks</span></span>

<span data-ttu-id="d45aa-115">Sie können den Wert dieser Zelle auch festlegen, auf der Registerkarte **Layout und Routing** im Dialogfeld **Seite einrichten** (klicken Sie auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten** ) mithilfe von das Kontrollkästchen **andere Shapes beim Ablegen abwesend verschieben** .</span><span class="sxs-lookup"><span data-stu-id="d45aa-115">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) by using the **Move other shapes away on drop** check box.</span></span> 
  
<span data-ttu-id="d45aa-116">Wenn Sie einen Verweis auf die Zelle PlowCode nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d45aa-116">To get a reference to the PlowCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d45aa-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="d45aa-117">Cell name:</span></span>  <br/> |<span data-ttu-id="d45aa-118">PlowCode</span><span class="sxs-lookup"><span data-stu-id="d45aa-118">PlowCode</span></span>  <br/> |
   
<span data-ttu-id="d45aa-119">Wenn Sie einen Verweis auf die Zelle PlowCode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="d45aa-119">To get a reference to the PlowCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d45aa-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="d45aa-120">Section index:</span></span>  <br/> |<span data-ttu-id="d45aa-121">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d45aa-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d45aa-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d45aa-122">Row index:</span></span>  <br/> |<span data-ttu-id="d45aa-123">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="d45aa-123">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="d45aa-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="d45aa-124">Cell index:</span></span>  <br/> |<span data-ttu-id="d45aa-125">**visPLOPlowCode**</span><span class="sxs-lookup"><span data-stu-id="d45aa-125">**visPLOPlowCode**</span></span> <br/> |
   

