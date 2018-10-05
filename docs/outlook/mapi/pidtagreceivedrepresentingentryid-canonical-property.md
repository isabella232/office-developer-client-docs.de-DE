---
title: PidTagReceivedRepresentingEntryId (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 33e41343e0c159be20ed1499fc24223947975e1d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383786"
---
# <a name="pidtagreceivedrepresentingentryid-canonical-property"></a><span data-ttu-id="804a5-103">PidTagReceivedRepresentingEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="804a5-103">PidTagReceivedRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="804a5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="804a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="804a5-105">Enthält die Eintrags-ID für den messaging-Benutzer, die von der empfangenden Benutzer dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="804a5-105">Contains the entry identifier for the messaging user who is represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="804a5-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="804a5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="804a5-107">PR_RCVD_REPRESENTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="804a5-107">PR_RCVD_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="804a5-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="804a5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="804a5-109">0x0043</span><span class="sxs-lookup"><span data-stu-id="804a5-109">0x0043</span></span>  <br/> |
|<span data-ttu-id="804a5-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="804a5-110">Data type:</span></span>  <br/> |<span data-ttu-id="804a5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="804a5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="804a5-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="804a5-112">Area:</span></span>  <br/> |<span data-ttu-id="804a5-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="804a5-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="804a5-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="804a5-114">Remarks</span></span>

<span data-ttu-id="804a5-115">Diese Eigenschaft ist eine der Adresseigenschaften für den messaging-Benutzer, die von der empfangenden Benutzer dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="804a5-115">This property is one of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="804a5-116">Von der eingehenden Adressbuchhierarchie muss festgelegt werden, die auch für die Autorisierung oder Überprüfung des Delegaten zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="804a5-116">It must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="804a5-117">Wenn kein messaging Benutzer dargestellt wird, sollten diese Eigenschaft auf die Eintrags-ID, die in der Eigenschaft **PR_RECEIVED_BY_ENTRYID** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md)) enthalten sind festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="804a5-117">If no messaging user is being represented, this property should be set to the entry identifier contained in the **PR_RECEIVED_BY_ENTRYID** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="804a5-118">Ein Client Application Antworten auf eine Nachricht im Auftrag einer anderen Client empfangene sollte diese Eigenschaft in der **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))-Eigenschaft für die Antwort aus der empfangenen Nachricht kopieren.</span><span class="sxs-lookup"><span data-stu-id="804a5-118">A client application replying to a message received on behalf of another client should copy this property from the received message into the **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="804a5-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="804a5-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="804a5-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="804a5-120">Protocol specifications</span></span>

<span data-ttu-id="804a5-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="804a5-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="804a5-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="804a5-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="804a5-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="804a5-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="804a5-124">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="804a5-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="804a5-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="804a5-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="804a5-126">Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.</span><span class="sxs-lookup"><span data-stu-id="804a5-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="804a5-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="804a5-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="804a5-128">Gibt die Methoden zum Herstellen einer Verbindung mit und Konfiguration von Postfächer als Stellvertretungen und Interaktionen mit Nachricht und Kalender-Objekte, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="804a5-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="804a5-129">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="804a5-129">Header files</span></span>

<span data-ttu-id="804a5-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="804a5-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="804a5-131">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="804a5-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="804a5-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="804a5-132">Mapitags.h</span></span>
  
> <span data-ttu-id="804a5-133">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="804a5-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="804a5-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="804a5-134">See also</span></span>



[<span data-ttu-id="804a5-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="804a5-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="804a5-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="804a5-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="804a5-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="804a5-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="804a5-138">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="804a5-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

