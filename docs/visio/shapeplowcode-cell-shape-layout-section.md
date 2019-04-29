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
ms.openlocfilehash: 6e155103f7bfc70a78826297f441fc9ce78942ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423895"
---
# <a name="shapeplowcode-cell-shape-layout-section"></a><span data-ttu-id="5a88f-103">Zelle "ShapePlowCode" (Abschnitt "Shape Layout")</span><span class="sxs-lookup"><span data-stu-id="5a88f-103">ShapePlowCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="5a88f-104">Legt fest, ob dieses platzierbare Shape verschoben wird, wenn Sie ein anderes platzierbares Shape in der Nähe dieses Shapes auf dem Zeichenblatt ablegen.</span><span class="sxs-lookup"><span data-stu-id="5a88f-104">Determines whether this placeable shape moves away when you drop another placeable shape near this shape on the drawing page.</span></span>
  
|<span data-ttu-id="5a88f-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="5a88f-105">**Value**</span></span>|<span data-ttu-id="5a88f-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5a88f-106">**Description**</span></span>|<span data-ttu-id="5a88f-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="5a88f-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5a88f-108">0</span><span class="sxs-lookup"><span data-stu-id="5a88f-108">0</span></span>  <br/> |<span data-ttu-id="5a88f-109">Verschieben nach Blattvorgabe.</span><span class="sxs-lookup"><span data-stu-id="5a88f-109">Plow as page specifies.</span></span>  <br/> |<span data-ttu-id="5a88f-110">**visSLOPlowDefault**</span><span class="sxs-lookup"><span data-stu-id="5a88f-110">**visSLOPlowDefault**</span></span> <br/> |
|<span data-ttu-id="5a88f-111">1</span><span class="sxs-lookup"><span data-stu-id="5a88f-111">1</span></span>  <br/> |<span data-ttu-id="5a88f-112">Keine Shapes verschieben.</span><span class="sxs-lookup"><span data-stu-id="5a88f-112">Plow no shapes.</span></span>  <br/> |<span data-ttu-id="5a88f-113">**visSLOPlowNever**</span><span class="sxs-lookup"><span data-stu-id="5a88f-113">**visSLOPlowNever**</span></span> <br/> |
|<span data-ttu-id="5a88f-114">2</span><span class="sxs-lookup"><span data-stu-id="5a88f-114">2</span></span>  <br/> |<span data-ttu-id="5a88f-115">Jedes Shape verschieben.</span><span class="sxs-lookup"><span data-stu-id="5a88f-115">Plow every shape.</span></span>  <br/> |<span data-ttu-id="5a88f-116">**visSLOPlowAlways**</span><span class="sxs-lookup"><span data-stu-id="5a88f-116">**visSLOPlowAlways**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a88f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a88f-117">Remarks</span></span>

<span data-ttu-id="5a88f-118">Sie können den Wert dieser Zelle für eine bestimmte Form auch im Dialogfeld **Verhalten** auf der Registerkarte **Platzierung** festlegen (bei aktiviertem Shape klicken Sie auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **Shape-Design** auf **Verhalten**, und klicken Sie dann auf die Registerkarte **Platzierung** ).</span><span class="sxs-lookup"><span data-stu-id="5a88f-118">You can also set the value of this cell for a particular shape on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="5a88f-119">Wenn Sie dieses Verhalten für *alle* Formen auf dem Zeichenblatt festlegen möchten, verwenden Sie die Zelle Zelle PlowCode im Abschnitt Seiten Layout.</span><span class="sxs-lookup"><span data-stu-id="5a88f-119">To set this behavior for  *all*  the shapes on the drawing page, use the PlowCode cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="5a88f-120">Wenn Sie einen Verweis auf die Zelle Zelle ShapePlowCode aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="5a88f-120">To get a reference to the ShapePlowCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5a88f-121">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="5a88f-121">Cell name:</span></span>  <br/> |<span data-ttu-id="5a88f-122">Zelle ShapePlowCode</span><span class="sxs-lookup"><span data-stu-id="5a88f-122">ShapePlowCode</span></span>  <br/> |
   
<span data-ttu-id="5a88f-123">Wenn Sie einen Verweis auf die Zelle Zelle ShapePlowCode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="5a88f-123">To get a reference to the ShapePlowCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5a88f-124">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="5a88f-124">Section index:</span></span>  <br/> |<span data-ttu-id="5a88f-125">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5a88f-125">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="5a88f-126">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="5a88f-126">Row index:</span></span>  <br/> |<span data-ttu-id="5a88f-127">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="5a88f-127">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="5a88f-128">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="5a88f-128">Cell index:</span></span>  <br/> |<span data-ttu-id="5a88f-129">**visSLOPlowCode**</span><span class="sxs-lookup"><span data-stu-id="5a88f-129">**visSLOPlowCode**</span></span> <br/> |
   

