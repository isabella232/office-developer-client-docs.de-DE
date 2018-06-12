---
title: POINTALONGPATH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f91e5d9-89b8-5a0d-e01f-aa81fbd5e1fd
description: Gibt die Koordinaten eines Punkts auf oder im Abstand zum Pfad zurück.
ms.openlocfilehash: 9ce6f8c171515b46aaff0ce07cbe7da4f1e958d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797644"
---
# <a name="pointalongpath-function"></a><span data-ttu-id="8d2f8-103">POINTALONGPATH Function</span><span class="sxs-lookup"><span data-stu-id="8d2f8-103">POINTALONGPATH Function</span></span>

<span data-ttu-id="8d2f8-104">Gibt die Koordinaten eines Punkts auf oder im Abstand zum Pfad zurück.</span><span class="sxs-lookup"><span data-stu-id="8d2f8-104">Returns the coordinates of a point on, or offset from, the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="8d2f8-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="8d2f8-105">Version Information</span></span>

<span data-ttu-id="8d2f8-106">Hinzugefügte Version: Visio 2010</span><span class="sxs-lookup"><span data-stu-id="8d2f8-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8d2f8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d2f8-107">Syntax</span></span>

<span data-ttu-id="8d2f8-108">POINTALONGPATH (** *Abschnitt* **, ** *Reisen* ** ** *[, Offset]* ** ** *[, Segment]* **)</span><span class="sxs-lookup"><span data-stu-id="8d2f8-108">POINTALONGPATH(** *section* **, ** *travel* ** ** *[,offset]* ** ** *[,segment]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8d2f8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d2f8-109">Parameters</span></span>

|<span data-ttu-id="8d2f8-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="8d2f8-110">**Name**</span></span>|<span data-ttu-id="8d2f8-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="8d2f8-111">**Required/Optional**</span></span>|<span data-ttu-id="8d2f8-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="8d2f8-112">**Data Type**</span></span>|<span data-ttu-id="8d2f8-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8d2f8-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8d2f8-114">_section_</span><span class="sxs-lookup"><span data-stu-id="8d2f8-114">_section_</span></span> <br/> |<span data-ttu-id="8d2f8-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8d2f8-115">Required</span></span>  <br/> |<span data-ttu-id="8d2f8-116">**String**</span><span class="sxs-lookup"><span data-stu-id="8d2f8-116">**String**</span></span> <br/> |<span data-ttu-id="8d2f8-117">Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).</span><span class="sxs-lookup"><span data-stu-id="8d2f8-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="8d2f8-118">_Reisen_</span><span class="sxs-lookup"><span data-stu-id="8d2f8-118">_travel_</span></span> <br/> |<span data-ttu-id="8d2f8-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8d2f8-119">Required</span></span>  <br/> |<span data-ttu-id="8d2f8-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="8d2f8-120">**Double**</span></span> <br/> |<span data-ttu-id="8d2f8-p101">Der Prozentsatz entlang des durchlaufenen Pfads vom Anfangs- zum Endpunkt, der den Punkt bezeichnet. Muss zwischen 0 und 1 liegen.</span><span class="sxs-lookup"><span data-stu-id="8d2f8-p101">The percentage of the path traversed, from the begin point to the end point that identifies the point. Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="8d2f8-123">_Offset_</span><span class="sxs-lookup"><span data-stu-id="8d2f8-123">_offset_</span></span> <br/> |<span data-ttu-id="8d2f8-124">Optional</span><span class="sxs-lookup"><span data-stu-id="8d2f8-124">Optional</span></span>  <br/> |<span data-ttu-id="8d2f8-125">**Double**</span><span class="sxs-lookup"><span data-stu-id="8d2f8-125">**Double**</span></span> <br/> |<span data-ttu-id="8d2f8-p102">Der Abstand, um den der Punkt vom Pfad abgesetzt ist. Weitere Informationen finden Sie unter "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="8d2f8-p102">The distance that the point is offset from the path. See Remarks for more information.</span></span>  <br/> |
| <span data-ttu-id="8d2f8-128">_Segment_</span><span class="sxs-lookup"><span data-stu-id="8d2f8-128">_segment_</span></span> <br/> |<span data-ttu-id="8d2f8-129">Optional</span><span class="sxs-lookup"><span data-stu-id="8d2f8-129">Optional</span></span>  <br/> |<span data-ttu-id="8d2f8-130">**Integer**</span><span class="sxs-lookup"><span data-stu-id="8d2f8-130">**Integer**</span></span> <br/> |<span data-ttu-id="8d2f8-131">Das auf 1 basierende Segment des Pfads, in dem die Koordinaten berechnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8d2f8-131">The 1-based segment of the path in which to calculate the coordinates.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8d2f8-132">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="8d2f8-132">Return value</span></span>

 <span data-ttu-id="8d2f8-133">**Punkt**</span><span class="sxs-lookup"><span data-stu-id="8d2f8-133">**Point**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8d2f8-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d2f8-134">Remarks</span></span>

<span data-ttu-id="8d2f8-135">Wenn _Section_ oder _Segment_ nicht vorhanden ist, gibt Microsoft Visio #REF! zurück.</span><span class="sxs-lookup"><span data-stu-id="8d2f8-135">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="8d2f8-136">Positive *Offset* -Werte geben Punkten Links der Laufrichtung an.</span><span class="sxs-lookup"><span data-stu-id="8d2f8-136">Positive  *offset*  values specify points to the left of the direction of travel.</span></span> 
  
<span data-ttu-id="8d2f8-137">Negative *Offset* -Werte geben Punkten rechts der Laufrichtung an.</span><span class="sxs-lookup"><span data-stu-id="8d2f8-137">Negative  *offset*  values specify points to the right of the direction of travel.</span></span> 
  
<span data-ttu-id="8d2f8-138">Ein **Punkt** stellt ein geordnetes Paar geometrischer Koordinaten (*X, y*) als einen single-Wert.</span><span class="sxs-lookup"><span data-stu-id="8d2f8-138">A **Point** represents an ordered pair of geometric coordinates (*x,y*) as a single value.</span></span> 
  

