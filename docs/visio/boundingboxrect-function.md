---
title: BOUNDINGBOXRECT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1f66d2b2-ec9e-cd58-7642-96850fe4589e
description: Gibt die Koordinate des angegebenen Rands des das Shape umgebenden Felds zurück.
ms.openlocfilehash: 0018118eb0991fe9dc1da0eb000566b69d8a4b4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418071"
---
# <a name="boundingboxrect-function"></a><span data-ttu-id="144d2-103">BOUNDINGBOXRECT Function</span><span class="sxs-lookup"><span data-stu-id="144d2-103">BOUNDINGBOXRECT Function</span></span>

<span data-ttu-id="144d2-104">Gibt die Koordinate des angegebenen Rands des das Shape umgebenden Felds zurück.</span><span class="sxs-lookup"><span data-stu-id="144d2-104">Returns the coordinate of the specified edge of the shape's bounding box.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="144d2-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="144d2-105">Version Information</span></span>

<span data-ttu-id="144d2-106">Hinzugefügte Version: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="144d2-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="144d2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="144d2-107">Syntax</span></span>

<span data-ttu-id="144d2-108">BOUNDINGBOXRECT(\*\* *Index* \*\* )</span><span class="sxs-lookup"><span data-stu-id="144d2-108">BOUNDINGBOXRECT(\*\* *Index* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="144d2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="144d2-109">Parameters</span></span>

|<span data-ttu-id="144d2-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="144d2-110">**Name**</span></span>|<span data-ttu-id="144d2-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="144d2-111">**Required/Optional**</span></span>|<span data-ttu-id="144d2-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="144d2-112">**Data Type**</span></span>|<span data-ttu-id="144d2-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="144d2-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="144d2-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="144d2-114">_Index_</span></span> <br/> |<span data-ttu-id="144d2-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="144d2-115">Required</span></span>  <br/> |<span data-ttu-id="144d2-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="144d2-116">**Integer**</span></span> <br/> |<span data-ttu-id="144d2-p101">Der Rand des das Shape umgebenden Felds, für den die Koordinate abgerufen werden soll. Mögliche Werte finden Sie in den Anmerkungen.</span><span class="sxs-lookup"><span data-stu-id="144d2-p101">The edge of the shape's bounding box for which to get the coordinate. See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="144d2-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="144d2-119">Return value</span></span>

 <span data-ttu-id="144d2-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="144d2-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="144d2-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="144d2-121">Remarks</span></span>

 <span data-ttu-id="144d2-122">*Index*  kann einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="144d2-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="144d2-123">**Aspekt**</span><span class="sxs-lookup"><span data-stu-id="144d2-123">**Item**</span></span>|<span data-ttu-id="144d2-124">**Wert**</span><span class="sxs-lookup"><span data-stu-id="144d2-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="144d2-125">Linker Rand</span><span class="sxs-lookup"><span data-stu-id="144d2-125">Left edge</span></span>  <br/> |<span data-ttu-id="144d2-126">0</span><span class="sxs-lookup"><span data-stu-id="144d2-126">0</span></span>  <br/> |
|<span data-ttu-id="144d2-127">Rechter Rand</span><span class="sxs-lookup"><span data-stu-id="144d2-127">Right edge</span></span>  <br/> |<span data-ttu-id="144d2-128">1</span><span class="sxs-lookup"><span data-stu-id="144d2-128">1</span></span>  <br/> |
|<span data-ttu-id="144d2-129">Oberer Rand</span><span class="sxs-lookup"><span data-stu-id="144d2-129">Top edge</span></span>  <br/> |<span data-ttu-id="144d2-130">2</span><span class="sxs-lookup"><span data-stu-id="144d2-130">2</span></span>  <br/> |
|<span data-ttu-id="144d2-131">Unterer Rand</span><span class="sxs-lookup"><span data-stu-id="144d2-131">Bottom edge</span></span>  <br/> |<span data-ttu-id="144d2-132">3</span><span class="sxs-lookup"><span data-stu-id="144d2-132">3</span></span>  <br/> |
   
<span data-ttu-id="144d2-133">Wenn das Shape über ein übergeordnetes Shape verfügt, befindet sich der Rückgabewert im Koordinatensystem dieses übergeordneten Shapes.</span><span class="sxs-lookup"><span data-stu-id="144d2-133">If the shape has a parent, the return value is in the coordinate system of that parent.</span></span>
  

