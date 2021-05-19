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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356819"
---
# <a name="pidtagreceivedrepresentingsearchkey-canonical-property"></a><span data-ttu-id="ff366-103">PidTagReceivedRepresentingSearchKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ff366-103">PidTagReceivedRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="ff366-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff366-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff366-105">Enthält den Suchschlüssel für den Messagingbenutzer, der vom empfangenden Benutzer dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ff366-105">Contains the search key for the messaging user represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ff366-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ff366-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ff366-107">PR_RCVD_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="ff366-107">PR_RCVD_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="ff366-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="ff366-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ff366-109">0x0052</span><span class="sxs-lookup"><span data-stu-id="ff366-109">0x0052</span></span>  <br/> |
|<span data-ttu-id="ff366-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ff366-110">Data type:</span></span>  <br/> |<span data-ttu-id="ff366-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ff366-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ff366-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ff366-112">Area:</span></span>  <br/> |<span data-ttu-id="ff366-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="ff366-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff366-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ff366-114">Remarks</span></span>

<span data-ttu-id="ff366-115">Diese Eigenschaft ist eine der Adresseigenschaften für den Messagingbenutzer, der vom empfangenden Benutzer dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ff366-115">This property is one of the address properties for the messaging user being represented by the receiving user.</span></span> <span data-ttu-id="ff366-116">Sie muss vom eingehenden Transportanbieter festgelegt werden, der auch für die Autorisierung oder Überprüfung der Stellvertretung zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="ff366-116">It must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="ff366-117">Wenn kein Messagingbenutzer dargestellt wird, sollte diese Eigenschaft auf den Suchschlüssel in der **PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md)) -Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ff366-117">If no messaging user is being represented, this property should be set to the search key contained in the **PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="ff366-118">Eine Clientanwendung, die auf eine Nachricht antwortet, die im Namen eines anderen Clients empfangen wurde, sollte diese Eigenschaft aus der empfangenen Nachricht in die **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))-Eigenschaft für die Antwort kopieren.</span><span class="sxs-lookup"><span data-stu-id="ff366-118">A client application replying to a message received on behalf of another client should copy this property from the received message into the **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ff366-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ff366-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ff366-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ff366-120">Protocol specifications</span></span>

<span data-ttu-id="ff366-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff366-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff366-122">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="ff366-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ff366-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff366-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff366-124">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="ff366-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="ff366-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff366-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff366-126">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="ff366-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="ff366-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff366-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff366-128">Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.</span><span class="sxs-lookup"><span data-stu-id="ff366-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="ff366-129">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff366-129">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff366-130">Gibt Methoden zum Verbinden und Konfigurieren von Postfächern als Stellvertretung sowie Interaktionen mit Nachrichten- und Kalenderobjekten an, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="ff366-130">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="ff366-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff366-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff366-132">Codiert und decodiert Nachrichten- und Anlagenobjekte in eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="ff366-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ff366-133">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="ff366-133">Header files</span></span>

<span data-ttu-id="ff366-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ff366-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="ff366-135">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ff366-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="ff366-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ff366-136">Mapitags.h</span></span>
  
> <span data-ttu-id="ff366-137">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="ff366-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ff366-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff366-138">See also</span></span>



[<span data-ttu-id="ff366-139">PidTagSearchKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ff366-139">PidTagSearchKey Canonical Property</span></span>](pidtagsearchkey-canonical-property.md)


[<span data-ttu-id="ff366-140">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ff366-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ff366-141">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="ff366-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ff366-142">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ff366-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ff366-143">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ff366-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

