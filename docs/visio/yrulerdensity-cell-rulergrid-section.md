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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406801"
---
# <a name="yrulerdensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="24b58-103">Zelle YRulerDensity Cell (Ruler &amp; Grid section)</span><span class="sxs-lookup"><span data-stu-id="24b58-103">YRulerDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="24b58-104">Legt die vertikalen Einteilungen auf dem Lineal des Zeichenblatts fest.</span><span class="sxs-lookup"><span data-stu-id="24b58-104">Specifies the vertical subdivisions on the ruler for the page.</span></span>
  
|<span data-ttu-id="24b58-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="24b58-105">**Value**</span></span>|<span data-ttu-id="24b58-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="24b58-106">**Description**</span></span>|<span data-ttu-id="24b58-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="24b58-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="24b58-108">0</span><span class="sxs-lookup"><span data-stu-id="24b58-108">0</span></span>  <br/> |<span data-ttu-id="24b58-109">Fest</span><span class="sxs-lookup"><span data-stu-id="24b58-109">Fixed</span></span>  <br/> |<span data-ttu-id="24b58-110">**visRulerFixed**</span><span class="sxs-lookup"><span data-stu-id="24b58-110">**visRulerFixed**</span></span> <br/> |
|<span data-ttu-id="24b58-111">8 (&amp;H8)</span><span class="sxs-lookup"><span data-stu-id="24b58-111">8 (&amp;H8)</span></span>  <br/> |<span data-ttu-id="24b58-112">Grob</span><span class="sxs-lookup"><span data-stu-id="24b58-112">Coarse</span></span>  <br/> |<span data-ttu-id="24b58-113">**visRulerCoarse**</span><span class="sxs-lookup"><span data-stu-id="24b58-113">**visRulerCoarse**</span></span> <br/> |
|<span data-ttu-id="24b58-114">16 (&amp;H10)</span><span class="sxs-lookup"><span data-stu-id="24b58-114">16 (&amp;H10)</span></span>  <br/> |<span data-ttu-id="24b58-115">Normal (Standard)</span><span class="sxs-lookup"><span data-stu-id="24b58-115">Normal (Default)</span></span>  <br/> |<span data-ttu-id="24b58-116">**visRulerNormal**</span><span class="sxs-lookup"><span data-stu-id="24b58-116">**visRulerNormal**</span></span> <br/> |
|<span data-ttu-id="24b58-117">32 (&amp;H20)</span><span class="sxs-lookup"><span data-stu-id="24b58-117">32 (&amp;H20)</span></span>  <br/> |<span data-ttu-id="24b58-118">Abgestimmter</span><span class="sxs-lookup"><span data-stu-id="24b58-118">Fine</span></span>  <br/> |<span data-ttu-id="24b58-119">**visRulerFine**</span><span class="sxs-lookup"><span data-stu-id="24b58-119">**visRulerFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24b58-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24b58-120">Remarks</span></span>

<span data-ttu-id="24b58-121">Diese Zelle entspricht der Option vertikale unter **Einheiten** im Dialogfeld \*\*\*\* **Lineal &amp; -Raster** (Klicken Sie auf der Registerkarte **Ansicht** auf den Pfeil).</span><span class="sxs-lookup"><span data-stu-id="24b58-121">This cell corresponds to the vertical **Subdivisions** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="24b58-122">Wenn Sie einen Verweis auf die Zelle Zelle YRulerDensity aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="24b58-122">To get a reference to the YRulerDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="24b58-123">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="24b58-123">Cell name:</span></span>  <br/> |<span data-ttu-id="24b58-124">Zelle YRulerDensity</span><span class="sxs-lookup"><span data-stu-id="24b58-124">YRulerDensity</span></span>  <br/> |
   
<span data-ttu-id="24b58-125">Wenn Sie einen Verweis auf die Zelle Zelle YRulerDensity aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="24b58-125">To get a reference to the YRulerDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="24b58-126">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="24b58-126">Section index:</span></span>  <br/> |<span data-ttu-id="24b58-127">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="24b58-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="24b58-128">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="24b58-128">Row index:</span></span>  <br/> |<span data-ttu-id="24b58-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="24b58-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="24b58-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="24b58-130">Cell index:</span></span>  <br/> |<span data-ttu-id="24b58-131">**visYRulerDensity**</span><span class="sxs-lookup"><span data-stu-id="24b58-131">**visYRulerDensity**</span></span> <br/> |
   

