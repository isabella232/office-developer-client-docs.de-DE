---
title: Zelle "ResizePage" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm850
localization_priority: Normal
ms.assetid: d63fe874-1027-3436-dbc1-73e722bce22e
description: Bestimmt, ob die Seite vergrößert werden soll, um die Zeichnung mit einzuschließen, nachdem Shapes mithilfe des Dialogfelds Layout konfigurieren ausgerichtet wurden (klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout auf Seite neu anordnen, und klicken Sie dann auf Weitere Layoutoptionen).
ms.openlocfilehash: 8d0001ce35808f8c5f11068ed78865ce992af5cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438092"
---
# <a name="resizepage-cell-page-layout-section"></a><span data-ttu-id="a02bd-103">Zelle "ResizePage" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="a02bd-103">ResizePage Cell (Page Layout Section)</span></span>

<span data-ttu-id="a02bd-104">Bestimmt, ob die Seite vergrößert werden soll, um die Zeichnung nach dem Layout von Shapes zu schließen, indem Sie das Dialogfeld **Layout** konfigurieren verwenden (klicken Sie auf der Registerkarte **Entwurf** in der **Gruppe Layout** auf **Seite** neu layout, und klicken Sie dann auf Weitere **Layoutoptionen**).</span><span class="sxs-lookup"><span data-stu-id="a02bd-104">Determines whether to enlarge the page to enclose the drawing after laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout** Page, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="a02bd-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a02bd-105">**Value**</span></span>|<span data-ttu-id="a02bd-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a02bd-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a02bd-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a02bd-107">TRUE</span></span>  <br/> | <span data-ttu-id="a02bd-108">Blatt vergrößern.</span><span class="sxs-lookup"><span data-stu-id="a02bd-108">Enlarge the page.</span></span>  <br/> |
| <span data-ttu-id="a02bd-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a02bd-109">FALSE</span></span>  <br/> | <span data-ttu-id="a02bd-110">Blatt nicht vergrößern.</span><span class="sxs-lookup"><span data-stu-id="a02bd-110">Do not enlarge the page.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a02bd-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a02bd-111">Remarks</span></span>

<span data-ttu-id="a02bd-112">Verwenden Sie zum Erhalten eines Verweises auf die Zelle ResizePage anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="a02bd-112">To get a reference to the ResizePage cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a02bd-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a02bd-113">Cell name:</span></span>  <br/> | <span data-ttu-id="a02bd-114">ResizePage</span><span class="sxs-lookup"><span data-stu-id="a02bd-114">ResizePage</span></span>  <br/> |
   
<span data-ttu-id="a02bd-115">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die ResizePage-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="a02bd-115">To get a reference to the ResizePage cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a02bd-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a02bd-116">Section index:</span></span>  <br/> |<span data-ttu-id="a02bd-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a02bd-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a02bd-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a02bd-118">Row index:</span></span>  <br/> |<span data-ttu-id="a02bd-119">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="a02bd-119">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="a02bd-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a02bd-120">Cell index:</span></span>  <br/> |<span data-ttu-id="a02bd-121">**visPLOResizePage**</span><span class="sxs-lookup"><span data-stu-id="a02bd-121">**visPLOResizePage**</span></span> <br/> |
   

