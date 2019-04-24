---
title: Kanonische Pidlidappointmenttimezonedefinitionrecur (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionRecur
api_type:
- COM
ms.assetid: 52fd57a0-9e34-4452-9ecd-2acb454446c9
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e5e9b06178a1517fc1c8652b0d667faf1afc77cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345353"
---
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a><span data-ttu-id="a3a36-103">Kanonische Pidlidappointmenttimezonedefinitionrecur (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a3a36-103">PidLidAppointmentTimeZoneDefinitionRecur Canonical Property</span></span>

  
  
<span data-ttu-id="a3a36-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3a36-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3a36-105">Enthält einen Stream, der dem beibehaltenen Format einer [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) -Struktur zugeordnet wird, in der die Beschreibung für die Zeitzone gespeichert wird, die beim Erstellen einer Terminserie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a3a36-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when a recurring appointment or meeting request is created.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a3a36-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a3a36-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a3a36-107">dispidApptTZDefRecur</span><span class="sxs-lookup"><span data-stu-id="a3a36-107">dispidApptTZDefRecur</span></span>  <br/> |
|<span data-ttu-id="a3a36-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="a3a36-108">Property set:</span></span>  <br/> |<span data-ttu-id="a3a36-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="a3a36-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="a3a36-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="a3a36-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a3a36-111">0x00008260</span><span class="sxs-lookup"><span data-stu-id="a3a36-111">0x00008260</span></span>  <br/> |
|<span data-ttu-id="a3a36-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a3a36-112">Data type:</span></span>  <br/> |<span data-ttu-id="a3a36-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a3a36-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a3a36-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a3a36-114">Area:</span></span>  <br/> |<span data-ttu-id="a3a36-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="a3a36-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a3a36-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3a36-116">Remarks</span></span>

<span data-ttu-id="a3a36-117">Versionen von Microsoft Outlook seit Microsoft Office Outlook 2007 und Lösungen auf der Grundlage von Collaboration Data Objects (CDO) 1.2.1, die das Outlook-oder Exchange Server-Kalender Aktualisierungstool ausgeführt haben, verwenden die **dispidApptTZDefRecur** und \*\* dispidTimeZoneStruct\*\* ([pidlidtimezonestruct (](pidlidtimezonestruct-canonical-property.md))-Eigenschaften, um zu bestimmen, ob die Besprechungsserie angepasst werden soll, wenn sich die Regeln der Zeitzone ändern.</span><span class="sxs-lookup"><span data-stu-id="a3a36-117">Versions of Microsoft Outlook since Microsoft Office Outlook 2007, and solutions based on Collaboration Data Objects (CDO) 1.2.1 that have run the Outlook or Exchange Server calendar update tool use the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) properties to determine whether the recurring meeting should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="a3a36-118">Diese Eigenschaften müssen synchronisiert werden, da ältere Clients die **dispidTimeZoneStruct** -Eigenschaft möglicherweise noch bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="a3a36-118">These properties must be synchronized, because older clients may still manipulate the **dispidTimeZoneStruct** property.</span></span> <span data-ttu-id="a3a36-119">Um zu überprüfen, ob die beiden Eigenschaften synchronisiert sind, sollte das **wFlags** -Element für die Regel, die mit **dispidTimeZoneStruct** übereinstimmt, das TZRULE_FLAG_RECUR_CURRENT_TZREG-Flag festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="a3a36-119">To detect whether the two properties are synchronized, the **wFlags** member for the rule that matches **dispidTimeZoneStruct** should have the TZRULE_FLAG_RECUR_CURRENT_TZREG flag set.</span></span> <span data-ttu-id="a3a36-120">Wenn dieses Flag nicht festgelegt ist oder es festgelegt ist und die Regel in der **dispidTimeZoneStruct** -Eigenschaft nicht mit der markierten Regel übereinstimmt, sollte die **dispidApptTZDefRecur** -Eigenschaft verworfen und stattdessen **dispidTimeZoneStruct** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3a36-120">If this flag is not set, or it is set and the rule in the **dispidTimeZoneStruct** property does not match the marked rule, the **dispidApptTZDefRecur** property should be discarded and **dispidTimeZoneStruct** should be used instead.</span></span> 
  
<span data-ttu-id="a3a36-121">Wenn Sie die Eigenschaften **dispidApptTZDefRecur** und **dispidTimeZoneStruct** in eine neue Besprechungsserie schreiben oder wenn Sie eine beliebige Auswahl treffen, um die **dispidTimeZoneStruct** -Eigenschaft zu verwenden, wird die aktuelle Definition für die Zeitzone ( gemäß der Windows-Registrierung) sollte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3a36-121">When you write both the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** properties to a new recurring meeting, or, when you make an arbitrary choice to use the **dispidTimeZoneStruct** property, the current definition for the time zone (according to the Windows registry) should be used.</span></span> 
  
<span data-ttu-id="a3a36-122">Ein Parser muss vorsichtig sein, wenn er einen Stream liest, der von **dispidApptTZDefRecur**abgerufen wird, oder wenn er **TZDEFINITION** in einem Stream für die Verpflichtung zu einer binären Eigenschaft wie **dispidApptTZDefRecur**.</span><span class="sxs-lookup"><span data-stu-id="a3a36-122">A parser must be careful when it reads a stream that is obtained from **dispidApptTZDefRecur**, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="a3a36-123">Weitere Informationen finden Sie unter [Informationen zum Speichern von TZDEFINITION in einem Stream, um eine binäre Eigenschaft zu über](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)nehmen.</span><span class="sxs-lookup"><span data-stu-id="a3a36-123">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
 <span data-ttu-id="a3a36-124">**dispidApptTZDefRecur** gibt Zeitzoneninformationen an, in denen das Datum und die Uhrzeit der Besprechung in einer wiederkehrenden Datenreihe in die und aus der koordiniertEn Weltzeit (UTC) konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="a3a36-124">**dispidApptTZDefRecur** specifies time zone information that describes how to convert the meeting date and time on a recurring series to and from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="a3a36-125">Wenn diese Eigenschaft festgelegt ist, aber Daten enthält, die mit den von **dispidTimeZoneStruct**dargestellten Daten inkonsistent sind, muss der Client **DispidTimeZoneStruct** anstelle von **dispidApptTZDefRecur**verwenden.</span><span class="sxs-lookup"><span data-stu-id="a3a36-125">If this property is set but it has data that is inconsistent with the data represented by **dispidTimeZoneStruct**, the client must use **dispidTimeZoneStruct** instead of **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="a3a36-126">Wenn **dispidApptTZDefRecur** nicht festgelegt ist, wird stattdessen die **pidlidtimezonestruct (** -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="a3a36-126">If **dispidApptTZDefRecur** is not set, the **PidLidTimeZoneStruct** property will be used instead.</span></span> <span data-ttu-id="a3a36-127">Die Felder in diesem BLOB werden in Little-Endian-Bytereihenfolge codiert.</span><span class="sxs-lookup"><span data-stu-id="a3a36-127">The fields in this BLOB are encoded in little-endian byte order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a3a36-128">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a3a36-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a3a36-129">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a3a36-129">Protocol specifications</span></span>

<span data-ttu-id="a3a36-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a3a36-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a3a36-131">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="a3a36-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a3a36-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a3a36-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a3a36-133">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="a3a36-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a3a36-134">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="a3a36-134">Header files</span></span>

<span data-ttu-id="a3a36-135">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a3a36-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="a3a36-136">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="a3a36-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a3a36-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3a36-137">See also</span></span>



[<span data-ttu-id="a3a36-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a3a36-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a3a36-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a3a36-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a3a36-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a3a36-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a3a36-141">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a3a36-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

