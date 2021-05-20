---
title: Zelle "CenterY" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033792
localization_priority: Normal
ms.assetid: 7ce0bf66-dc8b-9646-7b04-50c969ecd67a
description: Bestimmt, ob das Zeichenblatt vertikal zentriert auf der Druckseite ausgerichtet wird.
ms.openlocfilehash: 858bf41c74fdcbd82d271a379df7c5816a7796fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437434"
---
# <a name="centery-cell-print-properties-section"></a><span data-ttu-id="56d0c-103">Zelle "CenterY" (Abschnitt "Print Properties")</span><span class="sxs-lookup"><span data-stu-id="56d0c-103">CenterY Cell (Print Properties Section)</span></span>

<span data-ttu-id="56d0c-104">Bestimmt, ob das Zeichenblatt vertikal zentriert auf der Druckseite ausgerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="56d0c-104">Determines whether the drawing page is centered vertically on the printer page.</span></span> 
  
|<span data-ttu-id="56d0c-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="56d0c-105">**Value**</span></span>|<span data-ttu-id="56d0c-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="56d0c-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="56d0c-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="56d0c-107">TRUE</span></span>  <br/> | <span data-ttu-id="56d0c-108">Zeichenblatt wird vertikal zentriert auf der Druckseite ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="56d0c-108">Center the drawing page vertically on the printer page.</span></span>  <br/> |
| <span data-ttu-id="56d0c-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="56d0c-109">FALSE</span></span>  <br/> | <span data-ttu-id="56d0c-110">Zeichenblatt wird nicht vertikal zentriert auf der Druckseite ausgerichtet (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="56d0c-110">Do not center the drawing page vertically on the printer page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56d0c-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="56d0c-111">Remarks</span></span>

<span data-ttu-id="56d0c-p101">In der Standardeinstellung werden Zeichenblätter am oberen und linken Rand der Druckseite ausgerichtet. Durch das Festlegen der Zellen CenterX und CenterY auf WAHR wird das Zeichenblatt auf der Druckseite zentriert (bzw. auf den Druckseiten, wenn eine Unterteilung erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="56d0c-p101">By default, drawing pages are justified to the top and left of the printer page. Setting the CenterX and CenterY cells to TRUE places the drawing page in the center of the printer page (or pages when tiling is necessary).</span></span> 
  
<span data-ttu-id="56d0c-114">Um einen Verweis auf die Zelle CenterY anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="56d0c-114">To get a reference to the CenterY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="56d0c-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="56d0c-115">Cell name:</span></span>  <br/> | <span data-ttu-id="56d0c-116">CenterY</span><span class="sxs-lookup"><span data-stu-id="56d0c-116">CenterY</span></span>  <br/> |
   
<span data-ttu-id="56d0c-117">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle CenterY nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="56d0c-117">To get a reference to the CenterY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="56d0c-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="56d0c-118">Section index:</span></span>  <br/> |<span data-ttu-id="56d0c-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="56d0c-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="56d0c-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="56d0c-120">Row index:</span></span>  <br/> |<span data-ttu-id="56d0c-121">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="56d0c-121">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="56d0c-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="56d0c-122">Cell index:</span></span>  <br/> |<span data-ttu-id="56d0c-123">**visPrintPropertiesCenterY**</span><span class="sxs-lookup"><span data-stu-id="56d0c-123">**visPrintPropertiesCenterY**</span></span> <br/> |
   

