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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e5e9b06178a1517fc1c8652b0d667faf1afc77cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345353"
---
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a><span data-ttu-id="1c363-103">PidLidAppointmentTimeZoneDefinitionRecur (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1c363-103">PidLidAppointmentTimeZoneDefinitionRecur Canonical Property</span></span>

  
  
<span data-ttu-id="1c363-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c363-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c363-105">Enthält einen Datenstrom, der dem dauerhaften Format einer [TZDEFINITION-Struktur](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) zu ordnet, in der die Beschreibung für die Zeitzone gespeichert wird, die beim Erstellen eines Termins oder einer Besprechungsserie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1c363-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when a recurring appointment or meeting request is created.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1c363-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1c363-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1c363-107">dispidApptTZDefRecur</span><span class="sxs-lookup"><span data-stu-id="1c363-107">dispidApptTZDefRecur</span></span>  <br/> |
|<span data-ttu-id="1c363-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="1c363-108">Property set:</span></span>  <br/> |<span data-ttu-id="1c363-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="1c363-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="1c363-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="1c363-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1c363-111">0x00008260</span><span class="sxs-lookup"><span data-stu-id="1c363-111">0x00008260</span></span>  <br/> |
|<span data-ttu-id="1c363-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1c363-112">Data type:</span></span>  <br/> |<span data-ttu-id="1c363-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1c363-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1c363-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1c363-114">Area:</span></span>  <br/> |<span data-ttu-id="1c363-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="1c363-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c363-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1c363-116">Remarks</span></span>

<span data-ttu-id="1c363-117">Versionen von Microsoft Outlook seit Microsoft Office Outlook 2007 und Lösungen, die auf den Eigenschaften Collaboration Data Objects (CDO) 1.2.1 basieren, die das Kalenderupdatetool Outlook oder Exchange Server ausgeführt haben, verwenden die **Eigenschaften dispidApptTZDefRecur** und **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)), um zu bestimmen, ob die Besprechungsserie angepasst werden soll, wenn sich die Regeln der Zeitzone ändern.</span><span class="sxs-lookup"><span data-stu-id="1c363-117">Versions of Microsoft Outlook since Microsoft Office Outlook 2007, and solutions based on Collaboration Data Objects (CDO) 1.2.1 that have run the Outlook or Exchange Server calendar update tool use the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) properties to determine whether the recurring meeting should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="1c363-118">Diese Eigenschaften müssen synchronisiert werden, da ältere Clients möglicherweise weiterhin die **dispidTimeZoneStruct-Eigenschaft** bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="1c363-118">These properties must be synchronized, because older clients may still manipulate the **dispidTimeZoneStruct** property.</span></span> <span data-ttu-id="1c363-119">Um zu ermitteln, ob die beiden Eigenschaften synchronisiert sind, sollte das **wFlags-Element** für die Regel, die **dispidTimeZoneStruct** entspricht, über TZRULE_FLAG_RECUR_CURRENT_TZREG verfügen.</span><span class="sxs-lookup"><span data-stu-id="1c363-119">To detect whether the two properties are synchronized, the **wFlags** member for the rule that matches **dispidTimeZoneStruct** should have the TZRULE_FLAG_RECUR_CURRENT_TZREG flag set.</span></span> <span data-ttu-id="1c363-120">Wenn dieses Flag nicht festgelegt oder festgelegt ist und die Regel in der **dispidTimeZoneStruct-Eigenschaft** nicht mit der markierten Regel übereinstimmen, sollte die **dispidApptTZDefRecur-Eigenschaft** verworfen und **stattdessen dispidTimeZoneStruct** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1c363-120">If this flag is not set, or it is set and the rule in the **dispidTimeZoneStruct** property does not match the marked rule, the **dispidApptTZDefRecur** property should be discarded and **dispidTimeZoneStruct** should be used instead.</span></span> 
  
<span data-ttu-id="1c363-121">Wenn Sie die Eigenschaften **dispidApptTZDefRecur** und **dispidTimeZoneStruct** in eine neue Besprechungsserie schreiben, oder wenn Sie eine beliebige Entscheidung für die Verwendung der **dispidTimeZoneStruct-Eigenschaft** treffen, sollte die aktuelle Definition für die Zeitzone (gemäß der Windows-Registrierung) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1c363-121">When you write both the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** properties to a new recurring meeting, or, when you make an arbitrary choice to use the **dispidTimeZoneStruct** property, the current definition for the time zone (according to the Windows registry) should be used.</span></span> 
  
<span data-ttu-id="1c363-122">Ein Parser muss vorsichtig sein, wenn er einen Datenstrom liest, der von **dispidApptTZDefRecur** erhalten wird, oder wenn **er TZDEFINITION** in einem Datenstrom für die Verpflichtung zu einer binären Eigenschaft wie **dispidApptTZDefRecur** beibehalten.</span><span class="sxs-lookup"><span data-stu-id="1c363-122">A parser must be careful when it reads a stream that is obtained from **dispidApptTZDefRecur**, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="1c363-123">Weitere Informationen finden Sie unter [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="1c363-123">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
 <span data-ttu-id="1c363-124">**dispidApptTZDefRecur** gibt Zeitzoneninformationen an, die beschreiben, wie Das Datum und die Uhrzeit der Besprechung in einer Serie in koordinierte Weltzeit (Coordinated Universal Time, UTC) konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="1c363-124">**dispidApptTZDefRecur** specifies time zone information that describes how to convert the meeting date and time on a recurring series to and from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="1c363-125">Wenn diese Eigenschaft festgelegt ist, aber Daten enthält, die mit den durch **dispidTimeZoneStruct** dargestellten Daten inkonsistent sind, muss der Client **dispidTimeZoneStruct** anstelle von **dispidApptTZDefRecur verwenden.**</span><span class="sxs-lookup"><span data-stu-id="1c363-125">If this property is set but it has data that is inconsistent with the data represented by **dispidTimeZoneStruct**, the client must use **dispidTimeZoneStruct** instead of **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="1c363-126">Wenn **dispidApptTZDefRecur** nicht festgelegt ist, wird stattdessen die **PidLidTimeZoneStruct-Eigenschaft** verwendet.</span><span class="sxs-lookup"><span data-stu-id="1c363-126">If **dispidApptTZDefRecur** is not set, the **PidLidTimeZoneStruct** property will be used instead.</span></span> <span data-ttu-id="1c363-127">Die Felder in diesem BLOB werden in klein-endischer Bytereihenfolge codiert.</span><span class="sxs-lookup"><span data-stu-id="1c363-127">The fields in this BLOB are encoded in little-endian byte order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1c363-128">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1c363-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1c363-129">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="1c363-129">Protocol specifications</span></span>

<span data-ttu-id="1c363-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c363-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c363-131">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="1c363-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1c363-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c363-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c363-133">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="1c363-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1c363-134">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="1c363-134">Header files</span></span>

<span data-ttu-id="1c363-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1c363-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="1c363-136">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1c363-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1c363-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c363-137">See also</span></span>



[<span data-ttu-id="1c363-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1c363-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1c363-139">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="1c363-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1c363-140">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1c363-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1c363-141">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1c363-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

