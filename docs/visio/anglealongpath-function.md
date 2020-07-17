---
title: ANGLEALONGPATH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Gibt den Winkel der Tangenten zum Pfad an einem gegebenen Punkt zurück.
ms.openlocfilehash: a15e45ff6135972cd1cd78382147a493f8fc8d69
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160293"
---
# <a name="anglealongpath-function"></a><span data-ttu-id="57f8e-103">ANGLEALONGPATH Function</span><span class="sxs-lookup"><span data-stu-id="57f8e-103">ANGLEALONGPATH Function</span></span>

<span data-ttu-id="57f8e-104">Gibt den Winkel der Tangenten zum Pfad an einem gegebenen Punkt zurück.</span><span class="sxs-lookup"><span data-stu-id="57f8e-104">Returns the angle of the tangent to the path at a given point.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="57f8e-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="57f8e-105">Version Information</span></span>

<span data-ttu-id="57f8e-106">Hinzugefügte Version: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="57f8e-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="57f8e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="57f8e-107">Syntax</span></span>

<span data-ttu-id="57f8e-108">ANGLEALONGPATH (***Abschnitt***, ***Reisen*** ***[, Segment]*** )</span><span class="sxs-lookup"><span data-stu-id="57f8e-108">ANGLEALONGPATH(***section***, ***travel*** ***[,segment]*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="57f8e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="57f8e-109">Parameters</span></span>

|<span data-ttu-id="57f8e-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="57f8e-110">**Name**</span></span>|<span data-ttu-id="57f8e-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="57f8e-111">**Required/Optional**</span></span>|<span data-ttu-id="57f8e-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="57f8e-112">**Data Type**</span></span>|<span data-ttu-id="57f8e-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="57f8e-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="57f8e-114">_section_</span><span class="sxs-lookup"><span data-stu-id="57f8e-114">_section_</span></span> <br/> |<span data-ttu-id="57f8e-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="57f8e-115">Required</span></span>  <br/> |<span data-ttu-id="57f8e-116">**String**</span><span class="sxs-lookup"><span data-stu-id="57f8e-116">**String**</span></span> <br/> |<span data-ttu-id="57f8e-117">Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).</span><span class="sxs-lookup"><span data-stu-id="57f8e-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="57f8e-118">_Reise_</span><span class="sxs-lookup"><span data-stu-id="57f8e-118">_travel_</span></span> <br/> |<span data-ttu-id="57f8e-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="57f8e-119">Required</span></span>  <br/> |<span data-ttu-id="57f8e-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="57f8e-120">**Double**</span></span> <br/> |<span data-ttu-id="57f8e-121">Der Prozentsatz entlang des Pfads vom Anfangs- zum Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="57f8e-121">The percentage along the path from begin point to end point.</span></span> <span data-ttu-id="57f8e-122">Muss zwischen 0 und 1 liegen.</span><span class="sxs-lookup"><span data-stu-id="57f8e-122">Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="57f8e-123">_segment_</span><span class="sxs-lookup"><span data-stu-id="57f8e-123">_segment_</span></span> <br/> |<span data-ttu-id="57f8e-124">Optional</span><span class="sxs-lookup"><span data-stu-id="57f8e-124">Optional</span></span>  <br/> |<span data-ttu-id="57f8e-125">**Integer**</span><span class="sxs-lookup"><span data-stu-id="57f8e-125">**Integer**</span></span> <br/> |<span data-ttu-id="57f8e-126">Das 1-basierte Segment des Pfads, an dem der Tangentenwinkel berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="57f8e-126">The 1-based segment of the path at which to calculate the tangent angle.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="57f8e-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="57f8e-127">Return value</span></span>

 <span data-ttu-id="57f8e-128">**Double**</span><span class="sxs-lookup"><span data-stu-id="57f8e-128">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="57f8e-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="57f8e-129">Remarks</span></span>

<span data-ttu-id="57f8e-130">Wenn Sie einen _Segment_ Wert einschließen, gibt ANGLEALONGPATH nur den Wert für dieses Segment zurück.</span><span class="sxs-lookup"><span data-stu-id="57f8e-130">If you include a  _segment_ value, ANGLEALONGPATH returns the value for that segment only.</span></span> 
  
<span data-ttu-id="57f8e-131">Wenn Sie einen _Segment_ Wert einschließen, bestimmt ANGLEALONGPATH den Eckpunkt der Tangente mithilfe von _Reisen_ , um das percertage entlang des _Segments_zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="57f8e-131">If you include a  _segment_ value, ANGLEALONGPATH determines the point of the tangent by using  _travel_ to calculate the percertage along  _segment_.</span></span>
  
<span data-ttu-id="57f8e-132">Wenn einer der _Abschnitte_ oder _Segmente_ nicht vorhanden ist, gibt Microsoft Visio #Ref! zurück.</span><span class="sxs-lookup"><span data-stu-id="57f8e-132">If either  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

