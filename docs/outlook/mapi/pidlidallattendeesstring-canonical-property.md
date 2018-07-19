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
ms.openlocfilehash: a9580428cd985902d3af6320dd754947565b74e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793345"
---
# <a name="pidlidallattendeesstring-canonical-property"></a><span data-ttu-id="589fd-103">PidLidAllAttendeesString (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="589fd-103">PidLidAllAttendeesString Canonical Property</span></span>

  
  
<span data-ttu-id="589fd-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="589fd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="589fd-105">Gibt eine Liste aller Teilnehmer außer dem Organisator, einschließlich Ressourcen und Teilnehmer zu senden.</span><span class="sxs-lookup"><span data-stu-id="589fd-105">Specifies a list of all the attendees except for the organizer, including resources and unsendable attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="589fd-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="589fd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="589fd-107">dispidAllAttendeesString</span><span class="sxs-lookup"><span data-stu-id="589fd-107">dispidAllAttendeesString</span></span>  <br/> |
|<span data-ttu-id="589fd-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="589fd-108">Property set:</span></span>  <br/> |<span data-ttu-id="589fd-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="589fd-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="589fd-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="589fd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="589fd-111">0x00008238</span><span class="sxs-lookup"><span data-stu-id="589fd-111">0x00008238</span></span>  <br/> |
|<span data-ttu-id="589fd-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="589fd-112">Data type:</span></span>  <br/> |<span data-ttu-id="589fd-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="589fd-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="589fd-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="589fd-114">Area:</span></span>  <br/> |<span data-ttu-id="589fd-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="589fd-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="589fd-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="589fd-116">Remarks</span></span>

<span data-ttu-id="589fd-117">Der Wert für jeden Teilnehmer ist Anzeigename den Namen des Teilnehmers.</span><span class="sxs-lookup"><span data-stu-id="589fd-117">The value for each attendee is the attendee's display name.</span></span> <span data-ttu-id="589fd-118">Separate Einträge müssen durch ein Semikolon, gefolgt von einem Leerzeichen getrennt sein.</span><span class="sxs-lookup"><span data-stu-id="589fd-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="589fd-119">Diese Eigenschaft ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="589fd-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="589fd-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="589fd-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="589fd-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="589fd-121">Protocol specifications</span></span>

<span data-ttu-id="589fd-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="589fd-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="589fd-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="589fd-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="589fd-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="589fd-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="589fd-125">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="589fd-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="589fd-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="589fd-126">Header files</span></span>

<span data-ttu-id="589fd-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="589fd-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="589fd-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="589fd-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="589fd-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="589fd-129">See also</span></span>



[<span data-ttu-id="589fd-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="589fd-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="589fd-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="589fd-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="589fd-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="589fd-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="589fd-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="589fd-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

