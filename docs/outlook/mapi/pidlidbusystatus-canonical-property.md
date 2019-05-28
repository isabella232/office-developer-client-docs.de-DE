---
title: Kanonische pidlidbusystatus (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusyStatus
api_type:
- COM
ms.assetid: 50c91fe6-2a61-4348-a16d-fd5c501b0715
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cb73a0e09436177b8b53a05588508886ee28a0a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342028"
---
# <a name="pidlidbusystatus-canonical-property"></a><span data-ttu-id="32f9b-103">Kanonische pidlidbusystatus (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="32f9b-103">PidLidBusyStatus Canonical Property</span></span>

  
  
<span data-ttu-id="32f9b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32f9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32f9b-105">Stellt die Verfügbarkeit des Benutzers für einen Termin dar.</span><span class="sxs-lookup"><span data-stu-id="32f9b-105">Represents the user's availability for an appointment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="32f9b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="32f9b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="32f9b-107">dispidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="32f9b-107">dispidBusyStatus</span></span>  <br/> |
|<span data-ttu-id="32f9b-108">Eigenschaftengruppe:</span><span class="sxs-lookup"><span data-stu-id="32f9b-108">Property set:</span></span>  <br/> |<span data-ttu-id="32f9b-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="32f9b-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="32f9b-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="32f9b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="32f9b-111">0x00008205</span><span class="sxs-lookup"><span data-stu-id="32f9b-111">0x00008205</span></span>  <br/> |
|<span data-ttu-id="32f9b-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="32f9b-112">Data type:</span></span>  <br/> |<span data-ttu-id="32f9b-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="32f9b-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="32f9b-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="32f9b-114">Area:</span></span>  <br/> |<span data-ttu-id="32f9b-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="32f9b-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="32f9b-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="32f9b-116">Remarks</span></span>

<span data-ttu-id="32f9b-117">Diese Eigenschaft gibt die Verfügbarkeit eines Benutzers für das vom Objekt beschriebene Ereignis an und muss einer der unten angegebenen Werte sein.</span><span class="sxs-lookup"><span data-stu-id="32f9b-117">This property specifies the availability of a user for the event described by the object and must be one of the values specified below.</span></span>
  
|<span data-ttu-id="32f9b-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="32f9b-118">**Value**</span></span>|<span data-ttu-id="32f9b-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="32f9b-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="32f9b-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="32f9b-120">0x00000000</span></span>  <br/> |<span data-ttu-id="32f9b-121">Der Benutzer ist verfügbar.</span><span class="sxs-lookup"><span data-stu-id="32f9b-121">The user is available.</span></span>  <br/> |
|<span data-ttu-id="32f9b-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="32f9b-122">0x00000001</span></span>  <br/> |<span data-ttu-id="32f9b-123">Der Benutzer hat ein vorläufiges Ereignis geplant.</span><span class="sxs-lookup"><span data-stu-id="32f9b-123">The user has a tentative event scheduled.</span></span>  <br/> |
|<span data-ttu-id="32f9b-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="32f9b-124">0x00000002</span></span>  <br/> |<span data-ttu-id="32f9b-125">Der Benutzer ist ausgelastet.</span><span class="sxs-lookup"><span data-stu-id="32f9b-125">The user is busy.</span></span>  <br/> |
|<span data-ttu-id="32f9b-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="32f9b-126">0x00000003</span></span>  <br/> |<span data-ttu-id="32f9b-127">Der Benutzer befindet sich nicht im Büro.</span><span class="sxs-lookup"><span data-stu-id="32f9b-127">The user is out of office.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="32f9b-128">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="32f9b-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="32f9b-129">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="32f9b-129">Protocol specifications</span></span>

<span data-ttu-id="32f9b-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="32f9b-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="32f9b-131">Stellt Eigenschaftenmengen Definitionen und Verweise auf zugehörige Exchange Server Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="32f9b-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="32f9b-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="32f9b-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="32f9b-133">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungsanfrage-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="32f9b-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="32f9b-134">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="32f9b-134">Header files</span></span>

<span data-ttu-id="32f9b-135">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="32f9b-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="32f9b-136">Stellt Definitionen von Datentypen bereit.</span><span class="sxs-lookup"><span data-stu-id="32f9b-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="32f9b-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32f9b-137">See also</span></span>



[<span data-ttu-id="32f9b-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="32f9b-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="32f9b-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="32f9b-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="32f9b-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="32f9b-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="32f9b-141">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="32f9b-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

