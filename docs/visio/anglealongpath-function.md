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
# <a name="anglealongpath-function"></a><span data-ttu-id="28460-103">ANGLEALONGPATH Function</span><span class="sxs-lookup"><span data-stu-id="28460-103">ANGLEALONGPATH Function</span></span>

<span data-ttu-id="28460-104">Gibt den Winkel der Tangenten zum Pfad an einem gegebenen Punkt zurück.</span><span class="sxs-lookup"><span data-stu-id="28460-104">Returns the angle of the tangent to the path at a given point.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="28460-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="28460-105">Version Information</span></span>

<span data-ttu-id="28460-106">Hinzugefügte Version: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="28460-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="28460-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="28460-107">Syntax</span></span>

<span data-ttu-id="28460-108">ANGLEALONGPATH(***section***, ***travel*** ***[,segment]*** )</span><span class="sxs-lookup"><span data-stu-id="28460-108">ANGLEALONGPATH(***section***, ***travel*** ***[,segment]*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="28460-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="28460-109">Parameters</span></span>

|<span data-ttu-id="28460-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="28460-110">**Name**</span></span>|<span data-ttu-id="28460-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="28460-111">**Required/Optional**</span></span>|<span data-ttu-id="28460-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="28460-112">**Data Type**</span></span>|<span data-ttu-id="28460-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="28460-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="28460-114">_section_</span><span class="sxs-lookup"><span data-stu-id="28460-114">_section_</span></span> <br/> |<span data-ttu-id="28460-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="28460-115">Required</span></span>  <br/> |<span data-ttu-id="28460-116">**String**</span><span class="sxs-lookup"><span data-stu-id="28460-116">**String**</span></span> <br/> |<span data-ttu-id="28460-117">Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).</span><span class="sxs-lookup"><span data-stu-id="28460-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="28460-118">_reise_</span><span class="sxs-lookup"><span data-stu-id="28460-118">_travel_</span></span> <br/> |<span data-ttu-id="28460-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="28460-119">Required</span></span>  <br/> |<span data-ttu-id="28460-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="28460-120">**Double**</span></span> <br/> |<span data-ttu-id="28460-p101">Der Prozentsatz entlang des Pfads vom Anfangs- zum Endpunkt. Muss zwischen 0 und 1 liegen.</span><span class="sxs-lookup"><span data-stu-id="28460-p101">The percentage along the path from begin point to end point. Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="28460-123">_segment_</span><span class="sxs-lookup"><span data-stu-id="28460-123">_segment_</span></span> <br/> |<span data-ttu-id="28460-124">Optional</span><span class="sxs-lookup"><span data-stu-id="28460-124">Optional</span></span>  <br/> |<span data-ttu-id="28460-125">**Integer**</span><span class="sxs-lookup"><span data-stu-id="28460-125">**Integer**</span></span> <br/> |<span data-ttu-id="28460-126">Das 1-basierte Segment des Pfads, an dem der Tangentenwinkel berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="28460-126">The 1-based segment of the path at which to calculate the tangent angle.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="28460-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="28460-127">Return value</span></span>

 <span data-ttu-id="28460-128">**Double**</span><span class="sxs-lookup"><span data-stu-id="28460-128">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="28460-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="28460-129">Remarks</span></span>

<span data-ttu-id="28460-130">Wenn Sie einen  _Segmentwert_ enthalten, gibt ANGLEALONGPATH nur den Wert für dieses Segment zurück.</span><span class="sxs-lookup"><span data-stu-id="28460-130">If you include a  _segment_ value, ANGLEALONGPATH returns the value for that segment only.</span></span> 
  
<span data-ttu-id="28460-131">Wenn Sie einen _Segmentwert_ verwenden, bestimmt ANGLEALONGPATH den Punkt der Tangente mithilfe von _Travel,_ um die Percertage entlang des Abschnitts _zu berechnen._</span><span class="sxs-lookup"><span data-stu-id="28460-131">If you include a  _segment_ value, ANGLEALONGPATH determines the point of the tangent by using  _travel_ to calculate the percertage along  _segment_.</span></span>
  
<span data-ttu-id="28460-132">Wenn weder _abschnitt noch_ _segment_ vorhanden ist, gibt Microsoft Visio #REF! zurück.</span><span class="sxs-lookup"><span data-stu-id="28460-132">If either  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

