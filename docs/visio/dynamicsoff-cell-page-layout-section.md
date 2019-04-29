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
# <a name="dynamicsoff-cell-page-layout-section"></a><span data-ttu-id="9008d-103">Zelle "DynamicsOff" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="9008d-103">DynamicsOff Cell (Page Layout Section)</span></span>

<span data-ttu-id="9008d-104">Legt fest, ob platzierbare Shapes verschoben und ob Verbinder um andere Shapes und Verbinder auf dem Zeichenblatt herum umgeleitet werden können.</span><span class="sxs-lookup"><span data-stu-id="9008d-104">Determines whether placeable shapes move and connectors reroute around other shapes and connectors on the drawing page.</span></span>
  
|<span data-ttu-id="9008d-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9008d-105">**Value**</span></span>|<span data-ttu-id="9008d-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9008d-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="9008d-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="9008d-107">TRUE</span></span>  <br/> | <span data-ttu-id="9008d-108">Dynamik deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="9008d-108">Disable dynamics.</span></span>  <br/> |
| <span data-ttu-id="9008d-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="9008d-109">FALSE</span></span>  <br/> | <span data-ttu-id="9008d-110">Dynamik aktivieren.</span><span class="sxs-lookup"><span data-stu-id="9008d-110">Enable dynamics.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9008d-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9008d-111">Remarks</span></span>

<span data-ttu-id="9008d-p101">Sie können die Dynamik deaktivieren, um die Leistung Ihrer Lösung zu steigern. Wenn Ihre Lösung beispielsweise Shape-Platzierungen in eine Zeichnung einfügt, Sie aber nicht möchten, dass die Anwendung Verbinder umleitet und Shapes neu platziert, sobald Sie ein Shape hinzufügen, können Sie die Dynamik deaktivieren. Aktivieren Sie die Dynamik wieder, nachdem Ihre Lösung die Shapes hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="9008d-p101">You can disable dynamics to increase your solution's performance. For example, if your solution adds placeable shapes to a drawing and you don't want the application to reroute connectors and reposition shapes each time you add a shape, you can disable dynamics. After your solution adds the shapes, re-enable dynamics.</span></span>
  
<span data-ttu-id="9008d-115">Wenn Sie einen Verweis auf die Zelle Zelle DynamicsOff aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9008d-115">To get a reference to the DynamicsOff cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9008d-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9008d-116">Cell name:</span></span>  <br/> | <span data-ttu-id="9008d-117">Zelle DynamicsOff</span><span class="sxs-lookup"><span data-stu-id="9008d-117">DynamicsOff</span></span>  <br/> |
   
<span data-ttu-id="9008d-118">Wenn Sie einen Verweis auf die Zelle Zelle DynamicsOff aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="9008d-118">To get a reference to the DynamicsOff cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9008d-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9008d-119">Section index:</span></span>  <br/> |<span data-ttu-id="9008d-120">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9008d-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9008d-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9008d-121">Row index:</span></span>  <br/> |<span data-ttu-id="9008d-122">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="9008d-122">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="9008d-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9008d-123">Cell index:</span></span>  <br/> |<span data-ttu-id="9008d-124">**visPLODynamicsOff**</span><span class="sxs-lookup"><span data-stu-id="9008d-124">**visPLODynamicsOff**</span></span> <br/> |
   

