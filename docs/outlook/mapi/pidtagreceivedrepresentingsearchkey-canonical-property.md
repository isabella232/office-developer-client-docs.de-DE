---
title: PidTagReceivedRepresentingSearchKey (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingSearchKey
api_type:
- COM
ms.assetid: 234c797c-4a3c-4e05-be22-2a2fa377871f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bcf310138e4b43b1cc36a177194f721c401caba6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394762"
---
# <a name="pidtagreceivedrepresentingsearchkey-canonical-property"></a><span data-ttu-id="bd733-103">PidTagReceivedRepresentingSearchKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bd733-103">PidTagReceivedRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="bd733-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd733-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd733-105">Enthält den Search-Schlüssel für die messaging-Benutzer von der empfangenden Benutzer dargestellt.</span><span class="sxs-lookup"><span data-stu-id="bd733-105">Contains the search key for the messaging user represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bd733-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bd733-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bd733-107">PR_RCVD_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="bd733-107">PR_RCVD_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="bd733-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="bd733-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bd733-109">0x0052</span><span class="sxs-lookup"><span data-stu-id="bd733-109">0x0052</span></span>  <br/> |
|<span data-ttu-id="bd733-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bd733-110">Data type:</span></span>  <br/> |<span data-ttu-id="bd733-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd733-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bd733-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bd733-112">Area:</span></span>  <br/> |<span data-ttu-id="bd733-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="bd733-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd733-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bd733-114">Remarks</span></span>

<span data-ttu-id="bd733-115">Diese Eigenschaft ist eine der Eigenschaften für die messaging-Benutzer, die von der empfangenden Benutzer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="bd733-115">This property is one of the address properties for the messaging user being represented by the receiving user.</span></span> <span data-ttu-id="bd733-116">Von der eingehenden Adressbuchhierarchie muss festgelegt werden, die auch für die Autorisierung oder Überprüfung des Delegaten zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="bd733-116">It must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="bd733-117">Wenn kein messaging Benutzer dargestellt wird, sollten diese Eigenschaft auf den Schlüssel Suche in der **PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md))-Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="bd733-117">If no messaging user is being represented, this property should be set to the search key contained in the **PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="bd733-118">Ein Client Application Antworten auf eine Nachricht im Auftrag einer anderen Client empfangene sollte diese Eigenschaft in der **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))-Eigenschaft für die Antwort aus der empfangenen Nachricht kopieren.</span><span class="sxs-lookup"><span data-stu-id="bd733-118">A client application replying to a message received on behalf of another client should copy this property from the received message into the **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bd733-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bd733-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bd733-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="bd733-120">Protocol specifications</span></span>

<span data-ttu-id="bd733-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd733-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd733-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="bd733-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bd733-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd733-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd733-124">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="bd733-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="bd733-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd733-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd733-126">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="bd733-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="bd733-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd733-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd733-128">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="bd733-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="bd733-129">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd733-129">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd733-130">Gibt die Methoden zum Herstellen einer Verbindung mit und Konfiguration von Postfächer als Stellvertretungen und Interaktionen mit Nachricht und Kalender-Objekte, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="bd733-130">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="bd733-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd733-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd733-132">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="bd733-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bd733-133">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="bd733-133">Header files</span></span>

<span data-ttu-id="bd733-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bd733-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="bd733-135">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="bd733-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="bd733-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bd733-136">Mapitags.h</span></span>
  
> <span data-ttu-id="bd733-137">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="bd733-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bd733-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd733-138">See also</span></span>



[<span data-ttu-id="bd733-139">PidTagSearchKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bd733-139">PidTagSearchKey Canonical Property</span></span>](pidtagsearchkey-canonical-property.md)


[<span data-ttu-id="bd733-140">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bd733-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bd733-141">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bd733-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bd733-142">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bd733-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bd733-143">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bd733-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

