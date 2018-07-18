---
title: PidTagScheduleInfoAppointmentTombstone (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoAppointmentTombstone
api_type:
- COM
ms.assetid: 6b82e2ee-992f-4cbe-bdcb-e7465e556640
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 37a6d101f6ee9c04236253e143aff3a51a9208d3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795083"
---
# <a name="pidtagscheduleinfoappointmenttombstone-canonical-property"></a><span data-ttu-id="4f2d1-103">PidTagScheduleInfoAppointmentTombstone (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4f2d1-103">PidTagScheduleInfoAppointmentTombstone Canonical Property</span></span>

  
  
<span data-ttu-id="4f2d1-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4f2d1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4f2d1-105">Enthält eine Liste der Datenblöcke, die Besprechungen darstellen, die abgelehnt wurden.</span><span class="sxs-lookup"><span data-stu-id="4f2d1-105">Contains a list of data blocks that represent meetings that have been declined.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4f2d1-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4f2d1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4f2d1-107">PR_SCHDINFO_APPT_TOMBSTONE</span><span class="sxs-lookup"><span data-stu-id="4f2d1-107">PR_SCHDINFO_APPT_TOMBSTONE</span></span>  <br/> |
|<span data-ttu-id="4f2d1-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="4f2d1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4f2d1-109">0x686A</span><span class="sxs-lookup"><span data-stu-id="4f2d1-109">0x686A</span></span>  <br/> |
|<span data-ttu-id="4f2d1-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4f2d1-110">Data type:</span></span>  <br/> |<span data-ttu-id="4f2d1-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4f2d1-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4f2d1-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4f2d1-112">Area:</span></span>  <br/> |<span data-ttu-id="4f2d1-113">Frei/Gebucht-Informationen</span><span class="sxs-lookup"><span data-stu-id="4f2d1-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f2d1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f2d1-114">Remarks</span></span>

<span data-ttu-id="4f2d1-115">Die Datenblöcke beginnen mit einer Kopfzeile der 32-Bit-Werte als definiert:</span><span class="sxs-lookup"><span data-stu-id="4f2d1-115">The data blocks begin with a header of 32 bit values defined as:</span></span>
  
|<span data-ttu-id="4f2d1-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="4f2d1-116">**Value**</span></span>|<span data-ttu-id="4f2d1-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f2d1-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4f2d1-118">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="4f2d1-118">Identifier</span></span>  <br/> |<span data-ttu-id="4f2d1-119">Dieses Feld muss den Wert 0xBEDEAFCD sein.</span><span class="sxs-lookup"><span data-stu-id="4f2d1-119">This field must be the value 0xBEDEAFCD.</span></span>  <br/> |
|<span data-ttu-id="4f2d1-120">HeaderSize</span><span class="sxs-lookup"><span data-stu-id="4f2d1-120">HeaderSize</span></span>  <br/> |<span data-ttu-id="4f2d1-121">Dieses Feld muss den Wert 0x00000014 haben.</span><span class="sxs-lookup"><span data-stu-id="4f2d1-121">This field must have the value 0x00000014.</span></span>  <br/> |
|<span data-ttu-id="4f2d1-122">Version</span><span class="sxs-lookup"><span data-stu-id="4f2d1-122">Version</span></span>  <br/> |<span data-ttu-id="4f2d1-123">Dieses Feld muss den Wert 3 haben.</span><span class="sxs-lookup"><span data-stu-id="4f2d1-123">This field must have the value 3.</span></span>  <br/> |
|<span data-ttu-id="4f2d1-124">RecordsCount</span><span class="sxs-lookup"><span data-stu-id="4f2d1-124">RecordsCount</span></span>  <br/> |<span data-ttu-id="4f2d1-125">Die Anzahl der Datensätze, die folgen.</span><span class="sxs-lookup"><span data-stu-id="4f2d1-125">The count of records that follow.</span></span>  <br/> |
|<span data-ttu-id="4f2d1-126">RecordsSize</span><span class="sxs-lookup"><span data-stu-id="4f2d1-126">RecordsSize</span></span>  <br/> |<span data-ttu-id="4f2d1-127">Dieses Feld muss den Wert 0x00000014 haben.</span><span class="sxs-lookup"><span data-stu-id="4f2d1-127">This field must have the value 0x00000014.</span></span>  <br/> |
   
<span data-ttu-id="4f2d1-128">Die Kopfzeile folgt **RecordsCount** Einträge der 32-Bit-Werte als definiert:</span><span class="sxs-lookup"><span data-stu-id="4f2d1-128">The header is followed by **RecordsCount** entries of 32 bit values defined as:</span></span> 
  
|<span data-ttu-id="4f2d1-129">**Wert**</span><span class="sxs-lookup"><span data-stu-id="4f2d1-129">**Value**</span></span>|<span data-ttu-id="4f2d1-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f2d1-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4f2d1-131">StartTime</span><span class="sxs-lookup"><span data-stu-id="4f2d1-131">StartTime</span></span>  <br/> |<span data-ttu-id="4f2d1-132">Die Besprechung Objekt Startzeit in Minuten seit Mitternacht, 1. Januar 1601 UTC.</span><span class="sxs-lookup"><span data-stu-id="4f2d1-132">The meeting object's start time in minutes since midnight, January 1, 1601, UTC.</span></span>  <br/> |
|<span data-ttu-id="4f2d1-133">EndTime</span><span class="sxs-lookup"><span data-stu-id="4f2d1-133">EndTime</span></span>  <br/> |<span data-ttu-id="4f2d1-134">Die Besprechung Objekt Endzeit in Minuten seit Mitternacht, 1. Januar 1601 UTC.</span><span class="sxs-lookup"><span data-stu-id="4f2d1-134">The meeting object's end time in minutes since midnight, January 1, 1601, UTC.</span></span>  <br/> |
|<span data-ttu-id="4f2d1-135">GlobalObjectIdSize</span><span class="sxs-lookup"><span data-stu-id="4f2d1-135">GlobalObjectIdSize</span></span>  <br/> |<span data-ttu-id="4f2d1-136">Die Größe des Feld GlobalObjectId in Bytes.</span><span class="sxs-lookup"><span data-stu-id="4f2d1-136">The size, in bytes, of the GlobalObjectId field.</span></span>  <br/> |
|<span data-ttu-id="4f2d1-137">GlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="4f2d1-137">GlobalObjectId</span></span>  <br/> |<span data-ttu-id="4f2d1-138">Der Wert der Eigenschaft **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) der Besprechung dieser Datensatz darstellt.</span><span class="sxs-lookup"><span data-stu-id="4f2d1-138">The value of the **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) property of the meeting this record represents.</span></span>  <br/> |
|<span data-ttu-id="4f2d1-139">UserName</span><span class="sxs-lookup"><span data-stu-id="4f2d1-139">UserName</span></span>  <br/> |<span data-ttu-id="4f2d1-140">Die ersten beiden Bytes sind die Länge der Zeichenfolge PT_STRING8, die bildet.</span><span class="sxs-lookup"><span data-stu-id="4f2d1-140">The first two bytes are the length of the PT_STRING8 string that follows.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="4f2d1-141">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4f2d1-141">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4f2d1-142">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4f2d1-142">Protocol specifications</span></span>

<span data-ttu-id="4f2d1-143">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f2d1-143">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f2d1-144">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="4f2d1-144">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4f2d1-145">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f2d1-145">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f2d1-146">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="4f2d1-146">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4f2d1-147">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="4f2d1-147">Header files</span></span>

<span data-ttu-id="4f2d1-148">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4f2d1-148">Mapidefs.h</span></span>
  
> <span data-ttu-id="4f2d1-149">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4f2d1-149">Provides data type definitions.</span></span>
    
<span data-ttu-id="4f2d1-150">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4f2d1-150">Mapitags.h</span></span>
  
> <span data-ttu-id="4f2d1-151">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4f2d1-151">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4f2d1-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f2d1-152">See also</span></span>



[<span data-ttu-id="4f2d1-153">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4f2d1-153">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4f2d1-154">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4f2d1-154">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4f2d1-155">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4f2d1-155">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4f2d1-156">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4f2d1-156">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

