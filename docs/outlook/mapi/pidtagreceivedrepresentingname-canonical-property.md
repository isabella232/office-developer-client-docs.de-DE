---
title: Kanonische PidTagReceivedRepresentingName-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingName
api_type:
- COM
ms.assetid: 8f699782-8a82-4834-bc55-a0b3cf18a117
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0df2cef2f82523fd5085f5567cac41dab860916d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794895"
---
# <a name="pidtagreceivedrepresentingname-canonical-property"></a><span data-ttu-id="e50ba-103">Kanonische PidTagReceivedRepresentingName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e50ba-103">PidTagReceivedRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="e50ba-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e50ba-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e50ba-105">Enthält den Anzeigenamen für den messaging-Benutzer, die von der empfangenden Benutzer dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e50ba-105">Contains the display name for the messaging user who is represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e50ba-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e50ba-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e50ba-107">PR_RCVD_REPRESENTING_NAME, PR_RCVD_REPRESENTING_NAME_A, PR_RCVD_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="e50ba-107">PR_RCVD_REPRESENTING_NAME, PR_RCVD_REPRESENTING_NAME_A, PR_RCVD_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="e50ba-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="e50ba-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e50ba-109">0x0044</span><span class="sxs-lookup"><span data-stu-id="e50ba-109">0x0044</span></span>  <br/> |
|<span data-ttu-id="e50ba-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e50ba-110">Data type:</span></span>  <br/> |<span data-ttu-id="e50ba-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="e50ba-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="e50ba-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e50ba-112">Area:</span></span>  <br/> |<span data-ttu-id="e50ba-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="e50ba-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e50ba-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e50ba-114">Remarks</span></span>

<span data-ttu-id="e50ba-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den messaging-Benutzer, die von der empfangenden Benutzer dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e50ba-115">These properties are examples of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="e50ba-116">Sie müssen von der eingehenden Adressbuchhierarchie festgelegt werden, die auch für die Autorisierung oder Überprüfung des Delegaten zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="e50ba-116">They must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="e50ba-117">Wenn kein messaging Benutzer dargestellt wird, sollte der Anzeigename, die in der Eigenschaft **PR_RECEIVED_BY_NAME** ([PidTagReceivedByName](pidtagreceivedbyname-canonical-property.md)) enthalten sind diese Eigenschaften fest.</span><span class="sxs-lookup"><span data-stu-id="e50ba-117">If no messaging user is being represented, these properties should be set to the display name contained in the **PR_RECEIVED_BY_NAME** ([PidTagReceivedByName](pidtagreceivedbyname-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="e50ba-118">Ein Client Application Antworten auf eine Nachricht im Auftrag einer anderen Client empfangene sollten diese Eigenschaften in die Eigenschaft **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) für die Antwort aus der empfangenen Nachricht kopieren.</span><span class="sxs-lookup"><span data-stu-id="e50ba-118">A client application replying to a message received on behalf of another client should copy these properties from the received message into the **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e50ba-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e50ba-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e50ba-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e50ba-120">Protocol specifications</span></span>

<span data-ttu-id="e50ba-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e50ba-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e50ba-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e50ba-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e50ba-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e50ba-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e50ba-124">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="e50ba-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="e50ba-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e50ba-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e50ba-126">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="e50ba-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="e50ba-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e50ba-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e50ba-128">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="e50ba-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="e50ba-129">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e50ba-129">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e50ba-130">Gibt die Methoden zum Herstellen einer Verbindung mit und Konfiguration von Postfächer als Stellvertretungen und Interaktionen mit Nachricht und Kalender-Objekte, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="e50ba-130">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="e50ba-131">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e50ba-131">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e50ba-132">Codiert und decodiert Nachrichten- und Objekte, die auf eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="e50ba-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e50ba-133">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="e50ba-133">Header files</span></span>

<span data-ttu-id="e50ba-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e50ba-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="e50ba-135">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e50ba-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="e50ba-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e50ba-136">Mapitags.h</span></span>
  
> <span data-ttu-id="e50ba-137">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e50ba-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e50ba-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e50ba-138">See also</span></span>



[<span data-ttu-id="e50ba-139">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e50ba-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e50ba-140">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e50ba-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e50ba-141">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e50ba-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e50ba-142">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e50ba-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
