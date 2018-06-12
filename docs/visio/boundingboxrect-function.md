---
title: BOUNDINGBOXRECT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1f66d2b2-ec9e-cd58-7642-96850fe4589e
description: Gibt die Koordinate des angegebenen Rands des das Shape umgebenden Felds zurück.
ms.openlocfilehash: 2c850cb213ec0093ead53cd860f92e38da46f27e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796551"
---
# <a name="boundingboxrect-function"></a><span data-ttu-id="6ca67-103">BOUNDINGBOXRECT Function</span><span class="sxs-lookup"><span data-stu-id="6ca67-103">BOUNDINGBOXRECT Function</span></span>

<span data-ttu-id="6ca67-104">Gibt die Koordinate des angegebenen Rands des das Shape umgebenden Felds zurück.</span><span class="sxs-lookup"><span data-stu-id="6ca67-104">Returns the coordinate of the specified edge of the shape's bounding box.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="6ca67-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="6ca67-105">Version Information</span></span>

<span data-ttu-id="6ca67-106">Hinzugefügte Version: Visio 2010</span><span class="sxs-lookup"><span data-stu-id="6ca67-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6ca67-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ca67-107">Syntax</span></span>

<span data-ttu-id="6ca67-108">BOUNDINGBOXRECT (** *Index* **)</span><span class="sxs-lookup"><span data-stu-id="6ca67-108">BOUNDINGBOXRECT(** *Index* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6ca67-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ca67-109">Parameters</span></span>

|<span data-ttu-id="6ca67-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="6ca67-110">**Name**</span></span>|<span data-ttu-id="6ca67-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="6ca67-111">**Required/Optional**</span></span>|<span data-ttu-id="6ca67-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="6ca67-112">**Data Type**</span></span>|<span data-ttu-id="6ca67-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6ca67-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6ca67-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="6ca67-114">_Index_</span></span> <br/> |<span data-ttu-id="6ca67-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="6ca67-115">Required</span></span>  <br/> |<span data-ttu-id="6ca67-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="6ca67-116">**Integer**</span></span> <br/> |<span data-ttu-id="6ca67-p101">Der Rand des das Shape umgebenden Felds, für den die Koordinate abgerufen werden soll. Mögliche Werte finden Sie in den Anmerkungen.</span><span class="sxs-lookup"><span data-stu-id="6ca67-p101">The edge of the shape's bounding box for which to get the coordinate. See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="6ca67-119">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="6ca67-119">Return value</span></span>

 <span data-ttu-id="6ca67-120">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="6ca67-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6ca67-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ca67-121">Remarks</span></span>

 <span data-ttu-id="6ca67-122">*Index* kann eine der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="6ca67-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="6ca67-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="6ca67-123">**Item**</span></span>|<span data-ttu-id="6ca67-124">**Wert**</span><span class="sxs-lookup"><span data-stu-id="6ca67-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6ca67-125">Linker Rand</span><span class="sxs-lookup"><span data-stu-id="6ca67-125">Left edge</span></span>  <br/> |<span data-ttu-id="6ca67-126">0</span><span class="sxs-lookup"><span data-stu-id="6ca67-126">0</span></span>  <br/> |
|<span data-ttu-id="6ca67-127">Rechter Rand</span><span class="sxs-lookup"><span data-stu-id="6ca67-127">Right edge</span></span>  <br/> |<span data-ttu-id="6ca67-128">1</span><span class="sxs-lookup"><span data-stu-id="6ca67-128">1</span></span>  <br/> |
|<span data-ttu-id="6ca67-129">Oberer Rand</span><span class="sxs-lookup"><span data-stu-id="6ca67-129">Top edge</span></span>  <br/> |<span data-ttu-id="6ca67-130">2</span><span class="sxs-lookup"><span data-stu-id="6ca67-130">2</span></span>  <br/> |
|<span data-ttu-id="6ca67-131">Unterer Rand</span><span class="sxs-lookup"><span data-stu-id="6ca67-131">Bottom edge</span></span>  <br/> |<span data-ttu-id="6ca67-132">3</span><span class="sxs-lookup"><span data-stu-id="6ca67-132">3</span></span>  <br/> |
   
<span data-ttu-id="6ca67-133">Wenn die Form ein übergeordnetes Objekt ist, ist der Rückgabewert im Koordinatensystem des übergeordneten.</span><span class="sxs-lookup"><span data-stu-id="6ca67-133">If the shape has a parent, the return value is in the coordinate system of that parent.</span></span>
  

