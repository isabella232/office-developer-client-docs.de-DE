---
title: Kanonische PidTagTransportMessageHeaders-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e184fd0933295984af97258d785df92306160a6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795301"
---
# <a name="pidtagtransportmessageheaders-canonical-property"></a><span data-ttu-id="ab8d5-103">Kanonische PidTagTransportMessageHeaders-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ab8d5-103">PidTagTransportMessageHeaders Canonical Property</span></span>

  
  
<span data-ttu-id="ab8d5-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ab8d5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ab8d5-105">Transport-spezifische Informationen im Nachrichtenumschlag enthält.</span><span class="sxs-lookup"><span data-stu-id="ab8d5-105">Contains transport-specific message envelope information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ab8d5-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ab8d5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ab8d5-107">PR_TRANSPORT_MESSAGE_HEADERS, PR_TRANSPORT_MESSAGE_HEADERS_A, PR_TRANSPORT_MESSAGE_HEADERS_W</span><span class="sxs-lookup"><span data-stu-id="ab8d5-107">PR_TRANSPORT_MESSAGE_HEADERS, PR_TRANSPORT_MESSAGE_HEADERS_A, PR_TRANSPORT_MESSAGE_HEADERS_W</span></span>  <br/> |
|<span data-ttu-id="ab8d5-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="ab8d5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ab8d5-109">0x007D</span><span class="sxs-lookup"><span data-stu-id="ab8d5-109">0x007D</span></span>  <br/> |
|<span data-ttu-id="ab8d5-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ab8d5-110">Data type:</span></span>  <br/> |<span data-ttu-id="ab8d5-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ab8d5-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ab8d5-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ab8d5-112">Area:</span></span>  <br/> |<span data-ttu-id="ab8d5-113">E-Mail</span><span class="sxs-lookup"><span data-stu-id="ab8d5-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab8d5-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ab8d5-114">Remarks</span></span>

<span data-ttu-id="ab8d5-115">Der Transportdienst kann die Kopfzeileninformationen für eingehende Nachrichten generieren.</span><span class="sxs-lookup"><span data-stu-id="ab8d5-115">The transport provider can generate the message header information for inbound messages.</span></span>
  
<span data-ttu-id="ab8d5-116">Diese Eigenschaften bieten eine Alternative zum Verwerfen der Transport Kopfzeileninformationen oder den Nachrichtentext vorangestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ab8d5-116">These properties offer an alternative to either discarding the transport message header information or prepending it to the message text.</span></span> <span data-ttu-id="ab8d5-117">Der Client können, ob die Informationen angezeigt werden soll oder nicht.</span><span class="sxs-lookup"><span data-stu-id="ab8d5-117">The client can choose whether or not to display the information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ab8d5-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ab8d5-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ab8d5-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ab8d5-119">Protocol specifications</span></span>

<span data-ttu-id="ab8d5-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab8d5-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab8d5-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="ab8d5-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ab8d5-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab8d5-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab8d5-123">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="ab8d5-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="ab8d5-124">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab8d5-124">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab8d5-125">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="ab8d5-125">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ab8d5-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="ab8d5-126">Header files</span></span>

<span data-ttu-id="ab8d5-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ab8d5-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="ab8d5-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ab8d5-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="ab8d5-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ab8d5-129">Mapitags.h</span></span>
  
> <span data-ttu-id="ab8d5-130">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ab8d5-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ab8d5-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab8d5-131">See also</span></span>



[<span data-ttu-id="ab8d5-132">Kanonische PidTagBody-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ab8d5-132">PidTagBody Canonical Property</span></span>](pidtagbody-canonical-property.md)


[<span data-ttu-id="ab8d5-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab8d5-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ab8d5-134">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab8d5-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ab8d5-135">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ab8d5-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ab8d5-136">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ab8d5-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

