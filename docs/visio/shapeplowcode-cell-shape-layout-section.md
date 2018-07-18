---
title: Zelle "ShapePlowCode" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm900
localization_priority: Normal
ms.assetid: acf07fd7-6aa6-1a92-9b7a-bd6fea8a7cb2
description: Legt fest, ob dieses platzierbare Shape verschoben wird, wenn Sie ein anderes platzierbares Shape in der Nähe dieses Shapes auf dem Zeichenblatt ablegen.
ms.openlocfilehash: 5917abad653e7aaf40da05eafa3f9f1a90a2cf9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798038"
---
# <a name="shapeplowcode-cell-shape-layout-section"></a><span data-ttu-id="55d7a-103">ShapePlowCode Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="55d7a-103">ShapePlowCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="55d7a-104">Legt fest, ob dieses platzierbare Shape verschoben wird, wenn Sie ein anderes platzierbares Shape in der Nähe dieses Shapes auf dem Zeichenblatt ablegen.</span><span class="sxs-lookup"><span data-stu-id="55d7a-104">Determines whether this placeable shape moves away when you drop another placeable shape near this shape on the drawing page.</span></span>
  
|<span data-ttu-id="55d7a-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="55d7a-105">**Value**</span></span>|<span data-ttu-id="55d7a-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="55d7a-106">**Description**</span></span>|<span data-ttu-id="55d7a-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="55d7a-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="55d7a-108">0</span><span class="sxs-lookup"><span data-stu-id="55d7a-108">0</span></span>  <br/> |<span data-ttu-id="55d7a-109">Verschieben nach Blattvorgabe.</span><span class="sxs-lookup"><span data-stu-id="55d7a-109">Plow as page specifies.</span></span>  <br/> |<span data-ttu-id="55d7a-110">**visSLOPlowDefault**</span><span class="sxs-lookup"><span data-stu-id="55d7a-110">**visSLOPlowDefault**</span></span> <br/> |
|<span data-ttu-id="55d7a-111">1</span><span class="sxs-lookup"><span data-stu-id="55d7a-111">1</span></span>  <br/> |<span data-ttu-id="55d7a-112">Keine Shapes verschieben.</span><span class="sxs-lookup"><span data-stu-id="55d7a-112">Plow no shapes.</span></span>  <br/> |<span data-ttu-id="55d7a-113">**visSLOPlowNever**</span><span class="sxs-lookup"><span data-stu-id="55d7a-113">**visSLOPlowNever**</span></span> <br/> |
|<span data-ttu-id="55d7a-114">2</span><span class="sxs-lookup"><span data-stu-id="55d7a-114">2</span></span>  <br/> |<span data-ttu-id="55d7a-115">Jedes Shape verschieben.</span><span class="sxs-lookup"><span data-stu-id="55d7a-115">Plow every shape.</span></span>  <br/> |<span data-ttu-id="55d7a-116">**visSLOPlowAlways**</span><span class="sxs-lookup"><span data-stu-id="55d7a-116">**visSLOPlowAlways**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55d7a-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55d7a-117">Remarks</span></span>

<span data-ttu-id="55d7a-118">Sie können auch den Wert dieser Zelle für ein bestimmtes Shape auf der Registerkarte **Platzierung** im Dialogfeld **Verhalten** festlegen (klicken Sie mit einem Shape ausgewählt haben, klicken Sie auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **Shape-Design** auf **Verhalten**, und klicken Sie dann auf die Registerkarte **Platzierung** ).</span><span class="sxs-lookup"><span data-stu-id="55d7a-118">You can also set the value of this cell for a particular shape on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="55d7a-119">Wenn Sie dieses Verhalten für *sämtliche* Shapes auf dem Zeichenblatt festlegen möchten, verwenden Sie die Zelle PlowCode im Abschnitt Page Layout.</span><span class="sxs-lookup"><span data-stu-id="55d7a-119">To set this behavior for  *all*  the shapes on the drawing page, use the PlowCode cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="55d7a-120">Wenn Sie einen Verweis auf die Zelle ShapePlowCode aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="55d7a-120">To get a reference to the ShapePlowCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="55d7a-121">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="55d7a-121">Cell name:</span></span>  <br/> |<span data-ttu-id="55d7a-122">ShapePlowCode</span><span class="sxs-lookup"><span data-stu-id="55d7a-122">ShapePlowCode</span></span>  <br/> |
   
<span data-ttu-id="55d7a-123">Wenn Sie einen Verweis auf die Zelle ShapePlowCode aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="55d7a-123">To get a reference to the ShapePlowCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="55d7a-124">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="55d7a-124">Section index:</span></span>  <br/> |<span data-ttu-id="55d7a-125">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="55d7a-125">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="55d7a-126">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="55d7a-126">Row index:</span></span>  <br/> |<span data-ttu-id="55d7a-127">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="55d7a-127">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="55d7a-128">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="55d7a-128">Cell index:</span></span>  <br/> |<span data-ttu-id="55d7a-129">**visSLOPlowCode**</span><span class="sxs-lookup"><span data-stu-id="55d7a-129">**visSLOPlowCode**</span></span> <br/> |
   

