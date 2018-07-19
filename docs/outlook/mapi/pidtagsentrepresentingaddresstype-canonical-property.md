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
ms.openlocfilehash: a58ae878ba13415823e61db3b1717e3cf07f29c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795141"
---
# <a name="pidtagsentrepresentingaddresstype-canonical-property"></a><span data-ttu-id="fb7ae-103">PidTagSentRepresentingAddressType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-103">PidTagSentRepresentingAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="fb7ae-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fb7ae-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fb7ae-105">Enthält den Adresstyp für den messaging-Benutzer, die vom Absender dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-105">Contains the address type for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fb7ae-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="fb7ae-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fb7ae-107">PR_SENT_REPRESENTING_ADDRTYPE, PR_SENT_REPRESENTING_ADDRTYPE_A, PR_SENT_REPRESENTING_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="fb7ae-107">PR_SENT_REPRESENTING_ADDRTYPE, PR_SENT_REPRESENTING_ADDRTYPE_A, PR_SENT_REPRESENTING_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="fb7ae-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="fb7ae-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fb7ae-109">0x0064</span><span class="sxs-lookup"><span data-stu-id="fb7ae-109">0x0064</span></span>  <br/> |
|<span data-ttu-id="fb7ae-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="fb7ae-110">Data type:</span></span>  <br/> |<span data-ttu-id="fb7ae-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="fb7ae-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="fb7ae-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="fb7ae-112">Area:</span></span>  <br/> |<span data-ttu-id="fb7ae-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="fb7ae-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fb7ae-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb7ae-114">Remarks</span></span>

<span data-ttu-id="fb7ae-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für die messaging-Benutzer, die vom Absender angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="fb7ae-116">Wenn eine Clientanwendung eine Nachricht im Auftrag einer anderen Client sendet, sollten sie alle Absender dargestellte Eigenschaften auf die Werte für diesen Client festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="fb7ae-117">Ein messaging-Benutzer in der Regel in einem eigenen Auftrag senden bewirkt, dass die dargestellte Absender Eigenschaften nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="fb7ae-118">Der ausgehende Adressbuchhierarchie muss immer lassen Sie diese Eigenschaft geändert, wenn es vom sendenden Client festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="fb7ae-119">Wenn es nicht festgelegt ist, sollte der Adressbuchhierarchie legen Sie es an die **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))-Eigenschaft für die ausgehende Kopie der Nachricht, und klicken Sie auf die lokale Kopie nicht festgelegt lassen.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-119">If it is unset, the transport provider should set it to the **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fb7ae-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fb7ae-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fb7ae-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="fb7ae-121">Protocol specifications</span></span>

<span data-ttu-id="fb7ae-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb7ae-123">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fb7ae-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb7ae-125">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-125">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="fb7ae-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb7ae-127">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="fb7ae-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb7ae-129">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-129">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="fb7ae-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb7ae-131">Gibt die Methoden zum Herstellen einer Verbindung mit und Konfiguration von Postfächer als Stellvertretungen und Interaktionen mit Nachricht und Kalender-Objekte, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="fb7ae-132">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-132">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb7ae-133">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-133">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="fb7ae-134">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-134">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb7ae-135">Gibt an, die Eigenschaften und Vorgänge, die für zulässige sind Objekte bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-135">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="fb7ae-136">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-136">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb7ae-137">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-137">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="fb7ae-138">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-138">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb7ae-139">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-139">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fb7ae-140">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="fb7ae-140">Header files</span></span>

<span data-ttu-id="fb7ae-141">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fb7ae-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="fb7ae-142">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="fb7ae-143">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fb7ae-143">Mapitags.h</span></span>
  
> <span data-ttu-id="fb7ae-144">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-144">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fb7ae-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb7ae-145">See also</span></span>



[<span data-ttu-id="fb7ae-146">PidTagAddressType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-146">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)


[<span data-ttu-id="fb7ae-147">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fb7ae-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fb7ae-148">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fb7ae-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fb7ae-149">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="fb7ae-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fb7ae-150">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="fb7ae-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

