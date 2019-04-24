---
title: Kanonische Pidtagsentrepresentingentryid (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 87d8fa21ed641b40ee679a4b5fc8d68b1050ab0e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359087"
---
# <a name="pidtagsentrepresentingentryid-canonical-property"></a><span data-ttu-id="e8554-103">Kanonische Pidtagsentrepresentingentryid (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e8554-103">PidTagSentRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="e8554-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8554-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8554-105">Enthält die Eintrags-ID für den vom Absender dargestellten Messagingbenutzer.</span><span class="sxs-lookup"><span data-stu-id="e8554-105">Contains the entry identifier for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e8554-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e8554-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e8554-107">PR_SENT_REPRESENTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e8554-107">PR_SENT_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="e8554-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e8554-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e8554-109">0x0041</span><span class="sxs-lookup"><span data-stu-id="e8554-109">0x0041</span></span>  <br/> |
|<span data-ttu-id="e8554-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e8554-110">Data type:</span></span>  <br/> |<span data-ttu-id="e8554-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e8554-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e8554-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e8554-112">Area:</span></span>  <br/> |<span data-ttu-id="e8554-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="e8554-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8554-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8554-114">Remarks</span></span>

<span data-ttu-id="e8554-115">Diese Eigenschaft ist eine der Adresseigenschaften für den Messagingbenutzer, der vom Absender dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e8554-115">This property is one of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="e8554-116">Wenn eine Clientanwendung eine Nachricht im Auftrag eines anderen Clients sendet, sollte Sie alle dargestellten Absender Eigenschaften auf die Werte für diesen Client festlegen.</span><span class="sxs-lookup"><span data-stu-id="e8554-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="e8554-117">Ein Messagingbenutzer, der im eigenen Namen sendet, lässt die dargestellten Absender Eigenschaften in der Regel nicht unset.</span><span class="sxs-lookup"><span data-stu-id="e8554-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="e8554-118">Der ausgehende Transportanbieter muss diese Eigenschaft immer unverändert lassen, wenn Sie vom sendenden Client festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="e8554-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="e8554-119">Wenn Sie nicht festgelegt ist, sollte der Transportanbieter Sie auf **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) für die ausgehende Kopie der Nachricht festlegen und Sie in der lokalen Kopie nicht löschen lassen.</span><span class="sxs-lookup"><span data-stu-id="e8554-119">If it is unset, the transport provider should set it to **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e8554-120">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e8554-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e8554-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e8554-121">Protocol specifications</span></span>

<span data-ttu-id="e8554-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8554-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e8554-123">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e8554-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e8554-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8554-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e8554-125">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="e8554-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="e8554-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8554-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e8554-127">Verarbeitet die Reihenfolge und den Ablauf für die Datenübertragung zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="e8554-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="e8554-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8554-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e8554-129">Konvertiert zwischen IETF-RFC2445, RFC2446 und RFC2447 sowie Termin-und Besprechungs Objekten.</span><span class="sxs-lookup"><span data-stu-id="e8554-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="e8554-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8554-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e8554-131">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="e8554-131">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="e8554-132">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8554-132">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e8554-133">Gibt Methoden zum Herstellen einer Verbindung mit und Konfigurieren von Postfächern als Stellvertreter sowie Interaktionen mit Nachrichten-und Kalenderobjekten an, wenn Sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="e8554-133">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="e8554-134">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8554-134">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e8554-135">Gibt die Eigenschaften und Vorgänge an, die für Post-Objekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="e8554-135">Specifies the properties and operations that are permissible for post objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e8554-136">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="e8554-136">Header files</span></span>

<span data-ttu-id="e8554-137">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e8554-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="e8554-138">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="e8554-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="e8554-139">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e8554-139">Mapitags.h</span></span>
  
> <span data-ttu-id="e8554-140">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="e8554-140">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e8554-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8554-141">See also</span></span>



[<span data-ttu-id="e8554-142">Kanonische PidTagEntryId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e8554-142">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)


[<span data-ttu-id="e8554-143">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e8554-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e8554-144">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e8554-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e8554-145">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e8554-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e8554-146">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e8554-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

