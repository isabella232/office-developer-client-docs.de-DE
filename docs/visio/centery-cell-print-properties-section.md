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
ms.openlocfilehash: 2fde1d6301d7b9de4540cd12f21e5af01d7a6239
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796643"
---
# <a name="centery-cell-print-properties-section"></a><span data-ttu-id="75adc-103">CenterY Cell (Print Properties Section)</span><span class="sxs-lookup"><span data-stu-id="75adc-103">CenterY Cell (Print Properties Section)</span></span>

<span data-ttu-id="75adc-104">Bestimmt, ob das Zeichenblatt vertikal zentriert auf der Druckseite ausgerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="75adc-104">Determines whether the drawing page is centered vertically on the printer page.</span></span> 
  
|<span data-ttu-id="75adc-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="75adc-105">**Value**</span></span>|<span data-ttu-id="75adc-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="75adc-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="75adc-107">WAHR</span><span class="sxs-lookup"><span data-stu-id="75adc-107">TRUE</span></span>  <br/> | <span data-ttu-id="75adc-108">Zeichenblatt wird vertikal zentriert auf der Druckseite ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="75adc-108">Center the drawing page vertically on the printer page.</span></span>  <br/> |
| <span data-ttu-id="75adc-109">FALSCH</span><span class="sxs-lookup"><span data-stu-id="75adc-109">FALSE</span></span>  <br/> | <span data-ttu-id="75adc-110">Zeichenblatt wird nicht vertikal zentriert auf der Druckseite ausgerichtet (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="75adc-110">Do not center the drawing page vertically on the printer page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75adc-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="75adc-111">Remarks</span></span>

<span data-ttu-id="75adc-p101">In der Standardeinstellung werden Zeichenblätter am oberen und linken Rand der Druckseite ausgerichtet. Durch das Festlegen der Zellen CenterX und CenterY auf WAHR wird das Zeichenblatt auf der Druckseite zentriert (bzw. auf den Druckseiten, wenn eine Unterteilung erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="75adc-p101">By default, drawing pages are justified to the top and left of the printer page. Setting the CenterX and CenterY cells to TRUE places the drawing page in the center of the printer page (or pages when tiling is necessary).</span></span> 
  
<span data-ttu-id="75adc-114">Wenn Sie einen Verweis auf die Zelle CenterY aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="75adc-114">To get a reference to the CenterY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="75adc-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="75adc-115">Cell name:</span></span>  <br/> | <span data-ttu-id="75adc-116">CenterY</span><span class="sxs-lookup"><span data-stu-id="75adc-116">CenterY</span></span>  <br/> |
   
<span data-ttu-id="75adc-117">Wenn Sie einen Verweis auf die Zelle CenterY aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="75adc-117">To get a reference to the CenterY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="75adc-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="75adc-118">Section index:</span></span>  <br/> |<span data-ttu-id="75adc-119">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="75adc-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="75adc-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="75adc-120">Row index:</span></span>  <br/> |<span data-ttu-id="75adc-121">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="75adc-121">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="75adc-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="75adc-122">Cell index:</span></span>  <br/> |<span data-ttu-id="75adc-123">**visPrintPropertiesCenterY**</span><span class="sxs-lookup"><span data-stu-id="75adc-123">**visPrintPropertiesCenterY**</span></span> <br/> |
   

