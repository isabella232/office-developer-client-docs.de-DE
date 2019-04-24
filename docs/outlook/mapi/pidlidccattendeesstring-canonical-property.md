---
title: Kanonische Pidlidccattendeesstring (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCcAttendeesString
api_type:
- COM
ms.assetid: 697d5c93-ec7f-4608-9866-9e249a093dbc
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 12cdbfcc140fb5ea3bb15a2db93f3689923d9390
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344968"
---
# <a name="pidlidccattendeesstring-canonical-property"></a><span data-ttu-id="18543-103">Kanonische Pidlidccattendeesstring (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="18543-103">PidLidCcAttendeesString Canonical Property</span></span>

  
  
<span data-ttu-id="18543-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18543-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18543-105">Enthält eine Liste aller sendenden Teilnehmer, die ebenfalls optionale Teilnehmer sind.</span><span class="sxs-lookup"><span data-stu-id="18543-105">Contains a list of all the sendable attendees who are also optional attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="18543-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="18543-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="18543-107">dispidCCAttendeesString</span><span class="sxs-lookup"><span data-stu-id="18543-107">dispidCCAttendeesString</span></span>  <br/> |
|<span data-ttu-id="18543-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="18543-108">Property set:</span></span>  <br/> |<span data-ttu-id="18543-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="18543-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="18543-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="18543-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="18543-111">0x0000823C</span><span class="sxs-lookup"><span data-stu-id="18543-111">0x0000823C</span></span>  <br/> |
|<span data-ttu-id="18543-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="18543-112">Data type:</span></span>  <br/> |<span data-ttu-id="18543-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="18543-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="18543-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="18543-114">Area:</span></span>  <br/> |<span data-ttu-id="18543-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="18543-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18543-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18543-116">Remarks</span></span>

<span data-ttu-id="18543-117">Der Wert für jeden Teilnehmer ist die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft des Adressbuchs des Teilnehmers.</span><span class="sxs-lookup"><span data-stu-id="18543-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's address book.</span></span> <span data-ttu-id="18543-118">Separate Einträge müssen durch ein Semikolon, gefolgt von einem Leerzeichen, getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="18543-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="18543-119">Diese Eigenschaft ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="18543-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="18543-120">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="18543-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="18543-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="18543-121">Protocol specifications</span></span>

<span data-ttu-id="18543-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18543-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18543-123">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="18543-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="18543-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18543-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18543-125">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="18543-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="18543-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18543-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18543-127">Konvertiert zwischen IETF-RFC2445, RFC2446 und RFC2447 sowie Termin-und Besprechungs Objekten.</span><span class="sxs-lookup"><span data-stu-id="18543-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="18543-128">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="18543-128">Header files</span></span>

<span data-ttu-id="18543-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="18543-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="18543-130">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="18543-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="18543-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18543-131">See also</span></span>



[<span data-ttu-id="18543-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18543-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="18543-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18543-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="18543-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="18543-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="18543-135">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="18543-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

