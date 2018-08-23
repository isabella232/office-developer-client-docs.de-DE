---
title: PidTagOwnerAppointmentId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOwnerAppointmentId
api_type:
- COM
ms.assetid: b5eea554-6bca-42d1-b943-1327f0d70584
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 954e6fdf2f306f5a49e2d32e191c41f146ef5997
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573019"
---
# <a name="pidtagownerappointmentid-canonical-property"></a><span data-ttu-id="743e1-103">PidTagOwnerAppointmentId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="743e1-103">PidTagOwnerAppointmentId Canonical Property</span></span>

  
  
<span data-ttu-id="743e1-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="743e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="743e1-105">Enthält einen Bezeichner für einen Termin in den Besitzer Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="743e1-105">Contains an identifier for an appointment in the owner's schedule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="743e1-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="743e1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="743e1-107">PR_OWNER_APPT_ID</span><span class="sxs-lookup"><span data-stu-id="743e1-107">PR_OWNER_APPT_ID</span></span>  <br/> |
|<span data-ttu-id="743e1-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="743e1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="743e1-109">0x0062</span><span class="sxs-lookup"><span data-stu-id="743e1-109">0x0062</span></span>  <br/> |
|<span data-ttu-id="743e1-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="743e1-110">Data type:</span></span>  <br/> |<span data-ttu-id="743e1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="743e1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="743e1-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="743e1-112">Area:</span></span>  <br/> |<span data-ttu-id="743e1-113">Termin</span><span class="sxs-lookup"><span data-stu-id="743e1-113">Appointment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="743e1-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="743e1-114">Remarks</span></span>

<span data-ttu-id="743e1-115">Diese Eigenschaft wird in Besprechungsanfragen verwendet.</span><span class="sxs-lookup"><span data-stu-id="743e1-115">This property is used in meeting requests.</span></span> <span data-ttu-id="743e1-116">Es stellt keine dar, eine Eintrags-ID, aber eine lange Ganzzahl, die den Termin in der Adresse des Absenders Zeitplan eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="743e1-116">It does not represent an entry identifier, but a long integer that uniquely identifies the appointment within the sender's schedule.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="743e1-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="743e1-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="743e1-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="743e1-118">Protocol specifications</span></span>

<span data-ttu-id="743e1-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="743e1-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="743e1-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="743e1-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="743e1-121">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="743e1-121">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="743e1-122">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="743e1-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="743e1-123">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="743e1-123">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="743e1-124">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="743e1-124">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="743e1-125">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="743e1-125">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="743e1-126">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="743e1-126">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="743e1-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="743e1-127">Header files</span></span>

<span data-ttu-id="743e1-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="743e1-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="743e1-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="743e1-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="743e1-130">mapitags.h</span><span class="sxs-lookup"><span data-stu-id="743e1-130">mapitags.h</span></span>
  
> <span data-ttu-id="743e1-131">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="743e1-131">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="743e1-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="743e1-132">See also</span></span>



[<span data-ttu-id="743e1-133">PidTagOriginalAuthorSearchKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="743e1-133">PidTagOriginalAuthorSearchKey Canonical Property</span></span>](pidtagoriginalauthorsearchkey-canonical-property.md)


[<span data-ttu-id="743e1-134">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="743e1-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="743e1-135">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="743e1-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="743e1-136">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="743e1-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="743e1-137">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="743e1-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

