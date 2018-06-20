---
title: Kanonische PidLidCcAttendeesString-Eigenschaft
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
ms.openlocfilehash: bb24d17e478de6b428750efb8d61797c8628b16d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793473"
---
# <a name="pidlidccattendeesstring-canonical-property"></a><span data-ttu-id="0ef8e-103">Kanonische PidLidCcAttendeesString-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0ef8e-103">PidLidCcAttendeesString Canonical Property</span></span>

  
  
<span data-ttu-id="0ef8e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0ef8e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0ef8e-105">Enthält eine Liste aller sendable Teilnehmer, die auch die optionale Teilnehmer sind.</span><span class="sxs-lookup"><span data-stu-id="0ef8e-105">Contains a list of all the sendable attendees who are also optional attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0ef8e-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0ef8e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0ef8e-107">dispidCCAttendeesString</span><span class="sxs-lookup"><span data-stu-id="0ef8e-107">dispidCCAttendeesString</span></span>  <br/> |
|<span data-ttu-id="0ef8e-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="0ef8e-108">Property set:</span></span>  <br/> |<span data-ttu-id="0ef8e-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="0ef8e-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="0ef8e-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="0ef8e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0ef8e-111">0x0000823C</span><span class="sxs-lookup"><span data-stu-id="0ef8e-111">0x0000823C</span></span>  <br/> |
|<span data-ttu-id="0ef8e-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0ef8e-112">Data type:</span></span>  <br/> |<span data-ttu-id="0ef8e-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0ef8e-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0ef8e-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0ef8e-114">Area:</span></span>  <br/> |<span data-ttu-id="0ef8e-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="0ef8e-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ef8e-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0ef8e-116">Remarks</span></span>

<span data-ttu-id="0ef8e-117">Der Wert für jeden Teilnehmer ist die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft des Adressbuchs des Teilnehmers.</span><span class="sxs-lookup"><span data-stu-id="0ef8e-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's address book.</span></span> <span data-ttu-id="0ef8e-118">Separate Einträge müssen durch ein Semikolon, gefolgt von einem Leerzeichen getrennt sein.</span><span class="sxs-lookup"><span data-stu-id="0ef8e-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="0ef8e-119">Diese Eigenschaft ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0ef8e-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0ef8e-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0ef8e-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0ef8e-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0ef8e-121">Protocol specifications</span></span>

<span data-ttu-id="0ef8e-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ef8e-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ef8e-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="0ef8e-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0ef8e-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ef8e-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ef8e-125">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="0ef8e-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="0ef8e-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ef8e-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ef8e-127">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="0ef8e-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0ef8e-128">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="0ef8e-128">Header files</span></span>

<span data-ttu-id="0ef8e-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0ef8e-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="0ef8e-130">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0ef8e-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0ef8e-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ef8e-131">See also</span></span>



[<span data-ttu-id="0ef8e-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0ef8e-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0ef8e-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0ef8e-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0ef8e-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0ef8e-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0ef8e-135">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0ef8e-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

