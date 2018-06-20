---
title: Kanonische PidTagReceivedRepresentingEntryId-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingEntryId
api_type:
- COM
ms.assetid: 2ae2266c-f093-41e5-b4d0-e12aa0f03190
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 12e4c97947cfe579f550cc6d48ca0b64750b9ab6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794883"
---
# <a name="pidtagreceivedrepresentingentryid-canonical-property"></a><span data-ttu-id="bc0ee-103">Kanonische PidTagReceivedRepresentingEntryId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bc0ee-103">PidTagReceivedRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="bc0ee-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bc0ee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bc0ee-105">Enthält die Eintrags-ID für den messaging-Benutzer, die von der empfangenden Benutzer dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-105">Contains the entry identifier for the messaging user who is represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bc0ee-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bc0ee-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bc0ee-107">PR_RCVD_REPRESENTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="bc0ee-107">PR_RCVD_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="bc0ee-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="bc0ee-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bc0ee-109">0x0043</span><span class="sxs-lookup"><span data-stu-id="bc0ee-109">0x0043</span></span>  <br/> |
|<span data-ttu-id="bc0ee-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bc0ee-110">Data type:</span></span>  <br/> |<span data-ttu-id="bc0ee-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bc0ee-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bc0ee-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bc0ee-112">Area:</span></span>  <br/> |<span data-ttu-id="bc0ee-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="bc0ee-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc0ee-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bc0ee-114">Remarks</span></span>

<span data-ttu-id="bc0ee-115">Diese Eigenschaft ist eine der Adresseigenschaften für den messaging-Benutzer, die von der empfangenden Benutzer dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-115">This property is one of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="bc0ee-116">Von der eingehenden Adressbuchhierarchie muss festgelegt werden, die auch für die Autorisierung oder Überprüfung des Delegaten zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-116">It must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="bc0ee-117">Wenn kein messaging Benutzer dargestellt wird, sollten diese Eigenschaft auf die Eintrags-ID, die in der Eigenschaft **PR_RECEIVED_BY_ENTRYID** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md)) enthalten sind festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-117">If no messaging user is being represented, this property should be set to the entry identifier contained in the **PR_RECEIVED_BY_ENTRYID** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="bc0ee-118">Ein Client Application Antworten auf eine Nachricht im Auftrag einer anderen Client empfangene sollte diese Eigenschaft in der **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))-Eigenschaft für die Antwort aus der empfangenen Nachricht kopieren.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-118">A client application replying to a message received on behalf of another client should copy this property from the received message into the **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bc0ee-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bc0ee-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bc0ee-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="bc0ee-120">Protocol specifications</span></span>

<span data-ttu-id="bc0ee-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc0ee-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bc0ee-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bc0ee-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc0ee-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bc0ee-124">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="bc0ee-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc0ee-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bc0ee-126">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="bc0ee-127">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc0ee-127">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bc0ee-128">Gibt die Methoden zum Herstellen einer Verbindung mit und Konfiguration von Postfächer als Stellvertretungen und Interaktionen mit Nachricht und Kalender-Objekte, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bc0ee-129">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="bc0ee-129">Header files</span></span>

<span data-ttu-id="bc0ee-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bc0ee-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="bc0ee-131">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="bc0ee-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bc0ee-132">Mapitags.h</span></span>
  
> <span data-ttu-id="bc0ee-133">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="bc0ee-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bc0ee-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc0ee-134">See also</span></span>



[<span data-ttu-id="bc0ee-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bc0ee-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bc0ee-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bc0ee-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bc0ee-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bc0ee-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bc0ee-138">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bc0ee-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

