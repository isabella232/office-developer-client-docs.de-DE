---
title: PidLidAppointmentReplyName (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f6707c49c70804aeb757119aa411ca4059e378eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356042"
---
# <a name="pidlidappointmentreplyname-canonical-property"></a><span data-ttu-id="c1b77-103">PidLidAppointmentReplyName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c1b77-103">PidLidAppointmentReplyName Canonical Property</span></span>

  
  
<span data-ttu-id="c1b77-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1b77-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1b77-105">Gibt den Benutzer an, der zuletzt auf das Besprechungsanfrage- oder Besprechungsupdateobjekt geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="c1b77-105">Specifies the user who last replied to the meeting request or meeting update object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c1b77-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c1b77-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c1b77-107">dispidApptReplyName</span><span class="sxs-lookup"><span data-stu-id="c1b77-107">dispidApptReplyName</span></span>  <br/> |
|<span data-ttu-id="c1b77-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="c1b77-108">Property set:</span></span>  <br/> |<span data-ttu-id="c1b77-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="c1b77-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="c1b77-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="c1b77-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c1b77-111">0x00008230</span><span class="sxs-lookup"><span data-stu-id="c1b77-111">0x00008230</span></span>  <br/> |
|<span data-ttu-id="c1b77-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c1b77-112">Data type:</span></span>  <br/> |<span data-ttu-id="c1b77-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c1b77-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c1b77-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c1b77-114">Area:</span></span>  <br/> |<span data-ttu-id="c1b77-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="c1b77-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c1b77-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c1b77-116">Remarks</span></span>

<span data-ttu-id="c1b77-117">Diese Eigenschaft wird nur für einen Delegator festgelegt, wenn eine Stellvertretung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="c1b77-117">This property is only set for a delegator when a delegate responded.</span></span> <span data-ttu-id="c1b77-118">Der Wert entspricht der **PR_MAILBOX_OWNER_NAME** ([PidTagMailboxOwnerName](pidtagmailboxownername-canonical-property.md)) -Eigenschaft für den Delegatspeicher.</span><span class="sxs-lookup"><span data-stu-id="c1b77-118">The value is equal to the **PR_MAILBOX_OWNER_NAME** ([PidTagMailboxOwnerName](pidtagmailboxownername-canonical-property.md)) property for the delegate's store.</span></span> <span data-ttu-id="c1b77-119">Diese Eigenschaft hat keine Bedeutung für den Organisator.</span><span class="sxs-lookup"><span data-stu-id="c1b77-119">This property has no meaning for the organizer.</span></span> <span data-ttu-id="c1b77-120">Weitere Informationen **zu** PR_MAILBOX_OWNER_NAME finden Sie unter Store object protocol specified in [[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c1b77-120">For details on **PR_MAILBOX_OWNER_NAME**, see store object protocol specified in [[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c1b77-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c1b77-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c1b77-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c1b77-122">Protocol specifications</span></span>

<span data-ttu-id="c1b77-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c1b77-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c1b77-124">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c1b77-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="c1b77-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c1b77-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c1b77-126">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="c1b77-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c1b77-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c1b77-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c1b77-128">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="c1b77-128">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c1b77-129">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="c1b77-129">Header files</span></span>

<span data-ttu-id="c1b77-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c1b77-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="c1b77-131">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c1b77-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c1b77-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1b77-132">See also</span></span>



[<span data-ttu-id="c1b77-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c1b77-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c1b77-134">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="c1b77-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c1b77-135">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c1b77-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c1b77-136">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c1b77-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

