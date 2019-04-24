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
ms.openlocfilehash: 33e41343e0c159be20ed1499fc24223947975e1d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359094"
---
# <a name="pidtagreceivedrepresentingentryid-canonical-property"></a><span data-ttu-id="33159-103">Kanonische PidTagReceivedRepresentingEntryId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="33159-103">PidTagReceivedRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="33159-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33159-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33159-105">Enthält die Eintrags-ID für den Messagingbenutzer, der vom empfangenden Benutzer dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="33159-105">Contains the entry identifier for the messaging user who is represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="33159-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="33159-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="33159-107">PR_RCVD_REPRESENTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="33159-107">PR_RCVD_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="33159-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="33159-108">Identifier:</span></span>  <br/> |<span data-ttu-id="33159-109">0x0043</span><span class="sxs-lookup"><span data-stu-id="33159-109">0x0043</span></span>  <br/> |
|<span data-ttu-id="33159-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="33159-110">Data type:</span></span>  <br/> |<span data-ttu-id="33159-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="33159-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="33159-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="33159-112">Area:</span></span>  <br/> |<span data-ttu-id="33159-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="33159-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33159-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33159-114">Remarks</span></span>

<span data-ttu-id="33159-115">Diese Eigenschaft ist eine der Adresseigenschaften für den Messagingbenutzer, der vom empfangenden Benutzer dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="33159-115">This property is one of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="33159-116">Er muss vom eingehenden Transportanbieter festgelegt werden, der auch für die Autorisierung oder Überprüfung des Stellvertreters zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="33159-116">It must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="33159-117">Wenn kein Messagingbenutzer dargestellt wird, sollte diese Eigenschaft auf die Eintrags-ID festgelegt werden, die in der **PR_RECEIVED_BY_ENTRYID** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md))-Eigenschaft enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="33159-117">If no messaging user is being represented, this property should be set to the entry identifier contained in the **PR_RECEIVED_BY_ENTRYID** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="33159-118">Eine Clientanwendung, die auf eine Nachricht antwortet, die im Auftrag eines anderen Clients empfangen wird, sollte diese Eigenschaft aus der empfangenen Nachricht in die **PR_SENT_REPRESENTING_ENTRYID** ([pidtagsentrepresentingentryid (](pidtagsentrepresentingentryid-canonical-property.md))-Eigenschaft für die Antwort kopieren.</span><span class="sxs-lookup"><span data-stu-id="33159-118">A client application replying to a message received on behalf of another client should copy this property from the received message into the **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="33159-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="33159-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="33159-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="33159-120">Protocol specifications</span></span>

<span data-ttu-id="33159-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33159-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33159-122">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="33159-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="33159-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33159-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33159-124">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="33159-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="33159-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33159-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33159-126">Verarbeitet die Reihenfolge und den Ablauf für die Datenübertragung zwischen einem Client und einem Server.</span><span class="sxs-lookup"><span data-stu-id="33159-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="33159-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33159-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33159-128">Gibt Methoden zum Herstellen einer Verbindung mit und Konfigurieren von Postfächern als Stellvertreter sowie Interaktionen mit Nachrichten-und Kalenderobjekten an, wenn Sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="33159-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="33159-129">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="33159-129">Header files</span></span>

<span data-ttu-id="33159-130">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="33159-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="33159-131">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="33159-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="33159-132">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="33159-132">Mapitags.h</span></span>
  
> <span data-ttu-id="33159-133">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="33159-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="33159-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33159-134">See also</span></span>



[<span data-ttu-id="33159-135">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="33159-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="33159-136">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="33159-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="33159-137">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="33159-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="33159-138">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="33159-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

