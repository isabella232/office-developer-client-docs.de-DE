---
title: Kanonische PidLidAppointmentReplyName-Eigenschaft
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
ms.openlocfilehash: 5b6d88b60f9f5c6a01a92ecc5905f711fbf3ab3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793398"
---
# <a name="pidlidappointmentreplyname-canonical-property"></a><span data-ttu-id="2e255-103">Kanonische PidLidAppointmentReplyName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2e255-103">PidLidAppointmentReplyName Canonical Property</span></span>

  
  
<span data-ttu-id="2e255-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2e255-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2e255-105">Gibt den Benutzer, die zuletzt auf die Besprechungsanfrage darauf geantwortet oder Besprechung aktualisieren-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2e255-105">Specifies the user who last replied to the meeting request or meeting update object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2e255-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2e255-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2e255-107">dispidApptReplyName</span><span class="sxs-lookup"><span data-stu-id="2e255-107">dispidApptReplyName</span></span>  <br/> |
|<span data-ttu-id="2e255-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="2e255-108">Property set:</span></span>  <br/> |<span data-ttu-id="2e255-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="2e255-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="2e255-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="2e255-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2e255-111">0x00008230</span><span class="sxs-lookup"><span data-stu-id="2e255-111">0x00008230</span></span>  <br/> |
|<span data-ttu-id="2e255-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="2e255-112">Data type:</span></span>  <br/> |<span data-ttu-id="2e255-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2e255-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2e255-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2e255-114">Area:</span></span>  <br/> |<span data-ttu-id="2e255-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="2e255-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e255-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2e255-116">Remarks</span></span>

<span data-ttu-id="2e255-117">Diese Eigenschaft wird nur für eine Delegator festgelegt, wenn eine Stellvertretung geantwortet.</span><span class="sxs-lookup"><span data-stu-id="2e255-117">This property is only set for a delegator when a delegate responded.</span></span> <span data-ttu-id="2e255-118">Der Wert ist gleich der **PR_MAILBOX_OWNER_NAME** ([PidTagMailboxOwnerName](pidtagmailboxownername-canonical-property.md))-Eigenschaft für den Delegaten Speicher.</span><span class="sxs-lookup"><span data-stu-id="2e255-118">The value is equal to the **PR_MAILBOX_OWNER_NAME** ([PidTagMailboxOwnerName](pidtagmailboxownername-canonical-property.md)) property for the delegate's store.</span></span> <span data-ttu-id="2e255-119">Diese Eigenschaft hat keine Bedeutung für den Organisator.</span><span class="sxs-lookup"><span data-stu-id="2e255-119">This property has no meaning for the organizer.</span></span> <span data-ttu-id="2e255-120">Ausführliche Informationen zum **PR_MAILBOX_OWNER_NAME**finden Sie unter Speichern in [[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)angegebene Objektprotokoll.</span><span class="sxs-lookup"><span data-stu-id="2e255-120">For details on **PR_MAILBOX_OWNER_NAME**, see store object protocol specified in [[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2e255-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2e255-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2e255-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="2e255-122">Protocol specifications</span></span>

<span data-ttu-id="2e255-123">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2e255-123">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2e255-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="2e255-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="2e255-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2e255-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2e255-126">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="2e255-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2e255-127">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2e255-127">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2e255-128">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="2e255-128">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2e255-129">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="2e255-129">Header files</span></span>

<span data-ttu-id="2e255-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2e255-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="2e255-131">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="2e255-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2e255-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e255-132">See also</span></span>



[<span data-ttu-id="2e255-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2e255-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2e255-134">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2e255-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2e255-135">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2e255-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2e255-136">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2e255-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

