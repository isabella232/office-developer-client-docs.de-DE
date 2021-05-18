---
title: Zelle "XRulerDensity" (Abschnitt "Ruler &amp; Grid")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1165
localization_priority: Normal
ms.assetid: c11717c5-eb0e-e4fa-5a91-c62ecc048635
description: Legt die horizontalen Einteilungen auf dem Lineal des Zeichenblatts fest.
ms.openlocfilehash: f459e5d1d19580201f1404ac2d1ae53c824293f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411470"
---
# <a name="xrulerdensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="f6cf1-103">Zelle "XRulerDensity" (Abschnitt "Ruler &amp; Grid")</span><span class="sxs-lookup"><span data-stu-id="f6cf1-103">XRulerDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="f6cf1-104">Legt die horizontalen Einteilungen auf dem Lineal des Zeichenblatts fest.</span><span class="sxs-lookup"><span data-stu-id="f6cf1-104">Specifies the horizontal subdivisions on the ruler for the page.</span></span>
  
|<span data-ttu-id="f6cf1-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="f6cf1-105">**Value**</span></span>|<span data-ttu-id="f6cf1-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f6cf1-106">**Description**</span></span>|<span data-ttu-id="f6cf1-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="f6cf1-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f6cf1-108">0</span><span class="sxs-lookup"><span data-stu-id="f6cf1-108">0</span></span>  <br/> |<span data-ttu-id="f6cf1-109">Fest</span><span class="sxs-lookup"><span data-stu-id="f6cf1-109">Fixed</span></span>  <br/> |<span data-ttu-id="f6cf1-110">**visRulerFixed**</span><span class="sxs-lookup"><span data-stu-id="f6cf1-110">**visRulerFixed**</span></span> <br/> |
|<span data-ttu-id="f6cf1-111">8 ( &amp; H8)</span><span class="sxs-lookup"><span data-stu-id="f6cf1-111">8 (&amp;H8)</span></span>  <br/> |<span data-ttu-id="f6cf1-112">Vorschrr</span><span class="sxs-lookup"><span data-stu-id="f6cf1-112">Coarse</span></span>  <br/> |<span data-ttu-id="f6cf1-113">**visRulerCoarse**</span><span class="sxs-lookup"><span data-stu-id="f6cf1-113">**visRulerCoarse**</span></span> <br/> |
|<span data-ttu-id="f6cf1-114">16 ( &amp; H10)</span><span class="sxs-lookup"><span data-stu-id="f6cf1-114">16 (&amp;H10)</span></span>  <br/> |<span data-ttu-id="f6cf1-115">Normal (Standard)</span><span class="sxs-lookup"><span data-stu-id="f6cf1-115">Normal (Default)</span></span>  <br/> |<span data-ttu-id="f6cf1-116">**visRulerNormal**</span><span class="sxs-lookup"><span data-stu-id="f6cf1-116">**visRulerNormal**</span></span> <br/> |
|<span data-ttu-id="f6cf1-117">32 (&amp;H20)</span><span class="sxs-lookup"><span data-stu-id="f6cf1-117">32 (&amp;H20)</span></span>  <br/> |<span data-ttu-id="f6cf1-118">Fine</span><span class="sxs-lookup"><span data-stu-id="f6cf1-118">Fine</span></span>  <br/> |<span data-ttu-id="f6cf1-119">**visRulerFine**</span><span class="sxs-lookup"><span data-stu-id="f6cf1-119">**visRulerFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6cf1-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f6cf1-120">Remarks</span></span>

<span data-ttu-id="f6cf1-121">Diese Zelle entspricht der horizontalen **Unterteilungsoption** im Dialogfeld  Linealraster (klicken Sie auf der Registerkarte Ansicht auf den **Pfeil anzeigen).** **&amp;**</span><span class="sxs-lookup"><span data-stu-id="f6cf1-121">This cell corresponds to the horizontal **Subdivisions** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="f6cf1-122">Um einen Verweis auf die Zelle XRulerDensity anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="f6cf1-122">To get a reference to the XRulerDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f6cf1-123">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="f6cf1-123">Cell name:</span></span>  <br/> |<span data-ttu-id="f6cf1-124">XRulerDensity</span><span class="sxs-lookup"><span data-stu-id="f6cf1-124">XRulerDensity</span></span>  <br/> |
   
<span data-ttu-id="f6cf1-125">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die XRulerDensity-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="f6cf1-125">To get a reference to the XRulerDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f6cf1-126">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="f6cf1-126">Section index:</span></span>  <br/> |<span data-ttu-id="f6cf1-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f6cf1-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f6cf1-128">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="f6cf1-128">Row index:</span></span>  <br/> |<span data-ttu-id="f6cf1-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="f6cf1-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="f6cf1-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="f6cf1-130">Cell index:</span></span>  <br/> |<span data-ttu-id="f6cf1-131">**visXRulerDensity**</span><span class="sxs-lookup"><span data-stu-id="f6cf1-131">**visXRulerDensity**</span></span> <br/> |
   

