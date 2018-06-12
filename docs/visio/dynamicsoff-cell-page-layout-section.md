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
ms.openlocfilehash: 72d65860d1a2ee37efd5287ae3f4baf54bd3addb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796911"
---
# <a name="dynamicsoff-cell-page-layout-section"></a><span data-ttu-id="b37d3-103">DynamicsOff Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="b37d3-103">DynamicsOff Cell (Page Layout Section)</span></span>

<span data-ttu-id="b37d3-104">Legt fest, ob platzierbare Shapes verschoben und ob Verbinder um andere Shapes und Verbinder auf dem Zeichenblatt herum umgeleitet werden können.</span><span class="sxs-lookup"><span data-stu-id="b37d3-104">Determines whether placeable shapes move and connectors reroute around other shapes and connectors on the drawing page.</span></span>
  
|<span data-ttu-id="b37d3-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b37d3-105">**Value**</span></span>|<span data-ttu-id="b37d3-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b37d3-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b37d3-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b37d3-107">TRUE</span></span>  <br/> | <span data-ttu-id="b37d3-108">Dynamik deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="b37d3-108">Disable dynamics.</span></span>  <br/> |
| <span data-ttu-id="b37d3-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b37d3-109">FALSE</span></span>  <br/> | <span data-ttu-id="b37d3-110">Dynamik aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b37d3-110">Enable dynamics.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b37d3-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b37d3-111">Remarks</span></span>

<span data-ttu-id="b37d3-p101">Sie können die Dynamik deaktivieren, um die Leistung Ihrer Lösung zu steigern. Wenn Ihre Lösung beispielsweise Shape-Platzierungen in eine Zeichnung einfügt, Sie aber nicht möchten, dass die Anwendung Verbinder umleitet und Shapes neu platziert, sobald Sie ein Shape hinzufügen, können Sie die Dynamik deaktivieren. Aktivieren Sie die Dynamik wieder, nachdem Ihre Lösung die Shapes hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="b37d3-p101">You can disable dynamics to increase your solution's performance. For example, if your solution adds placeable shapes to a drawing and you don't want the application to reroute connectors and reposition shapes each time you add a shape, you can disable dynamics. After your solution adds the shapes, re-enable dynamics.</span></span>
  
<span data-ttu-id="b37d3-115">Wenn Sie einen Verweis auf die Zelle DynamicsOff nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b37d3-115">To get a reference to the DynamicsOff cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b37d3-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b37d3-116">Cell name:</span></span>  <br/> | <span data-ttu-id="b37d3-117">DynamicsOff</span><span class="sxs-lookup"><span data-stu-id="b37d3-117">DynamicsOff</span></span>  <br/> |
   
<span data-ttu-id="b37d3-118">Wenn Sie einen Verweis auf die Zelle DynamicsOff aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="b37d3-118">To get a reference to the DynamicsOff cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b37d3-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b37d3-119">Section index:</span></span>  <br/> |<span data-ttu-id="b37d3-120">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b37d3-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b37d3-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b37d3-121">Row index:</span></span>  <br/> |<span data-ttu-id="b37d3-122">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="b37d3-122">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="b37d3-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b37d3-123">Cell index:</span></span>  <br/> |<span data-ttu-id="b37d3-124">**visPLODynamicsOff**</span><span class="sxs-lookup"><span data-stu-id="b37d3-124">**visPLODynamicsOff**</span></span> <br/> |
   

