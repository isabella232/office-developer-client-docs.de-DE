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
description: Bestimmt, ob die Seite, um die Zeichnung, nachdem das Layout von Shapes mithilfe des Dialogfelds Layout konfigurieren einzuschließen, vergrößert (klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout, klicken Sie auf der Seite Re-Layout, und klicken Sie dann auf Weitere Layoutoptionen).
ms.openlocfilehash: fab37ee4561ba82ea1f314ad595e513253478b30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797853"
---
# <a name="resizepage-cell-page-layout-section"></a><span data-ttu-id="e1e40-103">Zelle "ResizePage" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="e1e40-103">ResizePage Cell (Page Layout Section)</span></span>

<span data-ttu-id="e1e40-104">Bestimmt, ob die Seite, um die Zeichnung, nachdem das Layout von Shapes mithilfe des Dialogfelds **Layout konfigurieren** einzuschließen, vergrößert (auf der Registerkarte **Entwurf** in der Gruppe **Layout** klicken Sie auf der Seite **Re-Layout** , und klicken Sie dann auf **mehr Layout Optionen**).</span><span class="sxs-lookup"><span data-stu-id="e1e40-104">Determines whether to enlarge the page to enclose the drawing after laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout** Page, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="e1e40-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e1e40-105">**Value**</span></span>|<span data-ttu-id="e1e40-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e1e40-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e1e40-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="e1e40-107">TRUE</span></span>  <br/> | <span data-ttu-id="e1e40-108">Blatt vergrößern.</span><span class="sxs-lookup"><span data-stu-id="e1e40-108">Enlarge the page.</span></span>  <br/> |
| <span data-ttu-id="e1e40-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="e1e40-109">FALSE</span></span>  <br/> | <span data-ttu-id="e1e40-110">Blatt nicht vergrößern.</span><span class="sxs-lookup"><span data-stu-id="e1e40-110">Do not enlarge the page.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1e40-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1e40-111">Remarks</span></span>

<span data-ttu-id="e1e40-112">Zum Abrufen eines Verweises auf die Zelle ResizePage nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e1e40-112">To get a reference to the ResizePage cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e1e40-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="e1e40-113">Cell name:</span></span>  <br/> | <span data-ttu-id="e1e40-114">ResizePage</span><span class="sxs-lookup"><span data-stu-id="e1e40-114">ResizePage</span></span>  <br/> |
   
<span data-ttu-id="e1e40-115">Wenn Sie einen Verweis auf die Zelle ResizePage aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="e1e40-115">To get a reference to the ResizePage cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e1e40-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="e1e40-116">Section index:</span></span>  <br/> |<span data-ttu-id="e1e40-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e1e40-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e1e40-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="e1e40-118">Row index:</span></span>  <br/> |<span data-ttu-id="e1e40-119">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="e1e40-119">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="e1e40-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="e1e40-120">Cell index:</span></span>  <br/> |<span data-ttu-id="e1e40-121">**visPLOResizePage**</span><span class="sxs-lookup"><span data-stu-id="e1e40-121">**visPLOResizePage**</span></span> <br/> |
   

