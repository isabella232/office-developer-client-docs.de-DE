---
title: PidTagReceivedRepresentingName (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5fce7e6d2163bdb8d1682dbef10d627b34ddd889
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356735"
---
# <a name="pidtagreceivedrepresentingname-canonical-property"></a><span data-ttu-id="de983-103">PidTagReceivedRepresentingName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="de983-103">PidTagReceivedRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="de983-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de983-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de983-105">Enthält den Anzeigenamen für den Messagingbenutzer, der vom empfangenden Benutzer dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="de983-105">Contains the display name for the messaging user who is represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="de983-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="de983-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="de983-107">PR_RCVD_REPRESENTING_NAME, PR_RCVD_REPRESENTING_NAME_A, PR_RCVD_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="de983-107">PR_RCVD_REPRESENTING_NAME, PR_RCVD_REPRESENTING_NAME_A, PR_RCVD_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="de983-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="de983-108">Identifier:</span></span>  <br/> |<span data-ttu-id="de983-109">0x0044</span><span class="sxs-lookup"><span data-stu-id="de983-109">0x0044</span></span>  <br/> |
|<span data-ttu-id="de983-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="de983-110">Data type:</span></span>  <br/> |<span data-ttu-id="de983-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="de983-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="de983-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="de983-112">Area:</span></span>  <br/> |<span data-ttu-id="de983-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="de983-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de983-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="de983-114">Remarks</span></span>

<span data-ttu-id="de983-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den Messagingbenutzer, der vom empfangenden Benutzer dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="de983-115">These properties are examples of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="de983-116">Sie müssen vom eingehenden Transportanbieter festgelegt werden, der auch für die Autorisierung oder Überprüfung der Stellvertretung zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="de983-116">They must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="de983-117">Wenn kein Messagingbenutzer dargestellt wird, sollten diese Eigenschaften auf den Anzeigenamen festgelegt werden, der in der **PR_RECEIVED_BY_NAME** ([PidTagReceivedByName](pidtagreceivedbyname-canonical-property.md)) -Eigenschaft enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="de983-117">If no messaging user is being represented, these properties should be set to the display name contained in the **PR_RECEIVED_BY_NAME** ([PidTagReceivedByName](pidtagreceivedbyname-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="de983-118">Eine Clientanwendung, die auf eine Nachricht antwortet, die im Namen eines anderen Clients empfangen wurde, sollte diese Eigenschaften aus der empfangenen Nachricht in die **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))-Eigenschaft für die Antwort kopieren.</span><span class="sxs-lookup"><span data-stu-id="de983-118">A client application replying to a message received on behalf of another client should copy these properties from the received message into the **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="de983-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="de983-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="de983-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="de983-120">Protocol specifications</span></span>

<span data-ttu-id="de983-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de983-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de983-122">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="de983-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="de983-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de983-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de983-124">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="de983-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="de983-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de983-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de983-126">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="de983-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="de983-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de983-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de983-128">Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.</span><span class="sxs-lookup"><span data-stu-id="de983-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="de983-129">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de983-129">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de983-130">Gibt Methoden zum Verbinden und Konfigurieren von Postfächern als Stellvertretung sowie Interaktionen mit Nachrichten- und Kalenderobjekten an, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="de983-130">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="de983-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de983-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de983-132">Codiert und decodiert Nachrichten- und Anlagenobjekte in eine effiziente Streamdarstellung.</span><span class="sxs-lookup"><span data-stu-id="de983-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="de983-133">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="de983-133">Header files</span></span>

<span data-ttu-id="de983-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="de983-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="de983-135">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="de983-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="de983-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="de983-136">Mapitags.h</span></span>
  
> <span data-ttu-id="de983-137">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="de983-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="de983-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de983-138">See also</span></span>



[<span data-ttu-id="de983-139">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="de983-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="de983-140">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="de983-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="de983-141">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="de983-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="de983-142">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="de983-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

