---
title: Kanonische PidTagSentRepresentingSearchKey-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d18a595a1019c3bd583ef0c38ee5cbe0d497bf93
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795139"
---
# <a name="pidtagsentrepresentingsearchkey-canonical-property"></a><span data-ttu-id="30fc9-103">Kanonische PidTagSentRepresentingSearchKey-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="30fc9-103">PidTagSentRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="30fc9-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="30fc9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="30fc9-105">Enthält den Search-Schlüssel für die messaging-Benutzer vom Absender dargestellt.</span><span class="sxs-lookup"><span data-stu-id="30fc9-105">Contains the search key for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="30fc9-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="30fc9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="30fc9-107">PR_SENT_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="30fc9-107">PR_SENT_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="30fc9-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="30fc9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="30fc9-109">0x003B</span><span class="sxs-lookup"><span data-stu-id="30fc9-109">0x003B</span></span>  <br/> |
|<span data-ttu-id="30fc9-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="30fc9-110">Data type:</span></span>  <br/> |<span data-ttu-id="30fc9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="30fc9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="30fc9-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="30fc9-112">Area:</span></span>  <br/> |<span data-ttu-id="30fc9-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="30fc9-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30fc9-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="30fc9-114">Remarks</span></span>

<span data-ttu-id="30fc9-115">Diese Eigenschaft ist eine der Adresseigenschaften für den messaging-Benutzer, die vom Absender dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="30fc9-115">This property is one of the address properties for the messaging user who is being represented by the sender.</span></span> <span data-ttu-id="30fc9-116">Wenn eine Clientanwendung eine Nachricht im Auftrag einer anderen Client sendet, sollten sie alle Absender dargestellte Eigenschaften auf die Werte für diesen Client festgelegt.</span><span class="sxs-lookup"><span data-stu-id="30fc9-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="30fc9-117">Ein messaging-Benutzer in der Regel in einem eigenen Auftrag senden bewirkt, dass die dargestellte Absender Eigenschaften nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="30fc9-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="30fc9-118">Der ausgehende Adressbuchhierarchie muss immer lassen Sie diese Eigenschaft geändert, wenn es vom sendenden Client festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="30fc9-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="30fc9-119">Wenn es nicht festgelegt ist, sollte der Adressbuchhierarchie für die ausgehende Kopie der Nachricht auf **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) festlegen, und der lokalen Kopie nicht festgelegt lassen.</span><span class="sxs-lookup"><span data-stu-id="30fc9-119">If it is unset, the transport provider should set it to **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="30fc9-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="30fc9-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="30fc9-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="30fc9-121">Protocol specifications</span></span>

<span data-ttu-id="30fc9-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30fc9-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30fc9-123">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="30fc9-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="30fc9-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30fc9-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30fc9-125">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="30fc9-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="30fc9-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30fc9-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30fc9-127">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="30fc9-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="30fc9-128">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30fc9-128">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30fc9-129">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="30fc9-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="30fc9-130">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30fc9-130">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30fc9-131">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="30fc9-131">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="30fc9-132">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30fc9-132">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30fc9-133">Gibt an, die Eigenschaften und Vorgänge, die für zulässige sind Objekte bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="30fc9-133">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="30fc9-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30fc9-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30fc9-135">Gibt die Eigenschaften und Operationen, die für zu kontaktieren und persönlichen Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="30fc9-135">Specifies the properties and operations that are permissible for contact and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="30fc9-136">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="30fc9-136">Header files</span></span>

<span data-ttu-id="30fc9-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="30fc9-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="30fc9-138">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="30fc9-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="30fc9-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="30fc9-139">Mapitags.h</span></span>
  
> <span data-ttu-id="30fc9-140">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="30fc9-140">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="30fc9-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30fc9-141">See also</span></span>



[<span data-ttu-id="30fc9-142">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="30fc9-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="30fc9-143">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="30fc9-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="30fc9-144">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="30fc9-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="30fc9-145">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="30fc9-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

