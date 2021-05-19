---
title: PidLidAppointmentRecur (kanonische Eigenschaft)
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
# <a name="pidlidappointmentrecur-canonical-property"></a><span data-ttu-id="a1aa2-103">PidLidAppointmentRecur (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a1aa2-103">PidLidAppointmentRecur Canonical Property</span></span>

  
  
<span data-ttu-id="a1aa2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1aa2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1aa2-105">Gibt die Datums- und Zeitangaben an, zu denen eine Serienserie auftritt, indem eines der serienmäßigen Muster und Bereiche verwendet wird, die in [[MS-OXOCAL] angegeben sind.](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1aa2-105">Specifies the dates and times when a recurring series occurs by using one of the recurrence patterns and ranges that are specified in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a1aa2-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a1aa2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a1aa2-107">dispidApptRecur</span><span class="sxs-lookup"><span data-stu-id="a1aa2-107">dispidApptRecur</span></span>  <br/> |
|<span data-ttu-id="a1aa2-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="a1aa2-108">Property set:</span></span>  <br/> |<span data-ttu-id="a1aa2-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="a1aa2-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="a1aa2-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="a1aa2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a1aa2-111">0x00008216</span><span class="sxs-lookup"><span data-stu-id="a1aa2-111">0x00008216</span></span>  <br/> |
|<span data-ttu-id="a1aa2-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a1aa2-112">Data type:</span></span>  <br/> |<span data-ttu-id="a1aa2-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a1aa2-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a1aa2-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a1aa2-114">Area:</span></span>  <br/> |<span data-ttu-id="a1aa2-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="a1aa2-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1aa2-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a1aa2-116">Remarks</span></span>

<span data-ttu-id="a1aa2-117">Diese Eigenschaft gibt die Datums- und Zeitangaben an, zu denen eine Serienserie auftritt, indem eines der Serienmuster und Bereiche verwendet wird, die in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)detailliert angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="a1aa2-117">This property specifies the dates and times when a recurring series occurs by using one of the recurrence patterns and ranges detailed in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span></span> <span data-ttu-id="a1aa2-118">Der Wert dieser Eigenschaft enthält auch Informationen zu geänderten und gelöschten Ausnahmen. Informationen wie Datum, Betreff, Ort und mehrere andere Eigenschaften von Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="a1aa2-118">The value of this property also contains information about both modified and deleted exceptions; information such as dates, subject, location, and several other properties of exceptions.</span></span> <span data-ttu-id="a1aa2-119">Die Binärdaten in dieser Eigenschaft für wiederkehrende Kalenderelemente werden als **AppointmentRecurrencePattern-Struktur** gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a1aa2-119">The binary data in this property for recurring calendar items is stored as the **AppointmentRecurrencePattern** structure.</span></span> <span data-ttu-id="a1aa2-120">Diese Eigenschaft darf in Kalenderelementen einer einzelnen Instanz nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="a1aa2-120">This property must not exist on single instance calendar items.</span></span> 
  
<span data-ttu-id="a1aa2-121">Es gibt einige Einschränkungen für Wiederholungen:</span><span class="sxs-lookup"><span data-stu-id="a1aa2-121">There are some limitations to recurrences:</span></span>
  
- <span data-ttu-id="a1aa2-122">Mehrere Instanzen dürfen nicht am gleichen Tag gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="a1aa2-122">Multiple instances must not start on the same day.</span></span>
    
- <span data-ttu-id="a1aa2-123">Vorkommen dürfen nicht überlappen.</span><span class="sxs-lookup"><span data-stu-id="a1aa2-123">Occurrences must not overlap.</span></span> <span data-ttu-id="a1aa2-124">Insbesondere muss eine Ausnahme, die das Startdatum einer Instanz in der Serienserie ändert, an einem Datum auftreten, das nach dem Ende der vorherigen Instanz und dem Beginn der nächsten Instanz in der Serienserie liegt.</span><span class="sxs-lookup"><span data-stu-id="a1aa2-124">Specifically, an exception that modifies the start date of an instance in the recurring series must occur on a date that is after the end of the prior instance and the start of the next instance in the recurring series.</span></span> <span data-ttu-id="a1aa2-125">Dasselbe gilt, wenn die vorherigen oder nächsten Instanzen in der Serienserie Ausnahmen sind.</span><span class="sxs-lookup"><span data-stu-id="a1aa2-125">The same is true if the prior or next instances in the recurring series are exceptions.</span></span>
    
<span data-ttu-id="a1aa2-126">Der Zeitplan einer Serienserie wird durch das Serienmuster und den Bereich bestimmt.</span><span class="sxs-lookup"><span data-stu-id="a1aa2-126">The schedule of a recurring series is determined by its recurrence pattern and range.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a1aa2-127">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a1aa2-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a1aa2-128">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a1aa2-128">Protocol specifications</span></span>

<span data-ttu-id="a1aa2-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1aa2-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1aa2-130">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="a1aa2-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a1aa2-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1aa2-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1aa2-132">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="a1aa2-132">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="a1aa2-133">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1aa2-133">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1aa2-134">Gibt die Eigenschaften und das Interaktionsmodell für E-Mail- und andere Objekterinnerungen an.</span><span class="sxs-lookup"><span data-stu-id="a1aa2-134">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a1aa2-135">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="a1aa2-135">Header files</span></span>

<span data-ttu-id="a1aa2-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a1aa2-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="a1aa2-137">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a1aa2-137">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a1aa2-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1aa2-138">See also</span></span>



[<span data-ttu-id="a1aa2-139">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a1aa2-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a1aa2-140">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="a1aa2-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a1aa2-141">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a1aa2-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a1aa2-142">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a1aa2-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

