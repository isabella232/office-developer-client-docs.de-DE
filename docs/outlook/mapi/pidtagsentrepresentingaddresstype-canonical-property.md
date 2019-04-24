---
title: Kanonische Pidtagsentrepresentingaddresstype (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: bbf1ae0d7b38886fe08af2ad13f1a2be6b6e01cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342574"
---
# <a name="pidtagsentrepresentingaddresstype-canonical-property"></a><span data-ttu-id="c57a3-103">Kanonische Pidtagsentrepresentingaddresstype (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c57a3-103">PidTagSentRepresentingAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="c57a3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c57a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c57a3-105">Enthält den Adresstyp für den Messagingbenutzer, der vom Absender repräsentiert wird.</span><span class="sxs-lookup"><span data-stu-id="c57a3-105">Contains the address type for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c57a3-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c57a3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c57a3-107">PR_SENT_REPRESENTING_ADDRTYPE, PR_SENT_REPRESENTING_ADDRTYPE_A, PR_SENT_REPRESENTING_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="c57a3-107">PR_SENT_REPRESENTING_ADDRTYPE, PR_SENT_REPRESENTING_ADDRTYPE_A, PR_SENT_REPRESENTING_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="c57a3-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="c57a3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c57a3-109">0x0064</span><span class="sxs-lookup"><span data-stu-id="c57a3-109">0x0064</span></span>  <br/> |
|<span data-ttu-id="c57a3-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c57a3-110">Data type:</span></span>  <br/> |<span data-ttu-id="c57a3-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="c57a3-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="c57a3-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c57a3-112">Area:</span></span>  <br/> |<span data-ttu-id="c57a3-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="c57a3-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c57a3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c57a3-114">Remarks</span></span>

<span data-ttu-id="c57a3-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den Messagingbenutzer, der vom Absender dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c57a3-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="c57a3-116">Wenn eine Clientanwendung eine Nachricht im Auftrag eines anderen Clients sendet, sollte Sie alle dargestellten Absender Eigenschaften auf die Werte für diesen Client festlegen.</span><span class="sxs-lookup"><span data-stu-id="c57a3-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="c57a3-117">Ein Messagingbenutzer, der im eigenen Namen sendet, lässt die dargestellten Absender Eigenschaften in der Regel nicht unset.</span><span class="sxs-lookup"><span data-stu-id="c57a3-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="c57a3-118">Der ausgehende Transportanbieter muss diese Eigenschaft immer unverändert lassen, wenn Sie vom sendenden Client festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="c57a3-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="c57a3-119">Wenn Sie nicht festgelegt ist, sollte der Transportanbieter Sie auf die **PR_SENDER_ADDRTYPE** ([pidtagsenderaddresstype (](pidtagsenderaddresstype-canonical-property.md))-Eigenschaft der ausgehenden Kopie der Nachricht festlegen und Sie in der lokalen Kopie nicht löschen lassen.</span><span class="sxs-lookup"><span data-stu-id="c57a3-119">If it is unset, the transport provider should set it to the **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c57a3-120">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c57a3-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c57a3-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c57a3-121">Protocol specifications</span></span>

<span data-ttu-id="c57a3-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c57a3-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c57a3-123">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="c57a3-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c57a3-124">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c57a3-124">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c57a3-125">Verarbeitet die Reihenfolge und den Ablauf für die Datenübertragung zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="c57a3-125">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="c57a3-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c57a3-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c57a3-127">Konvertiert zwischen IETF-RFC2445, RFC2446 und RFC2447 sowie Termin-und Besprechungs Objekten.</span><span class="sxs-lookup"><span data-stu-id="c57a3-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="c57a3-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c57a3-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c57a3-129">Konvertiert von Internet Standard-e-Mail-Konventionen in Nachrichtenobjekte.</span><span class="sxs-lookup"><span data-stu-id="c57a3-129">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="c57a3-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c57a3-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c57a3-131">Gibt Methoden zum Herstellen einer Verbindung mit und Konfigurieren von Postfächern als Stellvertreter sowie Interaktionen mit Nachrichten-und Kalenderobjekten an, wenn Sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="c57a3-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="c57a3-132">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c57a3-132">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c57a3-133">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="c57a3-133">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="c57a3-134">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c57a3-134">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c57a3-135">Gibt die Eigenschaften und Vorgänge an, die für Post-Objekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="c57a3-135">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="c57a3-136">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c57a3-136">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c57a3-137">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="c57a3-137">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="c57a3-138">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c57a3-138">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c57a3-139">Codiert und dekodiert Message-und Attachment-Objekte in einer effizienten Datenstrom Darstellung.</span><span class="sxs-lookup"><span data-stu-id="c57a3-139">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c57a3-140">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="c57a3-140">Header files</span></span>

<span data-ttu-id="c57a3-141">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c57a3-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="c57a3-142">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="c57a3-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="c57a3-143">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="c57a3-143">Mapitags.h</span></span>
  
> <span data-ttu-id="c57a3-144">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="c57a3-144">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c57a3-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c57a3-145">See also</span></span>



[<span data-ttu-id="c57a3-146">Kanonische Pidtagaddresstype (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c57a3-146">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)


[<span data-ttu-id="c57a3-147">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c57a3-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c57a3-148">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c57a3-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c57a3-149">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c57a3-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c57a3-150">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c57a3-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

