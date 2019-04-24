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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325606"
---
# <a name="shapeplowcode-cell-shape-layout-section"></a><span data-ttu-id="60d23-103">Zelle "ShapePlowCode" (Abschnitt "Shape Layout")</span><span class="sxs-lookup"><span data-stu-id="60d23-103">ShapePlowCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="60d23-104">Legt fest, ob dieses platzierbare Shape verschoben wird, wenn Sie ein anderes platzierbares Shape in der Nähe dieses Shapes auf dem Zeichenblatt ablegen.</span><span class="sxs-lookup"><span data-stu-id="60d23-104">Determines whether this placeable shape moves away when you drop another placeable shape near this shape on the drawing page.</span></span>
  
|<span data-ttu-id="60d23-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="60d23-105">**Value**</span></span>|<span data-ttu-id="60d23-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="60d23-106">**Description**</span></span>|<span data-ttu-id="60d23-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="60d23-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="60d23-108">0</span><span class="sxs-lookup"><span data-stu-id="60d23-108">0</span></span>  <br/> |<span data-ttu-id="60d23-109">Verschieben nach Blattvorgabe.</span><span class="sxs-lookup"><span data-stu-id="60d23-109">Plow as page specifies.</span></span>  <br/> |<span data-ttu-id="60d23-110">**visSLOPlowDefault**</span><span class="sxs-lookup"><span data-stu-id="60d23-110">**visSLOPlowDefault**</span></span> <br/> |
|<span data-ttu-id="60d23-111">1</span><span class="sxs-lookup"><span data-stu-id="60d23-111">1</span></span>  <br/> |<span data-ttu-id="60d23-112">Keine Shapes verschieben.</span><span class="sxs-lookup"><span data-stu-id="60d23-112">Plow no shapes.</span></span>  <br/> |<span data-ttu-id="60d23-113">**visSLOPlowNever**</span><span class="sxs-lookup"><span data-stu-id="60d23-113">**visSLOPlowNever**</span></span> <br/> |
|<span data-ttu-id="60d23-114">2</span><span class="sxs-lookup"><span data-stu-id="60d23-114">2</span></span>  <br/> |<span data-ttu-id="60d23-115">Jedes Shape verschieben.</span><span class="sxs-lookup"><span data-stu-id="60d23-115">Plow every shape.</span></span>  <br/> |<span data-ttu-id="60d23-116">**visSLOPlowAlways**</span><span class="sxs-lookup"><span data-stu-id="60d23-116">**visSLOPlowAlways**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="60d23-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60d23-117">Remarks</span></span>

<span data-ttu-id="60d23-118">Sie können den Wert dieser Zelle für eine bestimmte Form auch im Dialogfeld **Verhalten** auf der Registerkarte **Platzierung** festlegen (bei aktiviertem Shape klicken Sie auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **Shape-Design** auf **Verhalten**, und klicken Sie dann auf die Registerkarte **Platzierung** ).</span><span class="sxs-lookup"><span data-stu-id="60d23-118">You can also set the value of this cell for a particular shape on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="60d23-119">Wenn Sie dieses Verhalten für *alle* Formen auf dem Zeichenblatt festlegen möchten, verwenden Sie die Zelle Zelle PlowCode im Abschnitt Seiten Layout.</span><span class="sxs-lookup"><span data-stu-id="60d23-119">To set this behavior for  *all*  the shapes on the drawing page, use the PlowCode cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="60d23-120">Wenn Sie einen Verweis auf die Zelle Zelle ShapePlowCode aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="60d23-120">To get a reference to the ShapePlowCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="60d23-121">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="60d23-121">Cell name:</span></span>  <br/> |<span data-ttu-id="60d23-122">Zelle ShapePlowCode</span><span class="sxs-lookup"><span data-stu-id="60d23-122">ShapePlowCode</span></span>  <br/> |
   
<span data-ttu-id="60d23-123">Wenn Sie einen Verweis auf die Zelle Zelle ShapePlowCode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="60d23-123">To get a reference to the ShapePlowCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="60d23-124">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="60d23-124">Section index:</span></span>  <br/> |<span data-ttu-id="60d23-125">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="60d23-125">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="60d23-126">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="60d23-126">Row index:</span></span>  <br/> |<span data-ttu-id="60d23-127">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="60d23-127">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="60d23-128">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="60d23-128">Cell index:</span></span>  <br/> |<span data-ttu-id="60d23-129">**visSLOPlowCode**</span><span class="sxs-lookup"><span data-stu-id="60d23-129">**visSLOPlowCode**</span></span> <br/> |
   

