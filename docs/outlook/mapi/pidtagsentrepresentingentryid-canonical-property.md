---
title: PidTagSentRepresentingEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingEntryId
api_type:
- COM
ms.assetid: f23bde8b-94cc-48c8-891a-166aa39aa3ee
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1afb34dace1b28053b185bc25a495a19e48ec1c6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577821"
---
# <a name="pidtagsentrepresentingentryid-canonical-property"></a><span data-ttu-id="801b5-103">PidTagSentRepresentingEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="801b5-103">PidTagSentRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="801b5-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="801b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="801b5-105">Enthält die Eintrags-ID für den messaging Benutzer, die vom Absender dargestellt.</span><span class="sxs-lookup"><span data-stu-id="801b5-105">Contains the entry identifier for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="801b5-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="801b5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="801b5-107">PR_SENT_REPRESENTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="801b5-107">PR_SENT_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="801b5-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="801b5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="801b5-109">0x0041</span><span class="sxs-lookup"><span data-stu-id="801b5-109">0x0041</span></span>  <br/> |
|<span data-ttu-id="801b5-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="801b5-110">Data type:</span></span>  <br/> |<span data-ttu-id="801b5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="801b5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="801b5-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="801b5-112">Area:</span></span>  <br/> |<span data-ttu-id="801b5-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="801b5-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="801b5-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="801b5-114">Remarks</span></span>

<span data-ttu-id="801b5-115">Diese Eigenschaft ist eine der Eigenschaften für die messaging-Benutzer, die vom Absender angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="801b5-115">This property is one of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="801b5-116">Wenn eine Clientanwendung eine Nachricht im Auftrag einer anderen Client sendet, sollten sie alle Absender dargestellte Eigenschaften auf die Werte für diesen Client festgelegt.</span><span class="sxs-lookup"><span data-stu-id="801b5-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="801b5-117">Ein messaging-Benutzer in der Regel in einem eigenen Auftrag senden bewirkt, dass die dargestellte Absender Eigenschaften nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="801b5-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="801b5-118">Der ausgehende Adressbuchhierarchie muss immer lassen Sie diese Eigenschaft geändert, wenn es vom sendenden Client festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="801b5-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="801b5-119">Wenn es nicht festgelegt ist, sollte der Adressbuchhierarchie für die ausgehende Kopie der Nachricht auf **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) festlegen, und der lokalen Kopie nicht festgelegt lassen.</span><span class="sxs-lookup"><span data-stu-id="801b5-119">If it is unset, the transport provider should set it to **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="801b5-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="801b5-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="801b5-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="801b5-121">Protocol specifications</span></span>

<span data-ttu-id="801b5-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="801b5-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="801b5-123">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="801b5-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="801b5-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="801b5-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="801b5-125">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="801b5-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="801b5-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="801b5-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="801b5-127">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="801b5-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="801b5-128">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="801b5-128">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="801b5-129">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="801b5-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="801b5-130">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="801b5-130">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="801b5-131">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="801b5-131">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="801b5-132">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="801b5-132">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="801b5-133">Gibt die Methoden zum Herstellen einer Verbindung mit und Konfiguration von Postfächer als Stellvertretungen und Interaktionen mit Nachricht und Kalender-Objekte, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="801b5-133">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="801b5-134">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="801b5-134">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="801b5-135">Gibt an, die Eigenschaften und Vorgänge, die für zulässige sind Objekte bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="801b5-135">Specifies the properties and operations that are permissible for post objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="801b5-136">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="801b5-136">Header files</span></span>

<span data-ttu-id="801b5-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="801b5-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="801b5-138">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="801b5-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="801b5-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="801b5-139">Mapitags.h</span></span>
  
> <span data-ttu-id="801b5-140">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="801b5-140">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="801b5-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="801b5-141">See also</span></span>



[<span data-ttu-id="801b5-142">PidTagEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="801b5-142">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)


[<span data-ttu-id="801b5-143">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="801b5-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="801b5-144">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="801b5-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="801b5-145">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="801b5-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="801b5-146">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="801b5-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

