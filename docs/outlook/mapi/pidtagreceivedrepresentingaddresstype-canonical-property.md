---
title: Kanonische Pidtagreceivedrepresentingaddresstype (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingAddressType
api_type:
- COM
ms.assetid: c342bb2a-157e-4748-bf21-0926f95e5312
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9592057757b7bad0c2400f8b1c720ef0146bb9a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359199"
---
# <a name="pidtagreceivedrepresentingaddresstype-canonical-property"></a><span data-ttu-id="5b304-103">Kanonische Pidtagreceivedrepresentingaddresstype (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5b304-103">PidTagReceivedRepresentingAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="5b304-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b304-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b304-105">Enthält den Adresstyp für den Messagingbenutzer, der von dem Benutzer repräsentiert wird, der die Nachricht tatsächlich empfängt.</span><span class="sxs-lookup"><span data-stu-id="5b304-105">Contains the address type for the messaging user who is represented by the user actually receiving the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5b304-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5b304-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5b304-107">PR_RCVD_REPRESENTING_ADDRTYPE, PR_RCVD_REPRESENTING_ADDRTYPE_A, PR_RCVD_REPRESENTING_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="5b304-107">PR_RCVD_REPRESENTING_ADDRTYPE, PR_RCVD_REPRESENTING_ADDRTYPE_A, PR_RCVD_REPRESENTING_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="5b304-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="5b304-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5b304-109">0x0077</span><span class="sxs-lookup"><span data-stu-id="5b304-109">0x0077</span></span>  <br/> |
|<span data-ttu-id="5b304-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5b304-110">Data type:</span></span>  <br/> |<span data-ttu-id="5b304-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="5b304-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="5b304-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5b304-112">Area:</span></span>  <br/> |<span data-ttu-id="5b304-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="5b304-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b304-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b304-114">Remarks</span></span>

<span data-ttu-id="5b304-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den Messagingbenutzer, der vom empfangenden Benutzer dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5b304-115">These properties are examples of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="5b304-116">Er muss vom eingehenden Transportanbieter festgelegt werden, der auch für die Autorisierung oder Überprüfung des Stellvertreters zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="5b304-116">It must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="5b304-117">Wenn kein Messagingbenutzer dargestellt wird, sollte diese Eigenschaft auf den Adresstyp festgelegt werden, der in der **PR_RECEIVED_BY_ADDRTYPE** ([pidtagreceivedbyaddresstype (](pidtagreceivedbyaddresstype-canonical-property.md))-Eigenschaft enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="5b304-117">If no messaging user is being represented, this property should be set to the address type contained in the **PR_RECEIVED_BY_ADDRTYPE** ([PidTagReceivedByAddressType](pidtagreceivedbyaddresstype-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="5b304-118">Eine Clientanwendung, die auf eine Nachricht antwortet, die im Auftrag eines anderen Clients empfangen wird, sollte diese Eigenschaft aus der empfangenen Nachricht in die **PR_SENT_REPRESENTING_ADDRTYPE** ([pidtagsentrepresentingaddresstype (](pidtagsentrepresentingaddresstype-canonical-property.md))-Eigenschaft für die Antwort kopieren.</span><span class="sxs-lookup"><span data-stu-id="5b304-118">A client application replying to a message received on behalf of another client should copy this property from the received message into the **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5b304-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5b304-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5b304-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5b304-120">Protocol specifications</span></span>

<span data-ttu-id="5b304-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b304-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b304-122">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="5b304-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5b304-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b304-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b304-124">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="5b304-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="5b304-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b304-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b304-126">Verarbeitet die Reihenfolge und den Ablauf für die Datenübertragung zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="5b304-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="5b304-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b304-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b304-128">Konvertiert zwischen IETF-RFC2445, RFC2446 und RFC2447 sowie Termin-und Besprechungs Objekten.</span><span class="sxs-lookup"><span data-stu-id="5b304-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="5b304-129">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b304-129">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b304-130">Gibt Methoden zum Herstellen einer Verbindung mit und Konfigurieren von Postfächern als Stellvertreter sowie Interaktionen mit Nachrichten-und Kalenderobjekten an, wenn Sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="5b304-130">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="5b304-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b304-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b304-132">Codiert und dekodiert Message-und Attachment-Objekte in einer effizienten Datenstrom Darstellung.</span><span class="sxs-lookup"><span data-stu-id="5b304-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5b304-133">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="5b304-133">Header files</span></span>

<span data-ttu-id="5b304-134">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5b304-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="5b304-135">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="5b304-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="5b304-136">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="5b304-136">Mapitags.h</span></span>
  
> <span data-ttu-id="5b304-137">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="5b304-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5b304-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b304-138">See also</span></span>



[<span data-ttu-id="5b304-139">Kanonische Pidtagaddresstype (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5b304-139">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)


[<span data-ttu-id="5b304-140">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5b304-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5b304-141">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5b304-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5b304-142">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5b304-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5b304-143">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5b304-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

