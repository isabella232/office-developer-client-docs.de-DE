---
title: Kanonische pidlidappointmentrecur (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentRecur
api_type:
- COM
ms.assetid: 56d6240f-d07b-48d1-aef0-bf57078ea6c3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: de50616664048af6b931a09df7c65461e9ee3399
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331780"
---
# <a name="pidlidappointmentrecur-canonical-property"></a><span data-ttu-id="87e91-103">Kanonische pidlidappointmentrecur (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="87e91-103">PidLidAppointmentRecur Canonical Property</span></span>

  
  
<span data-ttu-id="87e91-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87e91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87e91-105">Gibt die Datums-und Uhrzeitangaben an, zu denen eine wiederkehrende Reihe mit einem der Serienmuster und Bereiche, die in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)angegeben sind, auftritt.</span><span class="sxs-lookup"><span data-stu-id="87e91-105">Specifies the dates and times when a recurring series occurs by using one of the recurrence patterns and ranges that are specified in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="87e91-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="87e91-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="87e91-107">dispidApptRecur</span><span class="sxs-lookup"><span data-stu-id="87e91-107">dispidApptRecur</span></span>  <br/> |
|<span data-ttu-id="87e91-108">Eigenschaftengruppe:</span><span class="sxs-lookup"><span data-stu-id="87e91-108">Property set:</span></span>  <br/> |<span data-ttu-id="87e91-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="87e91-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="87e91-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="87e91-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="87e91-111">0x00008216</span><span class="sxs-lookup"><span data-stu-id="87e91-111">0x00008216</span></span>  <br/> |
|<span data-ttu-id="87e91-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="87e91-112">Data type:</span></span>  <br/> |<span data-ttu-id="87e91-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="87e91-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="87e91-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="87e91-114">Area:</span></span>  <br/> |<span data-ttu-id="87e91-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="87e91-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87e91-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="87e91-116">Remarks</span></span>

<span data-ttu-id="87e91-117">Diese Eigenschaft gibt die Datums-und Uhrzeitangaben an, zu denen eine wiederkehrende Reihe mit einem der in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)detaillierten Serienmuster und Bereiche auftritt.</span><span class="sxs-lookup"><span data-stu-id="87e91-117">This property specifies the dates and times when a recurring series occurs by using one of the recurrence patterns and ranges detailed in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span></span> <span data-ttu-id="87e91-118">Der Wert dieser Eigenschaft enthält auch Informationen zu geänderten und gelöschten Ausnahmen; Informationen wie Daten, Betreff, Ort und verschiedene andere Eigenschaften von Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="87e91-118">The value of this property also contains information about both modified and deleted exceptions; information such as dates, subject, location, and several other properties of exceptions.</span></span> <span data-ttu-id="87e91-119">Die Binärdaten in dieser Eigenschaft für wiederkehrende Kalenderelemente werden als **AppointmentRecurrencePattern** -Struktur gespeichert.</span><span class="sxs-lookup"><span data-stu-id="87e91-119">The binary data in this property for recurring calendar items is stored as the **AppointmentRecurrencePattern** structure.</span></span> <span data-ttu-id="87e91-120">Diese Eigenschaft darf nicht in Kalenderelementen für einzelne Instanzen vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="87e91-120">This property must not exist on single instance calendar items.</span></span> 
  
<span data-ttu-id="87e91-121">Es gibt einige Einschränkungen für Serien:</span><span class="sxs-lookup"><span data-stu-id="87e91-121">There are some limitations to recurrences:</span></span>
  
- <span data-ttu-id="87e91-122">Mehrere Instanzen dürfen nicht am selben Tag gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="87e91-122">Multiple instances must not start on the same day.</span></span>
    
- <span data-ttu-id="87e91-123">Vorkommen dürfen sich nicht überschneiden.</span><span class="sxs-lookup"><span data-stu-id="87e91-123">Occurrences must not overlap.</span></span> <span data-ttu-id="87e91-124">Eine Ausnahme, die das Startdatum einer Instanz in der Terminserie ändert, muss insbesondere an einem Datum auftreten, das sich nach dem Ende der vorherigen Instanz und dem Beginn der nächsten Instanz in der Terminserie befindet.</span><span class="sxs-lookup"><span data-stu-id="87e91-124">Specifically, an exception that modifies the start date of an instance in the recurring series must occur on a date that is after the end of the prior instance and the start of the next instance in the recurring series.</span></span> <span data-ttu-id="87e91-125">Das gleiche gilt, wenn die vorherigen oder nächsten Instanzen in der Terminserie Ausnahmen sind.</span><span class="sxs-lookup"><span data-stu-id="87e91-125">The same is true if the prior or next instances in the recurring series are exceptions.</span></span>
    
<span data-ttu-id="87e91-126">Der Zeitplan für eine wiederkehrende Reihe wird durch das Serienmuster und den Bereich bestimmt.</span><span class="sxs-lookup"><span data-stu-id="87e91-126">The schedule of a recurring series is determined by its recurrence pattern and range.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="87e91-127">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="87e91-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="87e91-128">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="87e91-128">Protocol specifications</span></span>

<span data-ttu-id="87e91-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87e91-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87e91-130">Stellt Eigenschaftenmengen Definitionen und Verweise auf zugehörige Exchange Server Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="87e91-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="87e91-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87e91-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87e91-132">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungsanfrage-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="87e91-132">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="87e91-133">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87e91-133">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87e91-134">Gibt die Eigenschaften und das Interaktionsmodell für e-Mails und andere Objekt Erinnerungen an.</span><span class="sxs-lookup"><span data-stu-id="87e91-134">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="87e91-135">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="87e91-135">Header files</span></span>

<span data-ttu-id="87e91-136">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="87e91-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="87e91-137">Stellt Definitionen von Datentypen bereit.</span><span class="sxs-lookup"><span data-stu-id="87e91-137">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="87e91-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87e91-138">See also</span></span>



[<span data-ttu-id="87e91-139">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="87e91-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="87e91-140">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="87e91-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="87e91-141">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="87e91-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="87e91-142">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="87e91-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

