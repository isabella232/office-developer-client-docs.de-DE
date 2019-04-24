---
title: Kanonische Pidlidappointmentreplyname (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentReplyName
api_type:
- COM
ms.assetid: 2f3a44d1-600f-412e-bc89-078841db5308
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f6707c49c70804aeb757119aa411ca4059e378eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356042"
---
# <a name="pidlidappointmentreplyname-canonical-property"></a><span data-ttu-id="89d98-103">Kanonische Pidlidappointmentreplyname (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="89d98-103">PidLidAppointmentReplyName Canonical Property</span></span>

  
  
<span data-ttu-id="89d98-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89d98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89d98-105">Gibt den Benutzer an, der zuletzt auf die Besprechungsanfrage oder das Besprechungs Update Objekt geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="89d98-105">Specifies the user who last replied to the meeting request or meeting update object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="89d98-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="89d98-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="89d98-107">dispidApptReplyName</span><span class="sxs-lookup"><span data-stu-id="89d98-107">dispidApptReplyName</span></span>  <br/> |
|<span data-ttu-id="89d98-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="89d98-108">Property set:</span></span>  <br/> |<span data-ttu-id="89d98-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="89d98-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="89d98-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="89d98-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="89d98-111">0x00008230</span><span class="sxs-lookup"><span data-stu-id="89d98-111">0x00008230</span></span>  <br/> |
|<span data-ttu-id="89d98-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="89d98-112">Data type:</span></span>  <br/> |<span data-ttu-id="89d98-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="89d98-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="89d98-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="89d98-114">Area:</span></span>  <br/> |<span data-ttu-id="89d98-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="89d98-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="89d98-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89d98-116">Remarks</span></span>

<span data-ttu-id="89d98-117">Diese Eigenschaft wird nur für einen delegierenden festgelegt, wenn ein Delegat reagiert.</span><span class="sxs-lookup"><span data-stu-id="89d98-117">This property is only set for a delegator when a delegate responded.</span></span> <span data-ttu-id="89d98-118">Der Wert ist gleich der **PR_MAILBOX_OWNER_NAME** ([pidtagmailboxownername (](pidtagmailboxownername-canonical-property.md))-Eigenschaft für den Speicher des Delegaten.</span><span class="sxs-lookup"><span data-stu-id="89d98-118">The value is equal to the **PR_MAILBOX_OWNER_NAME** ([PidTagMailboxOwnerName](pidtagmailboxownername-canonical-property.md)) property for the delegate's store.</span></span> <span data-ttu-id="89d98-119">Diese Eigenschaft hat keine Bedeutung für den Organisator.</span><span class="sxs-lookup"><span data-stu-id="89d98-119">This property has no meaning for the organizer.</span></span> <span data-ttu-id="89d98-120">Weitere Informationen zu **PR_MAILBOX_OWNER_NAME**finden Sie unter Store Object Protocol, angegeben in [[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="89d98-120">For details on **PR_MAILBOX_OWNER_NAME**, see store object protocol specified in [[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="89d98-121">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="89d98-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="89d98-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="89d98-122">Protocol specifications</span></span>

<span data-ttu-id="89d98-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="89d98-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="89d98-124">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="89d98-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="89d98-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="89d98-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="89d98-126">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="89d98-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="89d98-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="89d98-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="89d98-128">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="89d98-128">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="89d98-129">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="89d98-129">Header files</span></span>

<span data-ttu-id="89d98-130">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="89d98-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="89d98-131">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="89d98-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="89d98-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89d98-132">See also</span></span>



[<span data-ttu-id="89d98-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="89d98-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="89d98-134">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="89d98-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="89d98-135">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="89d98-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="89d98-136">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="89d98-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

