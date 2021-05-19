---
title: PidTagSentRepresentingAddressType (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingAddressType
api_type:
- COM
ms.assetid: 6ecbf653-1faf-47bd-81a4-20157859fdfd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bbf1ae0d7b38886fe08af2ad13f1a2be6b6e01cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342574"
---
# <a name="pidtagsentrepresentingaddresstype-canonical-property"></a><span data-ttu-id="d8e42-103">PidTagSentRepresentingAddressType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d8e42-103">PidTagSentRepresentingAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="d8e42-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8e42-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8e42-105">Enthält den Adresstyp für den Messagingbenutzer, der durch den Absender dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d8e42-105">Contains the address type for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d8e42-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d8e42-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d8e42-107">PR_SENT_REPRESENTING_ADDRTYPE, PR_SENT_REPRESENTING_ADDRTYPE_A, PR_SENT_REPRESENTING_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="d8e42-107">PR_SENT_REPRESENTING_ADDRTYPE, PR_SENT_REPRESENTING_ADDRTYPE_A, PR_SENT_REPRESENTING_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="d8e42-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="d8e42-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d8e42-109">0x0064</span><span class="sxs-lookup"><span data-stu-id="d8e42-109">0x0064</span></span>  <br/> |
|<span data-ttu-id="d8e42-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d8e42-110">Data type:</span></span>  <br/> |<span data-ttu-id="d8e42-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="d8e42-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="d8e42-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d8e42-112">Area:</span></span>  <br/> |<span data-ttu-id="d8e42-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="d8e42-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d8e42-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d8e42-114">Remarks</span></span>

<span data-ttu-id="d8e42-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den Messagingbenutzer, der vom Absender dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d8e42-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="d8e42-116">Wenn eine Clientanwendung eine Nachricht im Namen eines anderen Clients sendet, sollte sie alle dargestellten Absendereigenschaften auf die Werte für den Client festlegen.</span><span class="sxs-lookup"><span data-stu-id="d8e42-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="d8e42-117">Ein Messagingbenutzer, der in seinem eigenen Namen sendet, überlässt in der Regel die dargestellten Absendereigenschaften nicht.</span><span class="sxs-lookup"><span data-stu-id="d8e42-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="d8e42-118">Der ausgehende Transportanbieter muss diese Eigenschaft immer unverändert lassen, wenn sie vom sendenden Client festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="d8e42-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="d8e42-119">Wenn sie nicht festgelegt ist, sollte der Transportanbieter sie auf die **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))-Eigenschaft für die ausgehende Kopie der Nachricht festlegen und sie in der lokalen Kopie nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="d8e42-119">If it is unset, the transport provider should set it to the **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d8e42-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d8e42-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d8e42-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d8e42-121">Protocol specifications</span></span>

<span data-ttu-id="d8e42-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d8e42-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d8e42-123">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="d8e42-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d8e42-124">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d8e42-124">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d8e42-125">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="d8e42-125">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="d8e42-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d8e42-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d8e42-127">Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.</span><span class="sxs-lookup"><span data-stu-id="d8e42-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="d8e42-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d8e42-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d8e42-129">Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="d8e42-129">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="d8e42-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d8e42-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d8e42-131">Gibt Methoden zum Verbinden und Konfigurieren von Postfächern als Stellvertretung sowie Interaktionen mit Nachrichten- und Kalenderobjekten an, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="d8e42-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="d8e42-132">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d8e42-132">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d8e42-133">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="d8e42-133">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="d8e42-134">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d8e42-134">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d8e42-135">Gibt die Eigenschaften und Vorgänge an, die für Postobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="d8e42-135">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="d8e42-136">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d8e42-136">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d8e42-137">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="d8e42-137">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="d8e42-138">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d8e42-138">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d8e42-139">Codiert und decodiert Nachrichten- und Anlagenobjekte in eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="d8e42-139">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d8e42-140">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="d8e42-140">Header files</span></span>

<span data-ttu-id="d8e42-141">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d8e42-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="d8e42-142">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d8e42-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="d8e42-143">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d8e42-143">Mapitags.h</span></span>
  
> <span data-ttu-id="d8e42-144">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="d8e42-144">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d8e42-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8e42-145">See also</span></span>



[<span data-ttu-id="d8e42-146">PidTagAddressType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d8e42-146">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)


[<span data-ttu-id="d8e42-147">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d8e42-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d8e42-148">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="d8e42-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d8e42-149">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d8e42-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d8e42-150">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d8e42-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

