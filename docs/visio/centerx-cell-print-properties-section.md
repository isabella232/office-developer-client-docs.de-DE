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
ms.openlocfilehash: a12b60f7d183a27d938bd18a1f571ef01af455d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796624"
---
# <a name="centerx-cell-print-properties-section"></a><span data-ttu-id="f0bdd-103">CenterX Cell (Print Properties Section)</span><span class="sxs-lookup"><span data-stu-id="f0bdd-103">CenterX Cell (Print Properties Section)</span></span>

<span data-ttu-id="f0bdd-104">Bestimmt, ob das Zeichenblatt horizontal zentriert auf der Druckseite ausgerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="f0bdd-104">Determines whether the drawing page is centered horizontally on the printer page.</span></span> 
  
|<span data-ttu-id="f0bdd-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="f0bdd-105">**Value**</span></span>|<span data-ttu-id="f0bdd-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f0bdd-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f0bdd-107">WAHR</span><span class="sxs-lookup"><span data-stu-id="f0bdd-107">TRUE</span></span>  <br/> | <span data-ttu-id="f0bdd-108">Zeichenblatt wird horizontal zentriert auf der Druckseite ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="f0bdd-108">Center the drawing page horizontally on the printer page.</span></span>  <br/> |
| <span data-ttu-id="f0bdd-109">FALSCH</span><span class="sxs-lookup"><span data-stu-id="f0bdd-109">FALSE</span></span>  <br/> | <span data-ttu-id="f0bdd-110">Zeichenblatt wird nicht horizontal zentriert auf der Druckseite ausgerichtet (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="f0bdd-110">Do not center the drawing page horizontally on the printer page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0bdd-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f0bdd-111">Remarks</span></span>

<span data-ttu-id="f0bdd-p101">In der Standardeinstellung werden Zeichenblätter am oberen und linken Rand der Druckseite ausgerichtet. Durch das Festlegen der Zellen CenterX und CenterY auf WAHR wird das Zeichenblatt auf der Druckseite zentriert (bzw. auf den Druckseiten, wenn eine Unterteilung erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="f0bdd-p101">By default, drawing pages are justified to the top and left of the printer page. Setting the CenterX and CenterY cells to TRUE places the drawing page in the center of the printer page (or pages when tiling is necessary).</span></span> 
  
<span data-ttu-id="f0bdd-114">Wenn Sie einen Verweis auf die Zelle CenterX aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f0bdd-114">To get a reference to the CenterX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f0bdd-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="f0bdd-115">Cell name:</span></span>  <br/> | <span data-ttu-id="f0bdd-116">CenterX</span><span class="sxs-lookup"><span data-stu-id="f0bdd-116">CenterX</span></span>  <br/> |
   
<span data-ttu-id="f0bdd-117">Wenn Sie einen Verweis auf die Zelle CenterX aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="f0bdd-117">To get a reference to the CenterX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f0bdd-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="f0bdd-118">Section index:</span></span>  <br/> |<span data-ttu-id="f0bdd-119">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f0bdd-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f0bdd-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="f0bdd-120">Row index:</span></span>  <br/> |<span data-ttu-id="f0bdd-121">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="f0bdd-121">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="f0bdd-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="f0bdd-122">Cell index:</span></span>  <br/> |<span data-ttu-id="f0bdd-123">**visPrintPropertiesCenterX**</span><span class="sxs-lookup"><span data-stu-id="f0bdd-123">**visPrintPropertiesCenterX**</span></span> <br/> |
   

