---
title: BOUNDINGBOXDIST-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: Gibt die Messung für den angegebenen Teil des das Shape umgebenden Felds zurück.
ms.openlocfilehash: 94cad37c4a0d2c6c7e7c69d997af09a9d7f1d651
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796556"
---
# <a name="boundingboxdist-function"></a><span data-ttu-id="35cbb-103">BOUNDINGBOXDIST Function</span><span class="sxs-lookup"><span data-stu-id="35cbb-103">BOUNDINGBOXDIST Function</span></span>

<span data-ttu-id="35cbb-104">Gibt die Messung für den angegebenen Teil des das Shape umgebenden Felds zurück.</span><span class="sxs-lookup"><span data-stu-id="35cbb-104">Returns the measurement of the specified part of the shape's bounding box.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="35cbb-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="35cbb-105">Version Information</span></span>

<span data-ttu-id="35cbb-106">Hinzugefügte Version: Visio 2010</span><span class="sxs-lookup"><span data-stu-id="35cbb-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="35cbb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="35cbb-107">Syntax</span></span>

<span data-ttu-id="35cbb-108">BOUNDINGBOXDIST (** *Index* **)</span><span class="sxs-lookup"><span data-stu-id="35cbb-108">BOUNDINGBOXDIST(** *Index* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="35cbb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="35cbb-109">Parameters</span></span>

|<span data-ttu-id="35cbb-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="35cbb-110">**Name**</span></span>|<span data-ttu-id="35cbb-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="35cbb-111">**Required/Optional**</span></span>|<span data-ttu-id="35cbb-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="35cbb-112">**Data Type**</span></span>|<span data-ttu-id="35cbb-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="35cbb-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="35cbb-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="35cbb-114">_Index_</span></span> <br/> |<span data-ttu-id="35cbb-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="35cbb-115">Required</span></span>  <br/> |<span data-ttu-id="35cbb-116">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="35cbb-116">**Number**</span></span> <br/> |<span data-ttu-id="35cbb-117">Der Teil des das Shape umgebenden Felds um messen und zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="35cbb-117">The part of the shape's bounding box to measure and return.</span></span> <span data-ttu-id="35cbb-118">Mögliche Werte finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="35cbb-118">See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="35cbb-119">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="35cbb-119">Return value</span></span>

 <span data-ttu-id="35cbb-120">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="35cbb-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="35cbb-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35cbb-121">Remarks</span></span>

 <span data-ttu-id="35cbb-122">*Index* kann eine der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="35cbb-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="35cbb-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="35cbb-123">**Item**</span></span>|<span data-ttu-id="35cbb-124">**Wert**</span><span class="sxs-lookup"><span data-stu-id="35cbb-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="35cbb-125">Breite</span><span class="sxs-lookup"><span data-stu-id="35cbb-125">Width</span></span>  <br/> |<span data-ttu-id="35cbb-126">0</span><span class="sxs-lookup"><span data-stu-id="35cbb-126">0</span></span>  <br/> |
|<span data-ttu-id="35cbb-127">Höhe</span><span class="sxs-lookup"><span data-stu-id="35cbb-127">Height</span></span>  <br/> |<span data-ttu-id="35cbb-128">1</span><span class="sxs-lookup"><span data-stu-id="35cbb-128">1</span></span>  <br/> |
|<span data-ttu-id="35cbb-129">Shape-Pin bis linke Kante</span><span class="sxs-lookup"><span data-stu-id="35cbb-129">Left edge to shape pin</span></span>  <br/> |<span data-ttu-id="35cbb-130">2</span><span class="sxs-lookup"><span data-stu-id="35cbb-130">2</span></span>  <br/> |
|<span data-ttu-id="35cbb-131">Shape-Pin bis rechte Kante</span><span class="sxs-lookup"><span data-stu-id="35cbb-131">Shape pin to right edge</span></span>  <br/> |<span data-ttu-id="35cbb-132">3</span><span class="sxs-lookup"><span data-stu-id="35cbb-132">3</span></span>  <br/> |
|<span data-ttu-id="35cbb-133">Shape-Pin bis obere Kante</span><span class="sxs-lookup"><span data-stu-id="35cbb-133">Shape pin to top edge</span></span>  <br/> |<span data-ttu-id="35cbb-134">4</span><span class="sxs-lookup"><span data-stu-id="35cbb-134">4</span></span>  <br/> |
|<span data-ttu-id="35cbb-135">Shape-Pin bis untere Kante</span><span class="sxs-lookup"><span data-stu-id="35cbb-135">Bottom edge to shape pin</span></span>  <br/> |<span data-ttu-id="35cbb-136">5</span><span class="sxs-lookup"><span data-stu-id="35cbb-136">5</span></span>  <br/> |
|<span data-ttu-id="35cbb-137">Mitte des umgebenden Felds bis PinX</span><span class="sxs-lookup"><span data-stu-id="35cbb-137">Center of bounding box to PinX</span></span>  <br/> |<span data-ttu-id="35cbb-138">6</span><span class="sxs-lookup"><span data-stu-id="35cbb-138">6</span></span>  <br/> |
|<span data-ttu-id="35cbb-139">Mitte des umgebenden Felds bis PinY</span><span class="sxs-lookup"><span data-stu-id="35cbb-139">Center of bounding box to PinY</span></span>  <br/> |<span data-ttu-id="35cbb-140">7</span><span class="sxs-lookup"><span data-stu-id="35cbb-140">7</span></span>  <br/> |
   

