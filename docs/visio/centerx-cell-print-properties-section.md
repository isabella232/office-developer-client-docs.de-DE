---
title: Zelle "CenterX" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60030
localization_priority: Normal
ms.assetid: 890e2537-66a5-2863-c78d-320b42565ea7
description: Bestimmt, ob das Zeichenblatt horizontal zentriert auf der Druckseite ausgerichtet wird.
ms.openlocfilehash: 13b05ed71248a3f8fada947fca6b203c6ab19c6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418078"
---
# <a name="centerx-cell-print-properties-section"></a><span data-ttu-id="d3ee6-103">Zelle "CenterX" (Abschnitt "Print Properties")</span><span class="sxs-lookup"><span data-stu-id="d3ee6-103">CenterX Cell (Print Properties Section)</span></span>

<span data-ttu-id="d3ee6-104">Bestimmt, ob das Zeichenblatt horizontal zentriert auf der Druckseite ausgerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="d3ee6-104">Determines whether the drawing page is centered horizontally on the printer page.</span></span> 
  
|<span data-ttu-id="d3ee6-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d3ee6-105">**Value**</span></span>|<span data-ttu-id="d3ee6-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d3ee6-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d3ee6-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d3ee6-107">TRUE</span></span>  <br/> | <span data-ttu-id="d3ee6-108">Zeichenblatt wird horizontal zentriert auf der Druckseite ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="d3ee6-108">Center the drawing page horizontally on the printer page.</span></span>  <br/> |
| <span data-ttu-id="d3ee6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d3ee6-109">FALSE</span></span>  <br/> | <span data-ttu-id="d3ee6-110">Zeichenblatt wird nicht horizontal zentriert auf der Druckseite ausgerichtet (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="d3ee6-110">Do not center the drawing page horizontally on the printer page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3ee6-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d3ee6-111">Remarks</span></span>

<span data-ttu-id="d3ee6-p101">In der Standardeinstellung werden Zeichenblätter am oberen und linken Rand der Druckseite ausgerichtet. Durch das Festlegen der Zellen CenterX und CenterY auf WAHR wird das Zeichenblatt auf der Druckseite zentriert (bzw. auf den Druckseiten, wenn eine Unterteilung erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="d3ee6-p101">By default, drawing pages are justified to the top and left of the printer page. Setting the CenterX and CenterY cells to TRUE places the drawing page in the center of the printer page (or pages when tiling is necessary).</span></span> 
  
<span data-ttu-id="d3ee6-114">Um einen Verweis auf die Zelle CenterX anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="d3ee6-114">To get a reference to the CenterX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d3ee6-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="d3ee6-115">Cell name:</span></span>  <br/> | <span data-ttu-id="d3ee6-116">CenterX</span><span class="sxs-lookup"><span data-stu-id="d3ee6-116">CenterX</span></span>  <br/> |
   
<span data-ttu-id="d3ee6-117">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die CenterX-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="d3ee6-117">To get a reference to the CenterX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d3ee6-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="d3ee6-118">Section index:</span></span>  <br/> |<span data-ttu-id="d3ee6-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d3ee6-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d3ee6-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d3ee6-120">Row index:</span></span>  <br/> |<span data-ttu-id="d3ee6-121">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="d3ee6-121">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="d3ee6-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d3ee6-122">Cell index:</span></span>  <br/> |<span data-ttu-id="d3ee6-123">**visPrintPropertiesCenterX**</span><span class="sxs-lookup"><span data-stu-id="d3ee6-123">**visPrintPropertiesCenterX**</span></span> <br/> |
   

