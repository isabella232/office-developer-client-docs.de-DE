---
title: PidTagSentRepresentingEmailAddress (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingEmailAddress
api_type:
- COM
ms.assetid: 5fa4edde-475c-4568-946b-73eb08f97a61
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 689bdeb463d0e54d02be88463dabb75ef756bee9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573922"
---
# <a name="pidtagsentrepresentingemailaddress-canonical-property"></a><span data-ttu-id="df6f6-103">PidTagSentRepresentingEmailAddress (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="df6f6-103">PidTagSentRepresentingEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="df6f6-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df6f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df6f6-105">Enthält die e-Mail-Adresse für den messaging-Benutzer, die vom Absender dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="df6f6-105">Contains the email address for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="df6f6-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="df6f6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="df6f6-107">PR_SENT_REPRESENTING_EMAIL_ADDRESS, PR_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_SENT_REPRESENTING_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="df6f6-107">PR_SENT_REPRESENTING_EMAIL_ADDRESS, PR_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_SENT_REPRESENTING_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="df6f6-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="df6f6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="df6f6-109">0 x 0065</span><span class="sxs-lookup"><span data-stu-id="df6f6-109">0x0065</span></span>  <br/> |
|<span data-ttu-id="df6f6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="df6f6-110">Data type:</span></span>  <br/> |<span data-ttu-id="df6f6-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="df6f6-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="df6f6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="df6f6-112">Area:</span></span>  <br/> |<span data-ttu-id="df6f6-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="df6f6-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df6f6-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="df6f6-114">Remarks</span></span>

<span data-ttu-id="df6f6-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für die messaging-Benutzer, die vom Absender angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="df6f6-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="df6f6-116">Wenn eine Clientanwendung eine Nachricht im Auftrag einer anderen Client sendet, sollten sie alle Absender dargestellte Eigenschaften auf die Werte für diesen Client festgelegt.</span><span class="sxs-lookup"><span data-stu-id="df6f6-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="df6f6-117">Ein messaging-Benutzer in der Regel in einem eigenen Auftrag senden bewirkt, dass die dargestellte Absender Eigenschaften nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="df6f6-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="df6f6-118">Der ausgehende Adressbuchhierarchie muss immer lassen Sie diese Eigenschaften geändert, wenn es vom sendenden Client festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="df6f6-118">The outgoing transport provider must always leave these properties unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="df6f6-119">Wenn es nicht festgelegt ist, sollte der Adressbuchhierarchie legen Sie es an die **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))-Eigenschaft für die ausgehende Kopie der Nachricht, und klicken Sie auf die lokale Kopie nicht festgelegt lassen.</span><span class="sxs-lookup"><span data-stu-id="df6f6-119">If it is unset, the transport provider should set it to the **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="df6f6-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="df6f6-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="df6f6-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="df6f6-121">Protocol specifications</span></span>

<span data-ttu-id="df6f6-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df6f6-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df6f6-123">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="df6f6-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="df6f6-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df6f6-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df6f6-125">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="df6f6-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="df6f6-126">[[MS-OXORSS]](http://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df6f6-126">[[MS-OXORSS]](http://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df6f6-127">Gibt die Eigenschaften und Operationen, die RSS-Elemente darstellen.</span><span class="sxs-lookup"><span data-stu-id="df6f6-127">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="df6f6-128">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df6f6-128">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df6f6-129">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="df6f6-129">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="df6f6-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df6f6-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df6f6-131">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="df6f6-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="df6f6-132">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df6f6-132">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df6f6-133">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="df6f6-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="df6f6-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df6f6-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df6f6-135">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="df6f6-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="df6f6-136">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df6f6-136">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df6f6-137">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="df6f6-137">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="df6f6-138">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="df6f6-138">Header files</span></span>

<span data-ttu-id="df6f6-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="df6f6-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="df6f6-140">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="df6f6-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="df6f6-141">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="df6f6-141">Mapitags.h</span></span>
  
> <span data-ttu-id="df6f6-142">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="df6f6-142">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="df6f6-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df6f6-143">See also</span></span>



[<span data-ttu-id="df6f6-144">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="df6f6-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="df6f6-145">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="df6f6-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="df6f6-146">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="df6f6-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="df6f6-147">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="df6f6-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

