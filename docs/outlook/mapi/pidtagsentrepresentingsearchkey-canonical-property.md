---
title: PidTagSentRepresentingSearchKey (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingSearchKey
api_type:
- COM
ms.assetid: 7a49b944-cef1-4642-9208-b137fd61171a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a9361f3027453742acbe50c3de01d860289cd0ed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356686"
---
# <a name="pidtagsentrepresentingsearchkey-canonical-property"></a><span data-ttu-id="0f612-103">PidTagSentRepresentingSearchKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0f612-103">PidTagSentRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="0f612-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f612-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f612-105">Enthält den Suchschlüssel für den Messagingbenutzer, der durch den Absender dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="0f612-105">Contains the search key for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0f612-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0f612-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0f612-107">PR_SENT_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="0f612-107">PR_SENT_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="0f612-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="0f612-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0f612-109">0x003B</span><span class="sxs-lookup"><span data-stu-id="0f612-109">0x003B</span></span>  <br/> |
|<span data-ttu-id="0f612-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0f612-110">Data type:</span></span>  <br/> |<span data-ttu-id="0f612-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0f612-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0f612-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0f612-112">Area:</span></span>  <br/> |<span data-ttu-id="0f612-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="0f612-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f612-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0f612-114">Remarks</span></span>

<span data-ttu-id="0f612-115">Diese Eigenschaft ist eine der Adresseigenschaften für den Messagingbenutzer, der vom Absender dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="0f612-115">This property is one of the address properties for the messaging user who is being represented by the sender.</span></span> <span data-ttu-id="0f612-116">Wenn eine Clientanwendung eine Nachricht im Namen eines anderen Clients sendet, sollte sie alle dargestellten Absendereigenschaften auf die Werte für den Client festlegen.</span><span class="sxs-lookup"><span data-stu-id="0f612-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="0f612-117">Ein Messagingbenutzer, der in seinem eigenen Namen sendet, überlässt in der Regel die dargestellten Absendereigenschaften nicht.</span><span class="sxs-lookup"><span data-stu-id="0f612-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="0f612-118">Der ausgehende Transportanbieter muss diese Eigenschaft immer unverändert lassen, wenn sie vom sendenden Client festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="0f612-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="0f612-119">Wenn sie nicht festgelegt ist, sollte der Transportanbieter sie auf **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) für die ausgehende Kopie der Nachricht festlegen und sie in der lokalen Kopie nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="0f612-119">If it is unset, the transport provider should set it to **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0f612-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0f612-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0f612-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0f612-121">Protocol specifications</span></span>

<span data-ttu-id="0f612-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f612-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f612-123">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="0f612-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0f612-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f612-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f612-125">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="0f612-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="0f612-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f612-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f612-127">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="0f612-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="0f612-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f612-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f612-129">Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.</span><span class="sxs-lookup"><span data-stu-id="0f612-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="0f612-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f612-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f612-131">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="0f612-131">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="0f612-132">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f612-132">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f612-133">Gibt die Eigenschaften und Vorgänge an, die für Postobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="0f612-133">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="0f612-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f612-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f612-135">Gibt die Eigenschaften und Vorgänge an, die für Kontakt- und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="0f612-135">Specifies the properties and operations that are permissible for contact and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0f612-136">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="0f612-136">Header files</span></span>

<span data-ttu-id="0f612-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0f612-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="0f612-138">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0f612-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="0f612-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0f612-139">Mapitags.h</span></span>
  
> <span data-ttu-id="0f612-140">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="0f612-140">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0f612-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f612-141">See also</span></span>



[<span data-ttu-id="0f612-142">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0f612-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0f612-143">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="0f612-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0f612-144">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0f612-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0f612-145">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0f612-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

