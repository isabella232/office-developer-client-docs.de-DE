---
title: Kanonische Pidlidappointmenttimezonedefinitionstartdisplay (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionStartDispl
api_type:
- COM
ms.assetid: 08239670-3211-420c-99d7-0056ed967cb8
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 504dc4b1cecb9798590e4a15968acc3aa98fe4a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345017"
---
# <a name="pidlidappointmenttimezonedefinitionstartdisplay-canonical-property"></a><span data-ttu-id="0ffef-103">Kanonische Pidlidappointmenttimezonedefinitionstartdisplay (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0ffef-103">PidLidAppointmentTimeZoneDefinitionStartDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="0ffef-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ffef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ffef-105">Enthält einen Stream, der dem beibehaltenen Format einer [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) -Struktur zugeordnet wird, in der die Beschreibung für die Zeitzone gespeichert wird, die verwendet wird, wenn die Startzeit eines einzelnen Termins oder einer Besprechungsanfrage ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="0ffef-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when the start time of a single-instance appointment or meeting request is selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0ffef-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0ffef-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0ffef-107">dispidApptTZDefStartDisplay</span><span class="sxs-lookup"><span data-stu-id="0ffef-107">dispidApptTZDefStartDisplay</span></span>  <br/> |
|<span data-ttu-id="0ffef-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="0ffef-108">Property set:</span></span>  <br/> |<span data-ttu-id="0ffef-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="0ffef-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="0ffef-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="0ffef-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0ffef-111">0x0000825E</span><span class="sxs-lookup"><span data-stu-id="0ffef-111">0x0000825E</span></span>  <br/> |
|<span data-ttu-id="0ffef-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0ffef-112">Data type:</span></span>  <br/> |<span data-ttu-id="0ffef-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0ffef-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0ffef-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0ffef-114">Area:</span></span>  <br/> |<span data-ttu-id="0ffef-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="0ffef-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ffef-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ffef-116">Remarks</span></span>

<span data-ttu-id="0ffef-117">Microsoft Office Outlook 2003 oder früher und Lösungen, die auf Collaboration Data Objects (CDO) 1.2.1 basieren und nicht das Kalender Aktualisierungstool für Outlook oder Microsoft Exchange Server ausgeführt haben, speichern Sie die Startzeit und die Endzeit der einzelnen Instanz. Termine und Besprechungsanfragen in koordinierter weltZeit (UTC).</span><span class="sxs-lookup"><span data-stu-id="0ffef-117">Microsoft Office Outlook 2003 or earlier, and solutions that are based on Collaboration Data Objects (CDO) 1.2.1 and that have not run the calendar update tool for Outlook or Microsoft Exchange Server, store the start time and end time of single-instance appointments and meeting requests in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="0ffef-118">Diese Clients speichern keine Informationen für die Zeitzone, in der der Termin oder die Besprechungsanfrage erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0ffef-118">These clients do not store any information for the time zone in which the appointment or meeting request is created.</span></span>
  
<span data-ttu-id="0ffef-119">Versionen von Outlook seit Microsoft Office Outlook 2007 und auf CDO 1.2.1 basierende Lösungen, die das Outlook-oder Exchange Server-Kalender Aktualisierungstool ausgeführt haben, verwenden Sie diese Eigenschaft, um die Zeitzone für die Startzeit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="0ffef-119">Versions of Outlook since Microsoft Office Outlook 2007, and solutions based on CDO 1.2.1 that have run the Outlook or Exchange Server calendar update tool use this property to store the time zone for the start time.</span></span> <span data-ttu-id="0ffef-120">Die **dispidApptTZDefStartDisplay** -Eigenschaft zeigt den Termin oder die Besprechung in der ursprünglich geplanten Zeitzone an.</span><span class="sxs-lookup"><span data-stu-id="0ffef-120">The **dispidApptTZDefStartDisplay** property shows the appointment or meeting in the original time zone that it was scheduled.</span></span> <span data-ttu-id="0ffef-121">Sie bestimmt, ob die Startzeit angepasst werden soll, wenn sich die Regeln der Zeitzone ändern.</span><span class="sxs-lookup"><span data-stu-id="0ffef-121">It determines whether the start time should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="0ffef-122">Wenn diese Eigenschaft nicht vorhanden ist, wird die aktuelle lokale Zeitzone angenommen.</span><span class="sxs-lookup"><span data-stu-id="0ffef-122">If this property is missing, the current local time zone is assumed.</span></span> <span data-ttu-id="0ffef-123">Diese Eigenschaft wird nur zu Anzeigezwecken verwendet und nicht in der Serienerweiterung verwendet.</span><span class="sxs-lookup"><span data-stu-id="0ffef-123">This property is used for display purposes only and is not used in recurrence expansion.</span></span> 
  
<span data-ttu-id="0ffef-124">Ein Parser muss beim Lesen eines Datenstroms, der von dieser Eigenschaft abgerufen wurde, vorsichtig sein, oder wenn er **TZDEFINITION** in einem Stream für die Verpflichtung für eine binäre Eigenschaft wie **dispidApptTZDefStartDisplay**beibehält.</span><span class="sxs-lookup"><span data-stu-id="0ffef-124">A parser must be careful when it reads a stream obtained from this property, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefStartDisplay**.</span></span> <span data-ttu-id="0ffef-125">Weitere Informationen finden Sie unter [Informationen zum Speichern von TZDEFINITION in einem Stream, um eine binäre Eigenschaft zu über](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)nehmen.</span><span class="sxs-lookup"><span data-stu-id="0ffef-125">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="0ffef-126">Diese Eigenschaft gibt Zeitzoneninformationen für die **dispidApptStartWhole** ([pidlidappointmentstartwhole (](pidlidappointmentstartwhole-canonical-property.md))-Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="0ffef-126">This property specifies time zone information for the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="0ffef-127">Der Wert von **dispidApptTZDefStartDisplay** wird verwendet, um das Startdatum und die Uhrzeit für Anzeigezwecke von UTC in die lokale Zeitzone zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="0ffef-127">The value of **dispidApptTZDefStartDisplay** is used to convert the start date and time from UTC to the local time zone for display purposes.</span></span> <span data-ttu-id="0ffef-128">Für jedes **TZRULE** , das von dieser Eigenschaft angegeben wird, darf das TZRULE_FLAG_RECUR_CURRENT_TZREG-Flag nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0ffef-128">For each **TZRULE** specified by this property, the TZRULE_FLAG_RECUR_CURRENT_TZREG flag must not be set.</span></span> <span data-ttu-id="0ffef-129">Wenn die **TZRULE** beispielsweise die effektive Regel ist, muss der Wert des Felds, **TZRULE** "0x0002" sein. Andernfalls muss es "0x0000" sein.</span><span class="sxs-lookup"><span data-stu-id="0ffef-129">For example, if the **TZRULE** is the effective rule, the value of the field, **TZRULE** must be "0x0002"; otherwise, it must be "0x0000".</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0ffef-130">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0ffef-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0ffef-131">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0ffef-131">Protocol specifications</span></span>

<span data-ttu-id="0ffef-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ffef-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ffef-133">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="0ffef-133">Provides property set definitions and references to related Exchange Server protocol specifications..</span></span>
    
<span data-ttu-id="0ffef-134">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ffef-134">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ffef-135">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="0ffef-135">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0ffef-136">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="0ffef-136">Header files</span></span>

<span data-ttu-id="0ffef-137">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0ffef-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="0ffef-138">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="0ffef-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0ffef-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ffef-139">See also</span></span>



[<span data-ttu-id="0ffef-140">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0ffef-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0ffef-141">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0ffef-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0ffef-142">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0ffef-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0ffef-143">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0ffef-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

