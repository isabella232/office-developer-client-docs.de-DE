---
title: Kanonische pidlidappointmenttimezonedefinitionenddisplay (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionEndDisplay
api_type:
- COM
ms.assetid: 7b6193cb-612b-408e-b9bc-285df313e2cc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 24ccd25a1d799f3146bd230e5156be0051104f47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345381"
---
# <a name="pidlidappointmenttimezonedefinitionenddisplay-canonical-property"></a><span data-ttu-id="edc5c-103">Kanonische pidlidappointmenttimezonedefinitionenddisplay (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="edc5c-103">PidLidAppointmentTimeZoneDefinitionEndDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="edc5c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="edc5c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="edc5c-105">Enthält einen Datenstrom, der dem beibehaltenen Format einer [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) -Struktur zugeordnet wird, in der die Beschreibung für die Zeitzone gespeichert wird, die verwendet wird, wenn die Endzeit eines Einzelinstanz-Termins oder einer Besprechungsanfrage ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="edc5c-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when the end time of a single-instance appointment or meeting request is selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="edc5c-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="edc5c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="edc5c-107">dispidApptTZDefEndDisplay</span><span class="sxs-lookup"><span data-stu-id="edc5c-107">dispidApptTZDefEndDisplay</span></span>  <br/> |
|<span data-ttu-id="edc5c-108">Eigenschaftengruppe:</span><span class="sxs-lookup"><span data-stu-id="edc5c-108">Property set:</span></span>  <br/> |<span data-ttu-id="edc5c-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="edc5c-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="edc5c-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="edc5c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="edc5c-111">0x0000825F</span><span class="sxs-lookup"><span data-stu-id="edc5c-111">0x0000825F</span></span>  <br/> |
|<span data-ttu-id="edc5c-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="edc5c-112">Data type:</span></span>  <br/> |<span data-ttu-id="edc5c-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="edc5c-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="edc5c-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="edc5c-114">Area:</span></span>  <br/> |<span data-ttu-id="edc5c-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="edc5c-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="edc5c-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="edc5c-116">Remarks</span></span>

<span data-ttu-id="edc5c-117">Microsoft Office Outlook 2003 oder früher und Lösungen, die auf Zusammenarbeits Datenobjekten (CDO) 1.2.1 basieren und das Tool zum Aktualisieren von Kalendern für Outlook oder Exchange Server nicht ausgeführt haben, speichern Sie die Startzeit und die Endzeit der einzelnen Instanzen. Termine und Besprechungsanfragen in koordinierter Weltzeit (Coordinated Universal Time, UTC).</span><span class="sxs-lookup"><span data-stu-id="edc5c-117">Microsoft Office Outlook 2003 or earlier, and solutions that are based on Collaboration Data Objects (CDO) 1.2.1 and that have not run the calendar update tool for Outlook or Microsoft Exchange Server, store the start time and end time of single-instance appointments and meeting requests in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="edc5c-118">Diese Clients speichern keine Informationen für die Zeitzone, in der der Termin oder die Besprechungsanfrage erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="edc5c-118">These clients do not store any information for the time zone where the appointment or meeting request is created.</span></span>
  
<span data-ttu-id="edc5c-119">Versionen von Microsoft Outlook seit Microsoft Office Outlook 2007 und auf CDO 1.2.1 basierende Lösungen, die das Outlook-oder Exchange Server-Kalender Update Tool ausgeführt haben, verwenden **dispidApptTZDefEndDisplay** zum Speichern der Zeitzone für die Endzeit.</span><span class="sxs-lookup"><span data-stu-id="edc5c-119">Versions of Microsoft Outlook since Microsoft Office Outlook 2007, and solutions based on CDO 1.2.1 that have run the Outlook or Exchange Server calendar update tool use **dispidApptTZDefEndDisplay** to store the time zone for the end time.</span></span> <span data-ttu-id="edc5c-120">**dispidApptTZDefEndDisplay** zeigt den Termin oder die Besprechung in der ursprünglichen Zeitzone an, die geplant wurde, und legt fest, ob die Endzeit angepasst werden soll, wenn sich die Regeln der Zeitzone ändern.</span><span class="sxs-lookup"><span data-stu-id="edc5c-120">**dispidApptTZDefEndDisplay** shows the appointment or meeting in the original time zone that it was scheduled, and determines whether the end time should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="edc5c-121">Wenn diese Eigenschaft nicht vorhanden ist, wird die von der **dispidApptTZDefStartDisplay** -Eigenschaft ([pidlidappointmenttimezonedefinitionstartdisplay (](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) angegebene Zeitzone verwendet.</span><span class="sxs-lookup"><span data-stu-id="edc5c-121">If this property is missing, the time zone specified by the **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) property is used.</span></span> <span data-ttu-id="edc5c-122">Wenn **dispidApptTZDefStartDisplay** fehlt oder ungültig ist, wird die aktuelle lokale Zeitzone angenommen.</span><span class="sxs-lookup"><span data-stu-id="edc5c-122">If **dispidApptTZDefStartDisplay** is missing or invalid, the current local time zone is assumed.</span></span> <span data-ttu-id="edc5c-123">**dispidApptTZDefEndDisplay** wird nur für Anzeigezwecke verwendet und nicht in der Serienerweiterung verwendet.</span><span class="sxs-lookup"><span data-stu-id="edc5c-123">**dispidApptTZDefEndDisplay** is used for display purposes only and is not used in recurrence expansion.</span></span> 
  
<span data-ttu-id="edc5c-124">Ein Parser muss vorsichtig sein, wenn er einen aus **dispidApptTZDefEndDisplay**abgerufenen Stream liest oder wenn er **TZDEFINITION** in einem Stream zur Bindung an eine binäre Eigenschaft wie **dispidApptTZDefEndDisplay**beibehält.</span><span class="sxs-lookup"><span data-stu-id="edc5c-124">A parser must be careful when it reads a stream obtained from **dispidApptTZDefEndDisplay**, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefEndDisplay**.</span></span> <span data-ttu-id="edc5c-125">Weitere Informationen finden Sie unter [about persistent TZDEFINITION to a Stream to Commit to a binary Property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="edc5c-125">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
 <span data-ttu-id="edc5c-126">**dispidApptTZDefEndDisplay** gibt Zeitzoneninformationen für die **dispidApptEndWhole** ([pidlidappointmentendwhole (](pidlidappointmentendwhole-canonical-property.md))-Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="edc5c-126">**dispidApptTZDefEndDisplay** specifies time zone information for the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="edc5c-127">Das Format, die Einschränkungen und die Berechnung von **dispidApptTZDefEndDisplay** entsprechen den Angaben in der **dispidApptTZDefStartDisplay** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="edc5c-127">The format, constraints, and computation of **dispidApptTZDefEndDisplay** are the same as specified in the **dispidApptTZDefStartDisplay** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="edc5c-128">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="edc5c-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="edc5c-129">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="edc5c-129">Protocol specifications</span></span>

<span data-ttu-id="edc5c-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edc5c-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edc5c-131">Stellt Eigenschaftenmengen Definitionen und Verweise auf zugehörige Exchange Server Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="edc5c-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="edc5c-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edc5c-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edc5c-133">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungsanfrage-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="edc5c-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="edc5c-134">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="edc5c-134">Header files</span></span>

<span data-ttu-id="edc5c-135">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="edc5c-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="edc5c-136">Stellt Definitionen von Datentypen bereit.</span><span class="sxs-lookup"><span data-stu-id="edc5c-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="edc5c-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="edc5c-137">See also</span></span>



[<span data-ttu-id="edc5c-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="edc5c-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="edc5c-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="edc5c-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="edc5c-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="edc5c-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="edc5c-141">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="edc5c-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

