---
title: ANGLEALONGPATH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Gibt den Winkel der Tangenten zum Pfad an einem gegebenen Punkt zurück.
ms.openlocfilehash: ec5529037275fc8661972cc7403886cd33150b38
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796420"
---
# <a name="anglealongpath-function"></a><span data-ttu-id="d67b8-103">ANGLEALONGPATH Function</span><span class="sxs-lookup"><span data-stu-id="d67b8-103">ANGLEALONGPATH Function</span></span>

<span data-ttu-id="d67b8-104">Gibt den Winkel der Tangenten zum Pfad an einem gegebenen Punkt zurück.</span><span class="sxs-lookup"><span data-stu-id="d67b8-104">Returns the angle of the tangent to the path at a given point.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="d67b8-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="d67b8-105">Version Information</span></span>

<span data-ttu-id="d67b8-106">Hinzugefügte Version: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="d67b8-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d67b8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d67b8-107">Syntax</span></span>

<span data-ttu-id="d67b8-108">ANGLEALONGPATH (** *Abschnitt* **, ** *Reisen* ** ** *[, Segment]* **)</span><span class="sxs-lookup"><span data-stu-id="d67b8-108">ANGLEALONGPATH(** *section* **, ** *travel* ** ** *[,segment]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d67b8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d67b8-109">Parameters</span></span>

|<span data-ttu-id="d67b8-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="d67b8-110">**Name**</span></span>|<span data-ttu-id="d67b8-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="d67b8-111">**Required/Optional**</span></span>|<span data-ttu-id="d67b8-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="d67b8-112">**Data Type**</span></span>|<span data-ttu-id="d67b8-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d67b8-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d67b8-114">_section_</span><span class="sxs-lookup"><span data-stu-id="d67b8-114">_section_</span></span> <br/> |<span data-ttu-id="d67b8-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d67b8-115">Required</span></span>  <br/> |<span data-ttu-id="d67b8-116">**String**</span><span class="sxs-lookup"><span data-stu-id="d67b8-116">**String**</span></span> <br/> |<span data-ttu-id="d67b8-117">Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).</span><span class="sxs-lookup"><span data-stu-id="d67b8-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="d67b8-118">_Reisen_</span><span class="sxs-lookup"><span data-stu-id="d67b8-118">_travel_</span></span> <br/> |<span data-ttu-id="d67b8-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d67b8-119">Required</span></span>  <br/> |<span data-ttu-id="d67b8-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="d67b8-120">**Double**</span></span> <br/> |<span data-ttu-id="d67b8-p101">Der Prozentsatz entlang des Pfads vom Anfangs- zum Endpunkt. Muss zwischen 0 und 1 liegen.</span><span class="sxs-lookup"><span data-stu-id="d67b8-p101">The percentage along the path from begin point to end point. Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="d67b8-123">_Segment_</span><span class="sxs-lookup"><span data-stu-id="d67b8-123">_segment_</span></span> <br/> |<span data-ttu-id="d67b8-124">Optional</span><span class="sxs-lookup"><span data-stu-id="d67b8-124">Optional</span></span>  <br/> |<span data-ttu-id="d67b8-125">**Integer**</span><span class="sxs-lookup"><span data-stu-id="d67b8-125">**Integer**</span></span> <br/> |<span data-ttu-id="d67b8-126">Das 1-basierte Segment des Pfads, an dem der Tangentenwinkel berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d67b8-126">The 1-based segment of the path at which to calculate the tangent angle.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d67b8-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d67b8-127">Return value</span></span>

 <span data-ttu-id="d67b8-128">**Double**</span><span class="sxs-lookup"><span data-stu-id="d67b8-128">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d67b8-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d67b8-129">Remarks</span></span>

<span data-ttu-id="d67b8-130">Wenn Sie einen Wert für _Segment_ eingeschlossen, gibt ANGLEALONGPATH den Wert für dieses Segment nur zurück.</span><span class="sxs-lookup"><span data-stu-id="d67b8-130">If you include a  _segment_ value, ANGLEALONGPATH returns the value for that segment only.</span></span> 
  
<span data-ttu-id="d67b8-131">Wenn Sie einen Wert für _Segment_ eingeschlossen, bestimmt ANGLEALONGPATH den Punkt der Tangente mithilfe von _unterwegs sind_ , um den Prozentsatz entlang _Segment_zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="d67b8-131">If you include a  _segment_ value, ANGLEALONGPATH determines the point of the tangent by using  _travel_ to calculate the percertage along  _segment_.</span></span>
  
<span data-ttu-id="d67b8-132">Wenn _Section_ oder _Segment_ nicht vorhanden ist, gibt Microsoft Visio #REF! zurück.</span><span class="sxs-lookup"><span data-stu-id="d67b8-132">If either  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

