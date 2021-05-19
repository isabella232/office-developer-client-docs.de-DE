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
ms.openlocfilehash: 7ad68a8ba527879871e79dd85e79d577291d32a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335441"
---
# <a name="pidtagownerappointmentid-canonical-property"></a><span data-ttu-id="0cb95-103">PidTagOwnerAppointmentId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0cb95-103">PidTagOwnerAppointmentId Canonical Property</span></span>

  
  
<span data-ttu-id="0cb95-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0cb95-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0cb95-105">Enthält einen Bezeichner für einen Termin im Zeitplan des Besitzers.</span><span class="sxs-lookup"><span data-stu-id="0cb95-105">Contains an identifier for an appointment in the owner's schedule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0cb95-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0cb95-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0cb95-107">PR_OWNER_APPT_ID</span><span class="sxs-lookup"><span data-stu-id="0cb95-107">PR_OWNER_APPT_ID</span></span>  <br/> |
|<span data-ttu-id="0cb95-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="0cb95-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0cb95-109">0x0062</span><span class="sxs-lookup"><span data-stu-id="0cb95-109">0x0062</span></span>  <br/> |
|<span data-ttu-id="0cb95-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0cb95-110">Data type:</span></span>  <br/> |<span data-ttu-id="0cb95-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0cb95-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0cb95-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0cb95-112">Area:</span></span>  <br/> |<span data-ttu-id="0cb95-113">Termin</span><span class="sxs-lookup"><span data-stu-id="0cb95-113">Appointment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0cb95-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0cb95-114">Remarks</span></span>

<span data-ttu-id="0cb95-115">Diese Eigenschaft wird in Besprechungsanfragen verwendet.</span><span class="sxs-lookup"><span data-stu-id="0cb95-115">This property is used in meeting requests.</span></span> <span data-ttu-id="0cb95-116">Es stellt keine Eintrags-ID dar, sondern eine lange ganzzahlige Zahl, die den Termin innerhalb des Zeitplans des Absenders eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0cb95-116">It does not represent an entry identifier, but a long integer that uniquely identifies the appointment within the sender's schedule.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0cb95-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0cb95-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0cb95-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0cb95-118">Protocol specifications</span></span>

<span data-ttu-id="0cb95-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0cb95-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0cb95-120">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="0cb95-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0cb95-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0cb95-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0cb95-122">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="0cb95-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="0cb95-123">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0cb95-123">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0cb95-124">Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.</span><span class="sxs-lookup"><span data-stu-id="0cb95-124">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="0cb95-125">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0cb95-125">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0cb95-126">Codiert und decodiert Nachrichten- und Anlagenobjekte in eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="0cb95-126">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0cb95-127">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="0cb95-127">Header files</span></span>

<span data-ttu-id="0cb95-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0cb95-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="0cb95-129">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0cb95-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="0cb95-130">mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0cb95-130">mapitags.h</span></span>
  
> <span data-ttu-id="0cb95-131">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="0cb95-131">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0cb95-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0cb95-132">See also</span></span>



[<span data-ttu-id="0cb95-133">PidTagOriginalAuthorSearchKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0cb95-133">PidTagOriginalAuthorSearchKey Canonical Property</span></span>](pidtagoriginalauthorsearchkey-canonical-property.md)


[<span data-ttu-id="0cb95-134">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0cb95-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0cb95-135">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="0cb95-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0cb95-136">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0cb95-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0cb95-137">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0cb95-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

