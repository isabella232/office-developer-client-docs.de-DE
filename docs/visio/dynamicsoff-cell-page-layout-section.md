---
title: Zelle "DynamicsOff" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251641
localization_priority: Normal
ms.assetid: 055764aa-9681-ffb0-83ce-fdd612fe37af
description: Legt fest, ob platzierbare Shapes verschoben und ob Verbinder um andere Shapes und Verbinder auf dem Zeichenblatt herum umgeleitet werden können.
ms.openlocfilehash: d1075ab1b0512d5db1c7b7a5f2895305318dae7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437476"
---
# <a name="dynamicsoff-cell-page-layout-section"></a><span data-ttu-id="bf3b4-103">Zelle "DynamicsOff" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="bf3b4-103">DynamicsOff Cell (Page Layout Section)</span></span>

<span data-ttu-id="bf3b4-104">Legt fest, ob platzierbare Shapes verschoben und ob Verbinder um andere Shapes und Verbinder auf dem Zeichenblatt herum umgeleitet werden können.</span><span class="sxs-lookup"><span data-stu-id="bf3b4-104">Determines whether placeable shapes move and connectors reroute around other shapes and connectors on the drawing page.</span></span>
  
|<span data-ttu-id="bf3b4-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="bf3b4-105">**Value**</span></span>|<span data-ttu-id="bf3b4-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bf3b4-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="bf3b4-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="bf3b4-107">TRUE</span></span>  <br/> | <span data-ttu-id="bf3b4-108">Dynamik deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="bf3b4-108">Disable dynamics.</span></span>  <br/> |
| <span data-ttu-id="bf3b4-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="bf3b4-109">FALSE</span></span>  <br/> | <span data-ttu-id="bf3b4-110">Dynamik aktivieren.</span><span class="sxs-lookup"><span data-stu-id="bf3b4-110">Enable dynamics.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf3b4-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bf3b4-111">Remarks</span></span>

<span data-ttu-id="bf3b4-p101">Sie können die Dynamik deaktivieren, um die Leistung Ihrer Lösung zu steigern. Wenn Ihre Lösung beispielsweise Shape-Platzierungen in eine Zeichnung einfügt, Sie aber nicht möchten, dass die Anwendung Verbinder umleitet und Shapes neu platziert, sobald Sie ein Shape hinzufügen, können Sie die Dynamik deaktivieren. Aktivieren Sie die Dynamik wieder, nachdem Ihre Lösung die Shapes hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="bf3b4-p101">You can disable dynamics to increase your solution's performance. For example, if your solution adds placeable shapes to a drawing and you don't want the application to reroute connectors and reposition shapes each time you add a shape, you can disable dynamics. After your solution adds the shapes, re-enable dynamics.</span></span>
  
<span data-ttu-id="bf3b4-115">Um einen Verweis auf die DynamicsOff-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="bf3b4-115">To get a reference to the DynamicsOff cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bf3b4-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="bf3b4-116">Cell name:</span></span>  <br/> | <span data-ttu-id="bf3b4-117">DynamicsOff</span><span class="sxs-lookup"><span data-stu-id="bf3b4-117">DynamicsOff</span></span>  <br/> |
   
<span data-ttu-id="bf3b4-118">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die DynamicsOff-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="bf3b4-118">To get a reference to the DynamicsOff cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bf3b4-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="bf3b4-119">Section index:</span></span>  <br/> |<span data-ttu-id="bf3b4-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bf3b4-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bf3b4-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="bf3b4-121">Row index:</span></span>  <br/> |<span data-ttu-id="bf3b4-122">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="bf3b4-122">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="bf3b4-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="bf3b4-123">Cell index:</span></span>  <br/> |<span data-ttu-id="bf3b4-124">**visPLODynamicsOff**</span><span class="sxs-lookup"><span data-stu-id="bf3b4-124">**visPLODynamicsOff**</span></span> <br/> |
   

