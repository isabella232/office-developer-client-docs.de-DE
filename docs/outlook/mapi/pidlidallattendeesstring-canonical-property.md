---
title: PidLidAllAttendeesString (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAllAttendeesString
api_type:
- COM
ms.assetid: 2ffc0609-341d-4e35-8f53-ed3096c6fa7f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 96ad0727797475effd0563e4753070cb3bac4b37
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334776"
---
# <a name="pidlidallattendeesstring-canonical-property"></a><span data-ttu-id="51cf1-103">PidLidAllAttendeesString (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="51cf1-103">PidLidAllAttendeesString Canonical Property</span></span>

  
  
<span data-ttu-id="51cf1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51cf1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51cf1-105">Gibt eine Liste aller Teilnehmer mit Ausnahme des Organisators an, einschließlich Ressourcen und nicht zu unterschätzenden Teilnehmern.</span><span class="sxs-lookup"><span data-stu-id="51cf1-105">Specifies a list of all the attendees except for the organizer, including resources and unsendable attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="51cf1-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="51cf1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="51cf1-107">dispidAllAttendeesString</span><span class="sxs-lookup"><span data-stu-id="51cf1-107">dispidAllAttendeesString</span></span>  <br/> |
|<span data-ttu-id="51cf1-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="51cf1-108">Property set:</span></span>  <br/> |<span data-ttu-id="51cf1-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="51cf1-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="51cf1-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="51cf1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="51cf1-111">0x00008238</span><span class="sxs-lookup"><span data-stu-id="51cf1-111">0x00008238</span></span>  <br/> |
|<span data-ttu-id="51cf1-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="51cf1-112">Data type:</span></span>  <br/> |<span data-ttu-id="51cf1-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="51cf1-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="51cf1-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="51cf1-114">Area:</span></span>  <br/> |<span data-ttu-id="51cf1-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="51cf1-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51cf1-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="51cf1-116">Remarks</span></span>

<span data-ttu-id="51cf1-117">Der Wert für jeden Teilnehmer ist der Anzeigename des Teilnehmers.</span><span class="sxs-lookup"><span data-stu-id="51cf1-117">The value for each attendee is the attendee's display name.</span></span> <span data-ttu-id="51cf1-118">Separate Einträge müssen durch ein Semikolon gefolgt von einem Leerzeichen getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="51cf1-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="51cf1-119">Diese Eigenschaft ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="51cf1-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="51cf1-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="51cf1-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="51cf1-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="51cf1-121">Protocol specifications</span></span>

<span data-ttu-id="51cf1-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51cf1-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51cf1-123">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="51cf1-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="51cf1-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51cf1-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51cf1-125">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="51cf1-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="51cf1-126">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="51cf1-126">Header files</span></span>

<span data-ttu-id="51cf1-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="51cf1-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="51cf1-128">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="51cf1-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="51cf1-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51cf1-129">See also</span></span>



[<span data-ttu-id="51cf1-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51cf1-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="51cf1-131">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="51cf1-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="51cf1-132">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="51cf1-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="51cf1-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="51cf1-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

