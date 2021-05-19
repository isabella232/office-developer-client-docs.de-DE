---
title: PidTagSentRepresentingSmtpAddress (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5ed122a2-0967-4de3-a2ee-69f81ae77b16
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a9114b1c9c3f5b09c5636f7d55d7111dd86afc06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341937"
---
# <a name="pidtagsentrepresentingsmtpaddress-canonical-property"></a><span data-ttu-id="9c347-103">PidTagSentRepresentingSmtpAddress (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9c347-103">PidTagSentRepresentingSmtpAddress Canonical Property</span></span>

  
  
<span data-ttu-id="9c347-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c347-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c347-105">Enthält die SMTP-E-Mail-Adresse (Simple Mail Transport Protocol) für den Messagingbenutzer, der durch den Absender dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="9c347-105">Contains the Simple Mail Transport Protocol (SMTP) email address for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9c347-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9c347-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9c347-107">PR_SENT_REPRESENTING_SMTP_ADDRESS, PR_SENT_REPRESENTING_SMTP_ADDRESS_A, PR_SENT_REPRESENTING_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="9c347-107">PR_SENT_REPRESENTING_SMTP_ADDRESS, PR_SENT_REPRESENTING_SMTP_ADDRESS_A, PR_SENT_REPRESENTING_SMTP_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="9c347-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="9c347-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9c347-109">0x5D02</span><span class="sxs-lookup"><span data-stu-id="9c347-109">0x5D02</span></span>  <br/> |
|<span data-ttu-id="9c347-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9c347-110">Data type:</span></span>  <br/> |<span data-ttu-id="9c347-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="9c347-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="9c347-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9c347-112">Area:</span></span>  <br/> |<span data-ttu-id="9c347-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="9c347-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9c347-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9c347-114">Remarks</span></span>

<span data-ttu-id="9c347-115">Diese Eigenschaft ist ein Beispiel für die Adresseigenschaften für den Messagingbenutzer, der vom Absender dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="9c347-115">This property is an example of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="9c347-116">Wenn eine Clientanwendung eine Nachricht im Namen eines anderen Clients sendet, sollte sie alle dargestellten Absendereigenschaften auf die Werte für den Client festlegen.</span><span class="sxs-lookup"><span data-stu-id="9c347-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="9c347-117">Ein Messagingbenutzer, der in seinem eigenen Namen sendet, überlässt in der Regel die dargestellten Absendereigenschaften nicht.</span><span class="sxs-lookup"><span data-stu-id="9c347-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="9c347-118">Der ausgehende Transportanbieter muss diese Eigenschaft immer unverändert lassen, wenn sie vom sendenden Client festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="9c347-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="9c347-119">Wenn dies nicht festgelegt ist, sollte der Transportanbieter die Eigenschaft **PR_SENDER_SMTP_ADDRESS** ([PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)) für die ausgehende Kopie der Nachricht festlegen und sie in der lokalen Kopie nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="9c347-119">If it is unset, the transport provider should set it to the **PR_SENDER_SMTP_ADDRESS** ([PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9c347-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9c347-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9c347-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="9c347-121">Protocol specifications</span></span>

<span data-ttu-id="9c347-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9c347-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9c347-123">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="9c347-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9c347-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9c347-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9c347-125">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="9c347-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="9c347-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9c347-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9c347-127">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="9c347-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="9c347-128">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9c347-128">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9c347-129">Gibt Methoden zum Verbinden und Konfigurieren von Postfächern als Stellvertretung sowie Interaktionen mit Nachrichten- und Kalenderobjekten an, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="9c347-129">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="9c347-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9c347-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9c347-131">Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.</span><span class="sxs-lookup"><span data-stu-id="9c347-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="9c347-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9c347-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9c347-133">Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="9c347-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="9c347-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9c347-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9c347-135">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="9c347-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="9c347-136">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9c347-136">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9c347-137">Codiert und decodiert Nachrichten- und Anlagenobjekte in eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="9c347-137">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9c347-138">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="9c347-138">Header files</span></span>

<span data-ttu-id="9c347-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9c347-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="9c347-140">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9c347-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="9c347-141">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9c347-141">Mapitags.h</span></span>
  
> <span data-ttu-id="9c347-142">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="9c347-142">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9c347-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c347-143">See also</span></span>



[<span data-ttu-id="9c347-144">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9c347-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9c347-145">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="9c347-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9c347-146">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9c347-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9c347-147">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9c347-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

