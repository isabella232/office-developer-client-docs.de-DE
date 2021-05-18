---
title: PidTagSentRepresentingName (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: bfee6c5e-d4c6-442e-af71-23156569fed5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8e2df13f4e9c5d1d636c4f71ea6805ac031899e9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314931"
---
# <a name="pidtagsentrepresentingname-canonical-property"></a><span data-ttu-id="8d7e2-103">PidTagSentRepresentingName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8d7e2-103">PidTagSentRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="8d7e2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d7e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d7e2-105">Enthält den Anzeigenamen für den Messagingbenutzer, der durch den Absender dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8d7e2-105">Contains the display name for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8d7e2-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8d7e2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8d7e2-107">PR_SENT_REPRESENTING_NAME, PR_SENT_REPRESENTING_NAME_A, PR_SENT_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="8d7e2-107">PR_SENT_REPRESENTING_NAME, PR_SENT_REPRESENTING_NAME_A, PR_SENT_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="8d7e2-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="8d7e2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8d7e2-109">0x0042</span><span class="sxs-lookup"><span data-stu-id="8d7e2-109">0x0042</span></span>  <br/> |
|<span data-ttu-id="8d7e2-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8d7e2-110">Data type:</span></span>  <br/> |<span data-ttu-id="8d7e2-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="8d7e2-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="8d7e2-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8d7e2-112">Area:</span></span>  <br/> |<span data-ttu-id="8d7e2-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="8d7e2-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d7e2-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8d7e2-114">Remarks</span></span>

<span data-ttu-id="8d7e2-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den Messagingbenutzer, der vom Absender dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8d7e2-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="8d7e2-116">Wenn eine Clientanwendung eine Nachricht im Namen eines anderen Clients sendet, sollte sie alle dargestellten Absendereigenschaften auf die Werte für den Client festlegen.</span><span class="sxs-lookup"><span data-stu-id="8d7e2-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="8d7e2-117">Ein Messagingbenutzer, der in seinem eigenen Namen sendet, überlässt in der Regel die dargestellten Absendereigenschaften nicht.</span><span class="sxs-lookup"><span data-stu-id="8d7e2-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="8d7e2-118">Der ausgehende Transportanbieter muss diese Eigenschaft immer unverändert lassen, wenn sie vom sendenden Client festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="8d7e2-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="8d7e2-119">Wenn dies nicht festgelegt ist, sollte der Transportanbieter ihn auf **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) für die ausgehende Kopie der Nachricht festlegen und die lokale Kopie nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d7e2-119">If it is unset, the transport provider should set it to **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8d7e2-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8d7e2-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8d7e2-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="8d7e2-121">Protocol specifications</span></span>

<span data-ttu-id="8d7e2-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d7e2-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d7e2-123">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="8d7e2-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8d7e2-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/cc433482%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d7e2-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/cc433482%28EXCHG.80%29.aspx)</span></span>
  
> <span data-ttu-id="8d7e2-125">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="8d7e2-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="8d7e2-126">[[MS-OXORSS]](https://msdn.microsoft.com/library/cc463884%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d7e2-126">[[MS-OXORSS]](https://msdn.microsoft.com/library/cc463884%28EXCHG.80%29.aspx)</span></span>
  
> <span data-ttu-id="8d7e2-127">Gibt die Eigenschaften und Vorgänge an, die RSS-Elemente darstellen.</span><span class="sxs-lookup"><span data-stu-id="8d7e2-127">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="8d7e2-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d7e2-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d7e2-129">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="8d7e2-129">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="8d7e2-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d7e2-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d7e2-131">Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.</span><span class="sxs-lookup"><span data-stu-id="8d7e2-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="8d7e2-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d7e2-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d7e2-133">Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="8d7e2-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="8d7e2-134">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d7e2-134">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d7e2-135">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="8d7e2-135">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="8d7e2-136">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d7e2-136">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d7e2-137">Gibt den Speicherort und die Eigenschaften von Client- und Serverkonfigurationsdaten an, z. B. freigegebene Kategorielisten und Arbeitszeiten.</span><span class="sxs-lookup"><span data-stu-id="8d7e2-137">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
<span data-ttu-id="8d7e2-138">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d7e2-138">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d7e2-139">Gibt Methoden zum Verbinden und Konfigurieren von Postfächern als Stellvertretung sowie Interaktionen mit Nachrichten- und Kalenderobjekten an, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="8d7e2-139">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="8d7e2-140">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d7e2-140">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d7e2-141">Gibt die Eigenschaften und Vorgänge an, die für Postobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="8d7e2-141">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="8d7e2-142">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d7e2-142">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d7e2-143">Gibt die Eigenschaften und Vorgänge an, die für Kontakt- und persönliche Verteilerlistenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="8d7e2-143">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="8d7e2-144">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d7e2-144">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d7e2-145">Codiert und decodiert Nachrichten- und Anlagenobjekte in eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="8d7e2-145">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8d7e2-146">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="8d7e2-146">Header files</span></span>

<span data-ttu-id="8d7e2-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8d7e2-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="8d7e2-148">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="8d7e2-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="8d7e2-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8d7e2-149">Mapitags.h</span></span>
  
> <span data-ttu-id="8d7e2-150">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="8d7e2-150">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8d7e2-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d7e2-151">See also</span></span>



[<span data-ttu-id="8d7e2-152">PidTagDisplayName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8d7e2-152">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="8d7e2-153">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8d7e2-153">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8d7e2-154">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="8d7e2-154">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8d7e2-155">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8d7e2-155">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8d7e2-156">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8d7e2-156">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

