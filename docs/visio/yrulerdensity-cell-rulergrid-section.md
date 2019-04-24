---
title: Zelle YRulerDensity Cell (Ruler &amp; Grid section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1215
localization_priority: Normal
ms.assetid: aebcd321-9d1c-e04e-7c85-3ec1ed851561
description: Legt die vertikalen Einteilungen auf dem Lineal des Zeichenblatts fest.
ms.openlocfilehash: c92c48f6c86fc794cf6f53a87fdb99e67a73b9f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357204"
---
# <a name="yrulerdensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="fc91e-103">Zelle YRulerDensity Cell (Ruler &amp; Grid section)</span><span class="sxs-lookup"><span data-stu-id="fc91e-103">YRulerDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="fc91e-104">Legt die vertikalen Einteilungen auf dem Lineal des Zeichenblatts fest.</span><span class="sxs-lookup"><span data-stu-id="fc91e-104">Specifies the vertical subdivisions on the ruler for the page.</span></span>
  
|<span data-ttu-id="fc91e-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="fc91e-105">**Value**</span></span>|<span data-ttu-id="fc91e-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fc91e-106">**Description**</span></span>|<span data-ttu-id="fc91e-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="fc91e-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fc91e-108">0</span><span class="sxs-lookup"><span data-stu-id="fc91e-108">0</span></span>  <br/> |<span data-ttu-id="fc91e-109">Fest</span><span class="sxs-lookup"><span data-stu-id="fc91e-109">Fixed</span></span>  <br/> |<span data-ttu-id="fc91e-110">**visRulerFixed**</span><span class="sxs-lookup"><span data-stu-id="fc91e-110">**visRulerFixed**</span></span> <br/> |
|<span data-ttu-id="fc91e-111">8 (&amp;H8)</span><span class="sxs-lookup"><span data-stu-id="fc91e-111">8 (&amp;H8)</span></span>  <br/> |<span data-ttu-id="fc91e-112">Grob</span><span class="sxs-lookup"><span data-stu-id="fc91e-112">Coarse</span></span>  <br/> |<span data-ttu-id="fc91e-113">**visRulerCoarse**</span><span class="sxs-lookup"><span data-stu-id="fc91e-113">**visRulerCoarse**</span></span> <br/> |
|<span data-ttu-id="fc91e-114">16 (&amp;H10)</span><span class="sxs-lookup"><span data-stu-id="fc91e-114">16 (&amp;H10)</span></span>  <br/> |<span data-ttu-id="fc91e-115">Normal (Standard)</span><span class="sxs-lookup"><span data-stu-id="fc91e-115">Normal (Default)</span></span>  <br/> |<span data-ttu-id="fc91e-116">**visRulerNormal**</span><span class="sxs-lookup"><span data-stu-id="fc91e-116">**visRulerNormal**</span></span> <br/> |
|<span data-ttu-id="fc91e-117">32 (&amp;H20)</span><span class="sxs-lookup"><span data-stu-id="fc91e-117">32 (&amp;H20)</span></span>  <br/> |<span data-ttu-id="fc91e-118">Abgestimmter</span><span class="sxs-lookup"><span data-stu-id="fc91e-118">Fine</span></span>  <br/> |<span data-ttu-id="fc91e-119">**visRulerFine**</span><span class="sxs-lookup"><span data-stu-id="fc91e-119">**visRulerFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc91e-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc91e-120">Remarks</span></span>

<span data-ttu-id="fc91e-121">Diese Zelle entspricht der Option vertikale unter **Einheiten** im Dialogfeld \*\*\*\* **Lineal &amp; -Raster** (Klicken Sie auf der Registerkarte **Ansicht** auf den Pfeil).</span><span class="sxs-lookup"><span data-stu-id="fc91e-121">This cell corresponds to the vertical **Subdivisions** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="fc91e-122">Wenn Sie einen Verweis auf die Zelle Zelle YRulerDensity aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="fc91e-122">To get a reference to the YRulerDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fc91e-123">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="fc91e-123">Cell name:</span></span>  <br/> |<span data-ttu-id="fc91e-124">Zelle YRulerDensity</span><span class="sxs-lookup"><span data-stu-id="fc91e-124">YRulerDensity</span></span>  <br/> |
   
<span data-ttu-id="fc91e-125">Wenn Sie einen Verweis auf die Zelle Zelle YRulerDensity aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="fc91e-125">To get a reference to the YRulerDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fc91e-126">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="fc91e-126">Section index:</span></span>  <br/> |<span data-ttu-id="fc91e-127">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fc91e-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="fc91e-128">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="fc91e-128">Row index:</span></span>  <br/> |<span data-ttu-id="fc91e-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="fc91e-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="fc91e-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="fc91e-130">Cell index:</span></span>  <br/> |<span data-ttu-id="fc91e-131">**visYRulerDensity**</span><span class="sxs-lookup"><span data-stu-id="fc91e-131">**visYRulerDensity**</span></span> <br/> |
   

