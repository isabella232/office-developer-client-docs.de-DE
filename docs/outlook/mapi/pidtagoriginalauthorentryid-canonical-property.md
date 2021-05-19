---
title: PidTagOriginalAuthorEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorEntryId
api_type:
- COM
ms.assetid: 34654660-b003-42f5-9fcd-24ebaccd735d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 866c28bc08f669d18487c99c9a13bc7347b605fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425589"
---
# <a name="pidtagoriginalauthorentryid-canonical-property"></a><span data-ttu-id="2ef74-103">PidTagOriginalAuthorEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2ef74-103">PidTagOriginalAuthorEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="2ef74-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ef74-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ef74-105">Enthält den Eintragsbezeichner des Autors der ersten Version einer Nachricht, d. h. die Nachricht, bevor sie weitergeleitet oder beantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="2ef74-105">Contains the entry identifier of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2ef74-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2ef74-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2ef74-107">PR_ORIGINAL_AUTHOR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2ef74-107">PR_ORIGINAL_AUTHOR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="2ef74-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="2ef74-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2ef74-109">0x004C</span><span class="sxs-lookup"><span data-stu-id="2ef74-109">0x004C</span></span>  <br/> |
|<span data-ttu-id="2ef74-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="2ef74-110">Data type:</span></span>  <br/> |<span data-ttu-id="2ef74-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2ef74-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2ef74-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2ef74-112">Area:</span></span>  <br/> |<span data-ttu-id="2ef74-113">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="2ef74-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ef74-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2ef74-114">Remarks</span></span>

<span data-ttu-id="2ef74-115">Diese Eigenschaft ist eine der Adresseigenschaften für den Autor einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="2ef74-115">This property is one of the address properties for the author of a message.</span></span> <span data-ttu-id="2ef74-116">Bei der ersten Übermittlung der Nachricht sollte die Clientanwendung diese Eigenschaft auf den Wert PR_SENDER_ENTRYID **(** [PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) festlegen.</span><span class="sxs-lookup"><span data-stu-id="2ef74-116">At first submission of the message, the client application should set this property to the value of **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span></span> <span data-ttu-id="2ef74-117">Sie wird nie geändert, wenn die Nachricht weitergeleitet oder beantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="2ef74-117">It is never changed when the message is forwarded or replied to.</span></span> 
  
<span data-ttu-id="2ef74-118">Die ursprüngliche Author-Eigenschaft ermöglicht die Aufbewahrung von Informationen außerhalb der lokalen Messagingdomäne.</span><span class="sxs-lookup"><span data-stu-id="2ef74-118">The original author property allows for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="2ef74-119">Wenn eine Nachricht von einer anderen Messagingdomäne, z. B. aus dem Internet, eintrifft, stellt diese Eigenschaft eine Möglichkeit zur Verfügung, um sicherzustellen, dass ursprüngliche Informationen nicht verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="2ef74-119">When a message arrives from another messaging domain, such as from the Internet, this property provides a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2ef74-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2ef74-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2ef74-121">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="2ef74-121">Header files</span></span>

<span data-ttu-id="2ef74-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2ef74-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="2ef74-123">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="2ef74-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="2ef74-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2ef74-124">Mapitags.h</span></span>
  
> <span data-ttu-id="2ef74-125">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="2ef74-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ef74-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ef74-126">See also</span></span>



[<span data-ttu-id="2ef74-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2ef74-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2ef74-128">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="2ef74-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2ef74-129">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2ef74-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2ef74-130">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2ef74-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

