---
title: ANGLEALONGPATH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Gibt den Winkel der Tangenten zum Pfad an einem gegebenen Punkt zurück.
ms.openlocfilehash: 0d38fc0e123a7e38b7826b55415cfc09c1789c0e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407326"
---
# <a name="anglealongpath-function"></a><span data-ttu-id="78a87-103">ANGLEALONGPATH Function</span><span class="sxs-lookup"><span data-stu-id="78a87-103">ANGLEALONGPATH Function</span></span>

<span data-ttu-id="78a87-104">Gibt den Winkel der Tangenten zum Pfad an einem gegebenen Punkt zurück.</span><span class="sxs-lookup"><span data-stu-id="78a87-104">Returns the angle of the tangent to the path at a given point.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="78a87-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="78a87-105">Version Information</span></span>

<span data-ttu-id="78a87-106">Hinzugefügte Version: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="78a87-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="78a87-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="78a87-107">Syntax</span></span>

<span data-ttu-id="78a87-108">ANGLEALONGPATH (\* \* *section* \* \*, \* \* *Reise* \* \* \* \* *[, Segment]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="78a87-108">ANGLEALONGPATH(\*\* *section* \*\*, \*\* *travel* \*\* \*\* *[,segment]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="78a87-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="78a87-109">Parameters</span></span>

|<span data-ttu-id="78a87-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="78a87-110">**Name**</span></span>|<span data-ttu-id="78a87-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="78a87-111">**Required/Optional**</span></span>|<span data-ttu-id="78a87-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="78a87-112">**Data Type**</span></span>|<span data-ttu-id="78a87-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="78a87-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="78a87-114">_section_</span><span class="sxs-lookup"><span data-stu-id="78a87-114">_section_</span></span> <br/> |<span data-ttu-id="78a87-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="78a87-115">Required</span></span>  <br/> |<span data-ttu-id="78a87-116">**String**</span><span class="sxs-lookup"><span data-stu-id="78a87-116">**String**</span></span> <br/> |<span data-ttu-id="78a87-117">Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).</span><span class="sxs-lookup"><span data-stu-id="78a87-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="78a87-118">_Reise_</span><span class="sxs-lookup"><span data-stu-id="78a87-118">_travel_</span></span> <br/> |<span data-ttu-id="78a87-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="78a87-119">Required</span></span>  <br/> |<span data-ttu-id="78a87-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="78a87-120">**Double**</span></span> <br/> |<span data-ttu-id="78a87-121">Der Prozentsatz entlang des Pfads vom Anfangs- zum Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="78a87-121">The percentage along the path from begin point to end point.</span></span> <span data-ttu-id="78a87-122">Muss zwischen 0 und 1 liegen.</span><span class="sxs-lookup"><span data-stu-id="78a87-122">Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="78a87-123">_Segment_</span><span class="sxs-lookup"><span data-stu-id="78a87-123">_segment_</span></span> <br/> |<span data-ttu-id="78a87-124">Optional</span><span class="sxs-lookup"><span data-stu-id="78a87-124">Optional</span></span>  <br/> |<span data-ttu-id="78a87-125">**Integer**</span><span class="sxs-lookup"><span data-stu-id="78a87-125">**Integer**</span></span> <br/> |<span data-ttu-id="78a87-126">Das 1-basierte Segment des Pfads, an dem der Tangentenwinkel berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="78a87-126">The 1-based segment of the path at which to calculate the tangent angle.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="78a87-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78a87-127">Return value</span></span>

 <span data-ttu-id="78a87-128">**Double**</span><span class="sxs-lookup"><span data-stu-id="78a87-128">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="78a87-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78a87-129">Remarks</span></span>

<span data-ttu-id="78a87-130">Wenn Sie einen _Segment_ Wert angeben, gibt ANGLEALONGPATH nur den Wert für dieses Segment zurück.</span><span class="sxs-lookup"><span data-stu-id="78a87-130">If you include a  _segment_ value, ANGLEALONGPATH returns the value for that segment only.</span></span> 
  
<span data-ttu-id="78a87-131">Wenn Sie einen _Segment_ Wert angeben, bestimmt ANGLEALONGPATH den Punkt der Tangente, indem Sie die Option _Reisen_ zum Berechnen der percertage im _Segment_verwenden.</span><span class="sxs-lookup"><span data-stu-id="78a87-131">If you include a  _segment_ value, ANGLEALONGPATH determines the point of the tangent by using  _travel_ to calculate the percertage along  _segment_.</span></span>
  
<span data-ttu-id="78a87-132">Wenn ein _Abschnitt_ oder _Segment_ nicht vorhanden ist, gibt Microsoft Visio #REF! zurück.</span><span class="sxs-lookup"><span data-stu-id="78a87-132">If either  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

