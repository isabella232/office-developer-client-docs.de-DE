---
title: PidLidAppointmentTimeZoneDefinitionStartDisplay (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6ca53633f0c1e5b226f7e03c8ee702d4cda7d115
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586795"
---
# <a name="pidlidappointmenttimezonedefinitionstartdisplay-canonical-property"></a><span data-ttu-id="e9d79-103">PidLidAppointmentTimeZoneDefinitionStartDisplay (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e9d79-103">PidLidAppointmentTimeZoneDefinitionStartDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="e9d79-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9d79-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9d79-105">Enthält einen Datenstrom, der mit beibehaltenen Format einer Struktur [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) ist der die Beschreibung für die Zeitzone gespeichert, die verwendet wird, wenn die Anfangszeit der eine Einzelinstanz-Termin oder eine Besprechungsanfrage ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="e9d79-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when the start time of a single-instance appointment or meeting request is selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e9d79-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e9d79-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e9d79-107">dispidApptTZDefStartDisplay</span><span class="sxs-lookup"><span data-stu-id="e9d79-107">dispidApptTZDefStartDisplay</span></span>  <br/> |
|<span data-ttu-id="e9d79-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="e9d79-108">Property set:</span></span>  <br/> |<span data-ttu-id="e9d79-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="e9d79-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="e9d79-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="e9d79-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e9d79-111">0x0000825E</span><span class="sxs-lookup"><span data-stu-id="e9d79-111">0x0000825E</span></span>  <br/> |
|<span data-ttu-id="e9d79-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e9d79-112">Data type:</span></span>  <br/> |<span data-ttu-id="e9d79-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e9d79-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e9d79-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e9d79-114">Area:</span></span>  <br/> |<span data-ttu-id="e9d79-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="e9d79-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9d79-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="e9d79-116">Remarks</span></span>

<span data-ttu-id="e9d79-117">Microsoft Office Outlook 2003 oder früher und Lösungen, basieren auf Collaboration Data Objects (CDO) 1.2.1 und, die das Calendar Update-Tool nicht für Microsoft Outlook und Microsoft Exchange Server ausgeführt haben, Speichern der Start- und Endzeit der Einzel-Instanz Termine und Besprechungsanfragen in koordinierter Weltzeit (UTC).</span><span class="sxs-lookup"><span data-stu-id="e9d79-117">Microsoft Office Outlook 2003 or earlier, and solutions that are based on Collaboration Data Objects (CDO) 1.2.1 and that have not run the calendar update tool for Outlook or Microsoft Exchange Server, store the start time and end time of single-instance appointments and meeting requests in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="e9d79-118">Diese Clients speichern keine Informationen für die Zeitzone in denen die Termin- oder Besprechungsanfragen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e9d79-118">These clients do not store any information for the time zone in which the appointment or meeting request is created.</span></span>
  
<span data-ttu-id="e9d79-119">Versionen von Outlook im Vergleich zu Microsoft Office Outlook 2007 und CDO 1.2.1-basierter Lösungen, die Outlook oder Exchange Server-Update Kalendertools ausgeführt haben mit dieser Eigenschaft können Sie um die Zeitzone für die Startzeit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="e9d79-119">Versions of Outlook since Microsoft Office Outlook 2007, and solutions based on CDO 1.2.1 that have run the Outlook or Exchange Server calendar update tool use this property to store the time zone for the start time.</span></span> <span data-ttu-id="e9d79-120">Die **DispidApptTZDefStartDisplay** -Eigenschaft zeigt, dass es geplant wurde Termin oder eine Besprechung in der ursprünglichen Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="e9d79-120">The **dispidApptTZDefStartDisplay** property shows the appointment or meeting in the original time zone that it was scheduled.</span></span> <span data-ttu-id="e9d79-121">Bestimmt, ob die Startzeit angepasst werden sollten, wenn die Regeln der Zeitzone ändern.</span><span class="sxs-lookup"><span data-stu-id="e9d79-121">It determines whether the start time should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="e9d79-122">Wenn diese Eigenschaft nicht vorhanden ist, wird davon ausgegangen, dass die aktuelle lokale Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="e9d79-122">If this property is missing, the current local time zone is assumed.</span></span> <span data-ttu-id="e9d79-123">Diese Eigenschaft wird nur für die Anzeige verwendet und ist nicht in Serie Erweiterung verwendet.</span><span class="sxs-lookup"><span data-stu-id="e9d79-123">This property is used for display purposes only and is not used in recurrence expansion.</span></span> 
  
<span data-ttu-id="e9d79-124">Ein Parser wird beim Lesen eines Streams von dieser Eigenschaft abgerufen oder wenn er in ein Stream-Objekt für eine binäre Eigenschaft wie **DispidApptTZDefStartDisplay**Engagement **TZDEFINITION** beibehalten.</span><span class="sxs-lookup"><span data-stu-id="e9d79-124">A parser must be careful when it reads a stream obtained from this property, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefStartDisplay**.</span></span> <span data-ttu-id="e9d79-125">Weitere Informationen finden Sie unter [Speichern von TZDEFINITION in ein Stream-Objekt an eine binäre Eigenschaft übermittelt werden](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e9d79-125">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="e9d79-126">Diese Eigenschaft gibt die Informationen zur Zeitzone für die Eigenschaft **DispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e9d79-126">This property specifies time zone information for the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="e9d79-127">Der Wert der **DispidApptTZDefStartDisplay** wird verwendet, um das Startdatum und die Uhrzeit aus UTC in die lokale Zeitzone für die Anzeige zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="e9d79-127">The value of **dispidApptTZDefStartDisplay** is used to convert the start date and time from UTC to the local time zone for display purposes.</span></span> <span data-ttu-id="e9d79-128">Für jede **TZRULE** von dieser Eigenschaft angegeben wird muss das Flag TZRULE_FLAG_RECUR_CURRENT_TZREG nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e9d79-128">For each **TZRULE** specified by this property, the TZRULE_FLAG_RECUR_CURRENT_TZREG flag must not be set.</span></span> <span data-ttu-id="e9d79-129">Beispielsweise ist der **TZRULE** die effektive Regel, muss der Wert des Felds, **TZRULE** "0 x 0002"; werden Andernfalls müssen sie "0 x 0000" sein.</span><span class="sxs-lookup"><span data-stu-id="e9d79-129">For example, if the **TZRULE** is the effective rule, the value of the field, **TZRULE** must be "0x0002"; otherwise, it must be "0x0000".</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e9d79-130">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e9d79-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e9d79-131">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e9d79-131">Protocol specifications</span></span>

<span data-ttu-id="e9d79-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9d79-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9d79-133">Bietet Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e9d79-133">Provides property set definitions and references to related Exchange Server protocol specifications..</span></span>
    
<span data-ttu-id="e9d79-134">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9d79-134">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9d79-135">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="e9d79-135">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e9d79-136">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="e9d79-136">Header files</span></span>

<span data-ttu-id="e9d79-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e9d79-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="e9d79-138">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e9d79-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e9d79-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9d79-139">See also</span></span>



[<span data-ttu-id="e9d79-140">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e9d79-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e9d79-141">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e9d79-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e9d79-142">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e9d79-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e9d79-143">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e9d79-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

