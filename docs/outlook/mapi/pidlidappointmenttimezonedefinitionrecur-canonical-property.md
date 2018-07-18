---
title: PidLidAppointmentTimeZoneDefinitionRecur (kanonische Eigenschaft)
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
ms.openlocfilehash: 5cff6ec7b39c26eec098d250688d98bf1e4799ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793460"
---
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a><span data-ttu-id="62ae0-103">PidLidAppointmentTimeZoneDefinitionRecur (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="62ae0-103">PidLidAppointmentTimeZoneDefinitionRecur Canonical Property</span></span>

  
  
<span data-ttu-id="62ae0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="62ae0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="62ae0-105">Enthält einen Datenstrom, der mit beibehaltenen Format einer Struktur [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) ist der die Beschreibung für die Zeitzone gespeichert, die verwendet wird, wenn eine Terminserie oder eine Besprechungsanfrage erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="62ae0-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when a recurring appointment or meeting request is created.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="62ae0-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="62ae0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="62ae0-107">dispidApptTZDefRecur</span><span class="sxs-lookup"><span data-stu-id="62ae0-107">dispidApptTZDefRecur</span></span>  <br/> |
|<span data-ttu-id="62ae0-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="62ae0-108">Property set:</span></span>  <br/> |<span data-ttu-id="62ae0-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="62ae0-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="62ae0-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="62ae0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="62ae0-111">0x00008260</span><span class="sxs-lookup"><span data-stu-id="62ae0-111">0x00008260</span></span>  <br/> |
|<span data-ttu-id="62ae0-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="62ae0-112">Data type:</span></span>  <br/> |<span data-ttu-id="62ae0-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="62ae0-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="62ae0-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="62ae0-114">Area:</span></span>  <br/> |<span data-ttu-id="62ae0-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="62ae0-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62ae0-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62ae0-116">Remarks</span></span>

<span data-ttu-id="62ae0-117">Versionen von Microsoft Outlook seit Microsoft Office Outlook 2007 und Lösungen basierend auf Collaboration Data Objects (CDO) 1.2.1 (engl.), die im Kalender von Outlook oder Exchange Server ausgeführt haben aktualisieren Tool verwendet die **DispidApptTZDefRecur** und ** DispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md))-Eigenschaften, um festzustellen, ob die Besprechungsserie angepasst werden soll, wenn die Regeln der Zeitzone ändern.</span><span class="sxs-lookup"><span data-stu-id="62ae0-117">Versions of Microsoft Outlook since Microsoft Office Outlook 2007, and solutions based on Collaboration Data Objects (CDO) 1.2.1 that have run the Outlook or Exchange Server calendar update tool use the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) properties to determine whether the recurring meeting should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="62ae0-118">Diese Eigenschaften müssen synchronisiert werden, weil ältere Clients die **DispidTimeZoneStruct** -Eigenschaft immer noch bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="62ae0-118">These properties must be synchronized, because older clients may still manipulate the **dispidTimeZoneStruct** property.</span></span> <span data-ttu-id="62ae0-119">Um zu ermitteln, ob die beiden Eigenschaften synchronisiert werden, sollte der **wFlags** Member für die Regel, **die dispidtimezonestruct** entspricht, die TZRULE_FLAG_RECUR_CURRENT_TZREG gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="62ae0-119">To detect whether the two properties are synchronized, the **wFlags** member for the rule that matches **dispidTimeZoneStruct** should have the TZRULE_FLAG_RECUR_CURRENT_TZREG flag set.</span></span> <span data-ttu-id="62ae0-120">Wenn dieses Flag nicht festgelegt ist, oder es wird festgelegt, und die Regel in der **DispidTimeZoneStruct** -Eigenschaft nicht der markierten Regel entspricht, die **DispidApptTZDefRecur** -Eigenschaft verworfen werden muss und **DispidTimeZoneStruct** stattdessen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="62ae0-120">If this flag is not set, or it is set and the rule in the **dispidTimeZoneStruct** property does not match the marked rule, the **dispidApptTZDefRecur** property should be discarded and **dispidTimeZoneStruct** should be used instead.</span></span> 
  
<span data-ttu-id="62ae0-121">Beim Schreiben der **DispidApptTZDefRecur** und die **DispidTimeZoneStruct** -Eigenschaft um eine neue Besprechungsserie oder, wenn Sie eine beliebige Auswahl mit der **DispidTimeZoneStruct** -Eigenschaft, die aktuelle Definition für die Zeitzone (treffen gemäß die Windows-Registrierung) sollte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="62ae0-121">When you write both the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** properties to a new recurring meeting, or, when you make an arbitrary choice to use the **dispidTimeZoneStruct** property, the current definition for the time zone (according to the Windows registry) should be used.</span></span> 
  
<span data-ttu-id="62ae0-122">Ein Parser wird beim Lesen eines Stream-Objekts, das aus **DispidApptTZDefRecur**abgerufen wird, oder wenn er in ein Stream-Objekt für eine binäre Eigenschaft wie **DispidApptTZDefRecur**Engagement **TZDEFINITION** beibehalten.</span><span class="sxs-lookup"><span data-stu-id="62ae0-122">A parser must be careful when it reads a stream that is obtained from **dispidApptTZDefRecur**, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="62ae0-123">Weitere Informationen finden Sie unter [Speichern von TZDEFINITION in ein Stream-Objekt an eine binäre Eigenschaft übermittelt werden](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="62ae0-123">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
 <span data-ttu-id="62ae0-124">**DispidApptTZDefRecur** gibt die Informationen zur Zeitzone, die Beschreibung der Vorgehensweise die Besprechungsdatum und Uhrzeit auf einer Terminserie und von koordinierte Weltzeit (UTC) zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="62ae0-124">**dispidApptTZDefRecur** specifies time zone information that describes how to convert the meeting date and time on a recurring series to and from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="62ae0-125">Wenn diese Eigenschaft wird festgelegt, aber es die Daten, die mit den Daten dargestellt durch **DispidTimeZoneStruct**inkonsistente hat, muss der Client **DispidTimeZoneStruct** anstelle von **DispidApptTZDefRecur**verwenden.</span><span class="sxs-lookup"><span data-stu-id="62ae0-125">If this property is set but it has data that is inconsistent with the data represented by **dispidTimeZoneStruct**, the client must use **dispidTimeZoneStruct** instead of **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="62ae0-126">Wenn **DispidApptTZDefRecur** nicht festgelegt ist, wird stattdessen die **PidLidTimeZoneStruct** -Eigenschaft verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="62ae0-126">If **dispidApptTZDefRecur** is not set, the **PidLidTimeZoneStruct** property will be used instead.</span></span> <span data-ttu-id="62ae0-127">Die Felder in dieser BLOB werden in little-Endian-Bytereihenfolge codiert.</span><span class="sxs-lookup"><span data-stu-id="62ae0-127">The fields in this BLOB are encoded in little-endian byte order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="62ae0-128">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="62ae0-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="62ae0-129">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="62ae0-129">Protocol specifications</span></span>

<span data-ttu-id="62ae0-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62ae0-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62ae0-131">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="62ae0-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="62ae0-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62ae0-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62ae0-133">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="62ae0-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="62ae0-134">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="62ae0-134">Header files</span></span>

<span data-ttu-id="62ae0-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="62ae0-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="62ae0-136">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="62ae0-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="62ae0-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62ae0-137">See also</span></span>



[<span data-ttu-id="62ae0-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="62ae0-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="62ae0-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="62ae0-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="62ae0-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="62ae0-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="62ae0-141">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="62ae0-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

