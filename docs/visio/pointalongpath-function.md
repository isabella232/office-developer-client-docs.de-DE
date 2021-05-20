---
title: POINTALONGPATH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f91e5d9-89b8-5a0d-e01f-aa81fbd5e1fd
description: Gibt die Koordinaten eines Punkts auf oder im Abstand zum Pfad zurück.
ms.openlocfilehash: ce8b54bbd821cbfa6eb1f2789193ff8d7dda42d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430483"
---
# <a name="pointalongpath-function"></a><span data-ttu-id="5b457-103">POINTALONGPATH Function</span><span class="sxs-lookup"><span data-stu-id="5b457-103">POINTALONGPATH Function</span></span>

<span data-ttu-id="5b457-104">Gibt die Koordinaten eines Punkts auf oder im Abstand zum Pfad zurück.</span><span class="sxs-lookup"><span data-stu-id="5b457-104">Returns the coordinates of a point on, or offset from, the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="5b457-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="5b457-105">Version Information</span></span>

<span data-ttu-id="5b457-106">Hinzugefügte Version: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="5b457-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5b457-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b457-107">Syntax</span></span>

<span data-ttu-id="5b457-108">POINTALONGPATH(\*\* *Section* \**, \*\* *travel* \*\* \*\*\* [,offset]* \*\* \*\* *[,segment]* \*\* )</span><span class="sxs-lookup"><span data-stu-id="5b457-108">POINTALONGPATH(\*\* *section* \*\*, \*\* *travel* \*\* \*\* *[,offset]* \*\* \*\* *[,segment]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5b457-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b457-109">Parameters</span></span>

|<span data-ttu-id="5b457-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="5b457-110">**Name**</span></span>|<span data-ttu-id="5b457-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="5b457-111">**Required/Optional**</span></span>|<span data-ttu-id="5b457-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="5b457-112">**Data Type**</span></span>|<span data-ttu-id="5b457-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5b457-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5b457-114">_section_</span><span class="sxs-lookup"><span data-stu-id="5b457-114">_section_</span></span> <br/> |<span data-ttu-id="5b457-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5b457-115">Required</span></span>  <br/> |<span data-ttu-id="5b457-116">**String**</span><span class="sxs-lookup"><span data-stu-id="5b457-116">**String**</span></span> <br/> |<span data-ttu-id="5b457-117">Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).</span><span class="sxs-lookup"><span data-stu-id="5b457-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="5b457-118">_reise_</span><span class="sxs-lookup"><span data-stu-id="5b457-118">_travel_</span></span> <br/> |<span data-ttu-id="5b457-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5b457-119">Required</span></span>  <br/> |<span data-ttu-id="5b457-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="5b457-120">**Double**</span></span> <br/> |<span data-ttu-id="5b457-p101">Der Prozentsatz entlang des durchlaufenen Pfads vom Anfangs- zum Endpunkt, der den Punkt bezeichnet. Muss zwischen 0 und 1 liegen.</span><span class="sxs-lookup"><span data-stu-id="5b457-p101">The percentage of the path traversed, from the begin point to the end point that identifies the point. Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="5b457-123">_offset_</span><span class="sxs-lookup"><span data-stu-id="5b457-123">_offset_</span></span> <br/> |<span data-ttu-id="5b457-124">Optional</span><span class="sxs-lookup"><span data-stu-id="5b457-124">Optional</span></span>  <br/> |<span data-ttu-id="5b457-125">**Double**</span><span class="sxs-lookup"><span data-stu-id="5b457-125">**Double**</span></span> <br/> |<span data-ttu-id="5b457-p102">Der Abstand, um den der Punkt vom Pfad abgesetzt ist. Weitere Informationen finden Sie unter "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="5b457-p102">The distance that the point is offset from the path. See Remarks for more information.</span></span>  <br/> |
| <span data-ttu-id="5b457-128">_segment_</span><span class="sxs-lookup"><span data-stu-id="5b457-128">_segment_</span></span> <br/> |<span data-ttu-id="5b457-129">Optional</span><span class="sxs-lookup"><span data-stu-id="5b457-129">Optional</span></span>  <br/> |<span data-ttu-id="5b457-130">**Integer**</span><span class="sxs-lookup"><span data-stu-id="5b457-130">**Integer**</span></span> <br/> |<span data-ttu-id="5b457-131">Das auf 1 basierende Segment des Pfads, in dem die Koordinaten berechnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5b457-131">The 1-based segment of the path in which to calculate the coordinates.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5b457-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5b457-132">Return value</span></span>

 <span data-ttu-id="5b457-133">**Point**</span><span class="sxs-lookup"><span data-stu-id="5b457-133">**Point**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5b457-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5b457-134">Remarks</span></span>

<span data-ttu-id="5b457-135">Wenn _kein Abschnitt_ oder _Segment_ vorhanden ist, gibt Microsoft Visio #REF! zurück.</span><span class="sxs-lookup"><span data-stu-id="5b457-135">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="5b457-136">Positive  *Offsetwerte*  geben Punkte links von der Reiserichtung an.</span><span class="sxs-lookup"><span data-stu-id="5b457-136">Positive  *offset*  values specify points to the left of the direction of travel.</span></span> 
  
<span data-ttu-id="5b457-137">Negative  *Offsetwerte*  geben Punkte rechts neben der Reiserichtung an.</span><span class="sxs-lookup"><span data-stu-id="5b457-137">Negative  *offset*  values specify points to the right of the direction of travel.</span></span> 
  
<span data-ttu-id="5b457-138">Ein **Point** steht für ein geordnetes Paar geometrischer Koordinaten (*x,y*) als einzelner Wert.</span><span class="sxs-lookup"><span data-stu-id="5b457-138">A **Point** represents an ordered pair of geometric coordinates (*x,y*) as a single value.</span></span> 
  

