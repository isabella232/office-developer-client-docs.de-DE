---
title: YRulerDensity Cell (Ruler &amp; Grid Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1215
localization_priority: Normal
ms.assetid: aebcd321-9d1c-e04e-7c85-3ec1ed851561
description: Legt die vertikalen Einteilungen auf dem Lineal des Zeichenblatts fest.
ms.openlocfilehash: 4b5dcba7a5cb1a588f742b1c2ea6b430cb2af12c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798468"
---
# <a name="yrulerdensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="87d65-103">YRulerDensity Cell (Ruler &amp; Grid Section)</span><span class="sxs-lookup"><span data-stu-id="87d65-103">YRulerDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="87d65-104">Legt die vertikalen Einteilungen auf dem Lineal des Zeichenblatts fest.</span><span class="sxs-lookup"><span data-stu-id="87d65-104">Specifies the vertical subdivisions on the ruler for the page.</span></span>
  
|<span data-ttu-id="87d65-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="87d65-105">**Value**</span></span>|<span data-ttu-id="87d65-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="87d65-106">**Description**</span></span>|<span data-ttu-id="87d65-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="87d65-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="87d65-108">0</span><span class="sxs-lookup"><span data-stu-id="87d65-108">0</span></span>  <br/> |<span data-ttu-id="87d65-109">Fest</span><span class="sxs-lookup"><span data-stu-id="87d65-109">Fixed</span></span>  <br/> |<span data-ttu-id="87d65-110">**visRulerFixed**</span><span class="sxs-lookup"><span data-stu-id="87d65-110">**visRulerFixed**</span></span> <br/> |
|<span data-ttu-id="87d65-111">8 (&amp;H8)</span><span class="sxs-lookup"><span data-stu-id="87d65-111">8 (&amp;H8)</span></span>  <br/> |<span data-ttu-id="87d65-112">Grob</span><span class="sxs-lookup"><span data-stu-id="87d65-112">Coarse</span></span>  <br/> |<span data-ttu-id="87d65-113">**visRulerCoarse**</span><span class="sxs-lookup"><span data-stu-id="87d65-113">**visRulerCoarse**</span></span> <br/> |
|<span data-ttu-id="87d65-114">16 (&amp;H10)</span><span class="sxs-lookup"><span data-stu-id="87d65-114">16 (&amp;H10)</span></span>  <br/> |<span data-ttu-id="87d65-115">Normal (Standard)</span><span class="sxs-lookup"><span data-stu-id="87d65-115">Normal (Default)</span></span>  <br/> |<span data-ttu-id="87d65-116">**visRulerNormal**</span><span class="sxs-lookup"><span data-stu-id="87d65-116">**visRulerNormal**</span></span> <br/> |
|<span data-ttu-id="87d65-117">32 (&amp;H20)</span><span class="sxs-lookup"><span data-stu-id="87d65-117">32 (&amp;H20)</span></span>  <br/> |<span data-ttu-id="87d65-118">Fein</span><span class="sxs-lookup"><span data-stu-id="87d65-118">Fine</span></span>  <br/> |<span data-ttu-id="87d65-119">**visRulerFine**</span><span class="sxs-lookup"><span data-stu-id="87d65-119">**visRulerFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87d65-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87d65-120">Remarks</span></span>

<span data-ttu-id="87d65-121">Diese Zelle entspricht der vertikalen Option **Einteilung** in die **Lineal &amp; Raster** im Dialogfeld (klicken Sie auf der Registerkarte **Ansicht** auf den Pfeil neben **Anzeigen** ).</span><span class="sxs-lookup"><span data-stu-id="87d65-121">This cell corresponds to the vertical **Subdivisions** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="87d65-122">Wenn Sie einen Verweis auf die Zelle YRulerDensity aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="87d65-122">To get a reference to the YRulerDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87d65-123">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="87d65-123">Cell name:</span></span>  <br/> |<span data-ttu-id="87d65-124">YRulerDensity</span><span class="sxs-lookup"><span data-stu-id="87d65-124">YRulerDensity</span></span>  <br/> |
   
<span data-ttu-id="87d65-125">Wenn Sie einen Verweis auf die Zelle YRulerDensity aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="87d65-125">To get a reference to the YRulerDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87d65-126">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="87d65-126">Section index:</span></span>  <br/> |<span data-ttu-id="87d65-127">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="87d65-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="87d65-128">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="87d65-128">Row index:</span></span>  <br/> |<span data-ttu-id="87d65-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="87d65-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="87d65-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="87d65-130">Cell index:</span></span>  <br/> |<span data-ttu-id="87d65-131">**visYRulerDensity**</span><span class="sxs-lookup"><span data-stu-id="87d65-131">**visYRulerDensity**</span></span> <br/> |
   

