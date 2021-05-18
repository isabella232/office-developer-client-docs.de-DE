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
ms.openlocfilehash: 7ad9048a19123b94c10afaddcbedb7f54e8fe477
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360760"
---
# <a name="pidtagtransportmessageheaders-canonical-property"></a><span data-ttu-id="c832a-103">PidTagTransportMessageHeaders (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c832a-103">PidTagTransportMessageHeaders Canonical Property</span></span>

  
  
<span data-ttu-id="c832a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c832a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c832a-105">Enthält transportspezifische Nachrichtenumschlaginformationen.</span><span class="sxs-lookup"><span data-stu-id="c832a-105">Contains transport-specific message envelope information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c832a-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c832a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c832a-107">PR_TRANSPORT_MESSAGE_HEADERS, PR_TRANSPORT_MESSAGE_HEADERS_A, PR_TRANSPORT_MESSAGE_HEADERS_W</span><span class="sxs-lookup"><span data-stu-id="c832a-107">PR_TRANSPORT_MESSAGE_HEADERS, PR_TRANSPORT_MESSAGE_HEADERS_A, PR_TRANSPORT_MESSAGE_HEADERS_W</span></span>  <br/> |
|<span data-ttu-id="c832a-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="c832a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c832a-109">0x007D</span><span class="sxs-lookup"><span data-stu-id="c832a-109">0x007D</span></span>  <br/> |
|<span data-ttu-id="c832a-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c832a-110">Data type:</span></span>  <br/> |<span data-ttu-id="c832a-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c832a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c832a-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c832a-112">Area:</span></span>  <br/> |<span data-ttu-id="c832a-113">E-Mails</span><span class="sxs-lookup"><span data-stu-id="c832a-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c832a-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c832a-114">Remarks</span></span>

<span data-ttu-id="c832a-115">Der Transportanbieter kann die Nachrichtenkopfinformationen für eingehende Nachrichten generieren.</span><span class="sxs-lookup"><span data-stu-id="c832a-115">The transport provider can generate the message header information for inbound messages.</span></span>
  
<span data-ttu-id="c832a-116">Diese Eigenschaften bieten eine Alternative zum Verwerfen der Kopfzeileninformationen für Transportnachrichten oder zum Vorabanstehen im Nachrichtentext.</span><span class="sxs-lookup"><span data-stu-id="c832a-116">These properties offer an alternative to either discarding the transport message header information or prepending it to the message text.</span></span> <span data-ttu-id="c832a-117">Der Client kann auswählen, ob die Informationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c832a-117">The client can choose whether or not to display the information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c832a-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c832a-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c832a-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c832a-119">Protocol specifications</span></span>

<span data-ttu-id="c832a-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c832a-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c832a-121">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="c832a-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c832a-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c832a-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c832a-123">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="c832a-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="c832a-124">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c832a-124">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c832a-125">Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="c832a-125">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c832a-126">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="c832a-126">Header files</span></span>

<span data-ttu-id="c832a-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c832a-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="c832a-128">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c832a-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="c832a-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c832a-129">Mapitags.h</span></span>
  
> <span data-ttu-id="c832a-130">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="c832a-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c832a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c832a-131">See also</span></span>



[<span data-ttu-id="c832a-132">PidTagBody (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c832a-132">PidTagBody Canonical Property</span></span>](pidtagbody-canonical-property.md)


[<span data-ttu-id="c832a-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c832a-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c832a-134">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="c832a-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c832a-135">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c832a-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c832a-136">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c832a-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

