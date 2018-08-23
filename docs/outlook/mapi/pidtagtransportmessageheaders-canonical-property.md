---
title: PidTagTransportMessageHeaders (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTransportMessageHeaders
api_type:
- COM
ms.assetid: 9f8e3f20-6454-4dfd-9b35-e0401abac6b3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 16c3684176de765a10b5bac620ea65a824cfe83a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588762"
---
# <a name="pidtagtransportmessageheaders-canonical-property"></a><span data-ttu-id="bf496-103">PidTagTransportMessageHeaders (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bf496-103">PidTagTransportMessageHeaders Canonical Property</span></span>

  
  
<span data-ttu-id="bf496-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf496-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf496-105">Transport-spezifische Informationen im Nachrichtenumschlag enthält.</span><span class="sxs-lookup"><span data-stu-id="bf496-105">Contains transport-specific message envelope information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bf496-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bf496-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bf496-107">PR_TRANSPORT_MESSAGE_HEADERS, PR_TRANSPORT_MESSAGE_HEADERS_A, PR_TRANSPORT_MESSAGE_HEADERS_W</span><span class="sxs-lookup"><span data-stu-id="bf496-107">PR_TRANSPORT_MESSAGE_HEADERS, PR_TRANSPORT_MESSAGE_HEADERS_A, PR_TRANSPORT_MESSAGE_HEADERS_W</span></span>  <br/> |
|<span data-ttu-id="bf496-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="bf496-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bf496-109">0x007D</span><span class="sxs-lookup"><span data-stu-id="bf496-109">0x007D</span></span>  <br/> |
|<span data-ttu-id="bf496-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bf496-110">Data type:</span></span>  <br/> |<span data-ttu-id="bf496-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bf496-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bf496-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bf496-112">Area:</span></span>  <br/> |<span data-ttu-id="bf496-113">E-Mail</span><span class="sxs-lookup"><span data-stu-id="bf496-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf496-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="bf496-114">Remarks</span></span>

<span data-ttu-id="bf496-115">Der Transportdienst kann die Kopfzeileninformationen für eingehende Nachrichten generieren.</span><span class="sxs-lookup"><span data-stu-id="bf496-115">The transport provider can generate the message header information for inbound messages.</span></span>
  
<span data-ttu-id="bf496-116">Diese Eigenschaften bieten eine Alternative zum Verwerfen der Transport Kopfzeileninformationen oder den Nachrichtentext vorangestellt wird.</span><span class="sxs-lookup"><span data-stu-id="bf496-116">These properties offer an alternative to either discarding the transport message header information or prepending it to the message text.</span></span> <span data-ttu-id="bf496-117">Der Client können, ob die Informationen angezeigt werden soll oder nicht.</span><span class="sxs-lookup"><span data-stu-id="bf496-117">The client can choose whether or not to display the information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bf496-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bf496-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bf496-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="bf496-119">Protocol specifications</span></span>

<span data-ttu-id="bf496-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf496-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf496-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="bf496-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bf496-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf496-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf496-123">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="bf496-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="bf496-124">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf496-124">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf496-125">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="bf496-125">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bf496-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="bf496-126">Header files</span></span>

<span data-ttu-id="bf496-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bf496-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="bf496-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="bf496-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="bf496-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bf496-129">Mapitags.h</span></span>
  
> <span data-ttu-id="bf496-130">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="bf496-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bf496-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf496-131">See also</span></span>



[<span data-ttu-id="bf496-132">PidTagBody (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bf496-132">PidTagBody Canonical Property</span></span>](pidtagbody-canonical-property.md)


[<span data-ttu-id="bf496-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bf496-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bf496-134">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bf496-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bf496-135">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bf496-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bf496-136">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bf496-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

