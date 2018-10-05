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
ms.openlocfilehash: 1b82e1e96a5ffbb5c17dd919e78a9f07342194c5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397380"
---
# <a name="pidtagsentrepresentingemailaddress-canonical-property"></a><span data-ttu-id="0c73e-103">PidTagSentRepresentingEmailAddress (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0c73e-103">PidTagSentRepresentingEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="0c73e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c73e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c73e-105">Enthält die e-Mail-Adresse für den messaging-Benutzer, die vom Absender dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="0c73e-105">Contains the email address for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0c73e-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0c73e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0c73e-107">PR_SENT_REPRESENTING_EMAIL_ADDRESS, PR_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_SENT_REPRESENTING_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="0c73e-107">PR_SENT_REPRESENTING_EMAIL_ADDRESS, PR_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_SENT_REPRESENTING_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="0c73e-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="0c73e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0c73e-109">0 x 0065</span><span class="sxs-lookup"><span data-stu-id="0c73e-109">0x0065</span></span>  <br/> |
|<span data-ttu-id="0c73e-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0c73e-110">Data type:</span></span>  <br/> |<span data-ttu-id="0c73e-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="0c73e-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="0c73e-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0c73e-112">Area:</span></span>  <br/> |<span data-ttu-id="0c73e-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="0c73e-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0c73e-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0c73e-114">Remarks</span></span>

<span data-ttu-id="0c73e-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für die messaging-Benutzer, die vom Absender angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0c73e-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="0c73e-116">Wenn eine Clientanwendung eine Nachricht im Auftrag einer anderen Client sendet, sollten sie alle Absender dargestellte Eigenschaften auf die Werte für diesen Client festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0c73e-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="0c73e-117">Ein messaging-Benutzer in der Regel in einem eigenen Auftrag senden bewirkt, dass die dargestellte Absender Eigenschaften nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0c73e-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="0c73e-118">Der ausgehende Adressbuchhierarchie muss immer lassen Sie diese Eigenschaften geändert, wenn es vom sendenden Client festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="0c73e-118">The outgoing transport provider must always leave these properties unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="0c73e-119">Wenn es nicht festgelegt ist, sollte der Adressbuchhierarchie legen Sie es an die **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))-Eigenschaft für die ausgehende Kopie der Nachricht, und klicken Sie auf die lokale Kopie nicht festgelegt lassen.</span><span class="sxs-lookup"><span data-stu-id="0c73e-119">If it is unset, the transport provider should set it to the **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0c73e-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0c73e-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0c73e-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0c73e-121">Protocol specifications</span></span>

<span data-ttu-id="0c73e-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c73e-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c73e-123">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="0c73e-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0c73e-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c73e-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c73e-125">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="0c73e-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="0c73e-126">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c73e-126">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c73e-127">Gibt die Eigenschaften und Operationen, die RSS-Elemente darstellen.</span><span class="sxs-lookup"><span data-stu-id="0c73e-127">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="0c73e-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c73e-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c73e-129">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="0c73e-129">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="0c73e-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c73e-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c73e-131">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="0c73e-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="0c73e-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c73e-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c73e-133">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="0c73e-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="0c73e-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c73e-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c73e-135">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="0c73e-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="0c73e-136">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c73e-136">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c73e-137">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="0c73e-137">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0c73e-138">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="0c73e-138">Header files</span></span>

<span data-ttu-id="0c73e-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0c73e-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="0c73e-140">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0c73e-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="0c73e-141">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0c73e-141">Mapitags.h</span></span>
  
> <span data-ttu-id="0c73e-142">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0c73e-142">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0c73e-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c73e-143">See also</span></span>



[<span data-ttu-id="0c73e-144">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0c73e-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0c73e-145">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0c73e-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0c73e-146">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0c73e-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0c73e-147">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0c73e-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

