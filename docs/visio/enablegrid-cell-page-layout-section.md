---
title: Zelle "EnableGrid" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251642
localization_priority: Normal
ms.assetid: bfea4ef4-1b30-eb22-215d-3b9b73098da9
description: Bestimmt, ob die Anwendung Shapes an einem internen unsichtbaren Zeichenblattgitter ausrichtet, wenn Sie das Layout im Dialogfeld Layout konfigurieren festlegen. (Klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout auf Seite neu anordnen, und klicken Sie dann auf Weitere Layoutoptionen.)
ms.openlocfilehash: 3371767343132219ebc38134b93afd1da46c7a45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796928"
---
# <a name="enablegrid-cell-page-layout-section"></a><span data-ttu-id="a19ed-104">EnableGrid Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="a19ed-104">EnableGrid Cell (Page Layout Section)</span></span>

<span data-ttu-id="a19ed-p102">Bestimmt, ob die Anwendung Shapes an einem internen unsichtbaren Zeichenblattgitter ausrichtet, wenn Sie das Layout im Dialogfeld **Layout konfigurieren** festlegen. (Klicken Sie auf der Registerkarte **Entwurf** in der Gruppe **Layout** auf **Seite neu anordnen**, und klicken Sie dann auf **Weitere Layoutoptionen**.)</span><span class="sxs-lookup"><span data-stu-id="a19ed-p102">Determines whether the application lays out shapes based on an internal, invisible page grid when you configure the layout in the **Configure Layout** dialog box. (On the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**.)</span></span>
  
|<span data-ttu-id="a19ed-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a19ed-107">**Value**</span></span>|<span data-ttu-id="a19ed-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a19ed-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a19ed-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="a19ed-109">TRUE</span></span>  <br/> |<span data-ttu-id="a19ed-110">Internes Zeichenblattgitter verwenden.</span><span class="sxs-lookup"><span data-stu-id="a19ed-110">Use the internal page grid.</span></span>  <br/> |
|<span data-ttu-id="a19ed-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="a19ed-111">FALSE</span></span>  <br/> |<span data-ttu-id="a19ed-112">Internes Zeichenblattgitter nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="a19ed-112">Do not use the internal page grid.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a19ed-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a19ed-113">Remarks</span></span>

<span data-ttu-id="a19ed-p103">Sie erstellen dieses Zeichenblattgitter im Dialogfeld **Abstände für Layout und Routing** mit den Werten **Abstand zwischen Shapes** und **Durchschnittliche Shape-Größe**. (Klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**, wählen Sie **Layout und Routing** aus, und klicken Sie dann auf **Abstand**.)</span><span class="sxs-lookup"><span data-stu-id="a19ed-p103">You create this page grid by using the **Space between shapes** and the **Average shape size** values in the **Layout and Routing Spacing** dialog box. (On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span> 
  
<span data-ttu-id="a19ed-116">Wenn Sie dieses Feature aktivieren, richtet die Anwendung den Zentralpunkt jedes platzierbaren Shapes an der Mitte eines Blocks auf dem internen Seitenraster aus.</span><span class="sxs-lookup"><span data-stu-id="a19ed-116">When you enable this feature, the application aligns each placeable shape's center point with the center of a block on the internal page grid.</span></span> 
  
<span data-ttu-id="a19ed-117">Wenn Sie einen Verweis auf die Zelle EnableGrid aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a19ed-117">To get a reference to the EnableGrid cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a19ed-118">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a19ed-118">Cell name:</span></span>  <br/> |<span data-ttu-id="a19ed-119">EnableGrid</span><span class="sxs-lookup"><span data-stu-id="a19ed-119">EnableGrid</span></span>  <br/> |
   
<span data-ttu-id="a19ed-120">Wenn Sie einen Verweis auf die Zelle EnableGrid aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a19ed-120">To get a reference to the EnableGrid cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a19ed-121">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a19ed-121">Section index:</span></span>  <br/> |<span data-ttu-id="a19ed-122">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a19ed-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a19ed-123">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a19ed-123">Row index:</span></span>  <br/> |<span data-ttu-id="a19ed-124">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="a19ed-124">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="a19ed-125">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a19ed-125">Cell index:</span></span>  <br/> |<span data-ttu-id="a19ed-126">**visPLOEnableGrid**</span><span class="sxs-lookup"><span data-stu-id="a19ed-126">**visPLOEnableGrid**</span></span> <br/> |
   

