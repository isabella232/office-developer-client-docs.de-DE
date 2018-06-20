---
title: Kanonische PidTagSentRepresentingName-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: bfee6c5e-d4c6-442e-af71-23156569fed5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5417b73fe13937a74bc01520a2dd9db359e894ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795157"
---
# <a name="pidtagsentrepresentingname-canonical-property"></a><span data-ttu-id="34e0c-103">Kanonische PidTagSentRepresentingName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="34e0c-103">PidTagSentRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="34e0c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="34e0c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="34e0c-105">Enthält den Anzeigenamen für die messaging-Benutzer vom Absender dargestellt.</span><span class="sxs-lookup"><span data-stu-id="34e0c-105">Contains the display name for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="34e0c-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="34e0c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="34e0c-107">PR_SENT_REPRESENTING_NAME, PR_SENT_REPRESENTING_NAME_A, PR_SENT_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="34e0c-107">PR_SENT_REPRESENTING_NAME, PR_SENT_REPRESENTING_NAME_A, PR_SENT_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="34e0c-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="34e0c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="34e0c-109">0x0042</span><span class="sxs-lookup"><span data-stu-id="34e0c-109">0x0042</span></span>  <br/> |
|<span data-ttu-id="34e0c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="34e0c-110">Data type:</span></span>  <br/> |<span data-ttu-id="34e0c-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="34e0c-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="34e0c-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="34e0c-112">Area:</span></span>  <br/> |<span data-ttu-id="34e0c-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="34e0c-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="34e0c-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="34e0c-114">Remarks</span></span>

<span data-ttu-id="34e0c-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für die messaging-Benutzer, die vom Absender angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="34e0c-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="34e0c-116">Wenn eine Clientanwendung eine Nachricht im Auftrag einer anderen Client sendet, sollten sie alle Absender dargestellte Eigenschaften auf die Werte für diesen Client festgelegt.</span><span class="sxs-lookup"><span data-stu-id="34e0c-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="34e0c-117">Ein messaging-Benutzer in der Regel in einem eigenen Auftrag senden bewirkt, dass die dargestellte Absender Eigenschaften nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="34e0c-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="34e0c-118">Der ausgehende Adressbuchhierarchie muss immer lassen Sie diese Eigenschaft geändert, wenn es vom sendenden Client festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="34e0c-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="34e0c-119">Wenn es nicht festgelegt ist, sollte der Adressbuchhierarchie für die ausgehende Kopie der Nachricht auf **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) festlegen, und der lokalen Kopie nicht festgelegt lassen.</span><span class="sxs-lookup"><span data-stu-id="34e0c-119">If it is unset, the transport provider should set it to **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="34e0c-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="34e0c-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="34e0c-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="34e0c-121">Protocol specifications</span></span>

<span data-ttu-id="34e0c-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34e0c-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34e0c-123">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="34e0c-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="34e0c-124">[[MS-OXOMSG]](http://msdn.microsoft.com/en-us/library/cc433482%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34e0c-124">[[MS-OXOMSG]](http://msdn.microsoft.com/en-us/library/cc433482%28EXCHG.80%29.aspx)</span></span>
  
> <span data-ttu-id="34e0c-125">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="34e0c-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="34e0c-126">[[MS-OXORSS]](http://msdn.microsoft.com/en-us/library/cc463884%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34e0c-126">[[MS-OXORSS]](http://msdn.microsoft.com/en-us/library/cc463884%28EXCHG.80%29.aspx)</span></span>
  
> <span data-ttu-id="34e0c-127">Gibt die Eigenschaften und Operationen, die RSS-Elemente darstellen.</span><span class="sxs-lookup"><span data-stu-id="34e0c-127">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="34e0c-128">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34e0c-128">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34e0c-129">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="34e0c-129">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="34e0c-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34e0c-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34e0c-131">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="34e0c-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="34e0c-132">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34e0c-132">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34e0c-133">Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="34e0c-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="34e0c-134">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34e0c-134">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34e0c-135">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="34e0c-135">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="34e0c-136">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34e0c-136">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34e0c-137">Gibt den Speicherort und die Eigenschaften von Client- und Konfigurationsdaten, wie etwa freigegebene Kategorielisten und Arbeitszeiten.</span><span class="sxs-lookup"><span data-stu-id="34e0c-137">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
<span data-ttu-id="34e0c-138">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34e0c-138">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34e0c-139">Gibt die Methoden zum Herstellen einer Verbindung mit und Konfiguration von Postfächer als Stellvertretungen und Interaktionen mit Nachricht und Kalender-Objekte, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="34e0c-139">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="34e0c-140">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34e0c-140">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34e0c-141">Gibt an, die Eigenschaften und Vorgänge, die für zulässige sind Objekte bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="34e0c-141">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="34e0c-142">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34e0c-142">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34e0c-143">Gibt die Eigenschaften und Operationen, die für Kontakt- und Objekte in der persönlichen Verteilerliste Liste zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="34e0c-143">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="34e0c-144">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34e0c-144">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34e0c-145">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="34e0c-145">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="34e0c-146">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="34e0c-146">Header files</span></span>

<span data-ttu-id="34e0c-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="34e0c-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="34e0c-148">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="34e0c-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="34e0c-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="34e0c-149">Mapitags.h</span></span>
  
> <span data-ttu-id="34e0c-150">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="34e0c-150">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="34e0c-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34e0c-151">See also</span></span>



[<span data-ttu-id="34e0c-152">Kanonische PidTagDisplayName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="34e0c-152">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="34e0c-153">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="34e0c-153">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="34e0c-154">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="34e0c-154">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="34e0c-155">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="34e0c-155">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="34e0c-156">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="34e0c-156">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

