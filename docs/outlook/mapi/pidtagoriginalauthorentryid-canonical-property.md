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
ms.openlocfilehash: 03dcc9a1f929bc6f99ca9e1dd9f75f3fb9c3dcb0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22562967"
---
# <a name="pidtagoriginalauthorentryid-canonical-property"></a><span data-ttu-id="e8007-103">PidTagOriginalAuthorEntryId (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e8007-103">PidTagOriginalAuthorEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="e8007-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8007-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8007-105">Enthält die Eintrags-ID des Autors der ersten Version einer Nachricht, d. h., die Nachricht vor dem weitergeleitet oder darauf geantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="e8007-105">Contains the entry identifier of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e8007-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e8007-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e8007-107">PR_ORIGINAL_AUTHOR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e8007-107">PR_ORIGINAL_AUTHOR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="e8007-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e8007-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e8007-109">0x004C</span><span class="sxs-lookup"><span data-stu-id="e8007-109">0x004C</span></span>  <br/> |
|<span data-ttu-id="e8007-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e8007-110">Data type:</span></span>  <br/> |<span data-ttu-id="e8007-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e8007-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e8007-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e8007-112">Area:</span></span>  <br/> |<span data-ttu-id="e8007-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="e8007-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8007-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="e8007-114">Remarks</span></span>

<span data-ttu-id="e8007-115">Diese Eigenschaft ist eine der Adresseigenschaften für den Autor einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e8007-115">This property is one of the address properties for the author of a message.</span></span> <span data-ttu-id="e8007-116">Am ersten Übermittlung der Nachricht sollte die Clientanwendung diese Eigenschaft auf den Wert der **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e8007-116">At first submission of the message, the client application should set this property to the value of **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span></span> <span data-ttu-id="e8007-117">Es wird nie geändert, wenn die Nachricht weitergeleitet oder darauf geantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="e8007-117">It is never changed when the message is forwarded or replied to.</span></span> 
  
<span data-ttu-id="e8007-118">Die ursprünglichen Author-Eigenschaft kann zur Aufbewahrung von Informationen von außerhalb der lokalen Domäne messaging.</span><span class="sxs-lookup"><span data-stu-id="e8007-118">The original author property allows for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="e8007-119">Wenn eine Nachricht aus einer anderen Domäne messaging, eintritt, wie diese Eigenschaft aus dem Internet stellt eine Möglichkeit, um sicherzustellen, dass diese ursprünglichen Informationen bereit ist nicht verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="e8007-119">When a message arrives from another messaging domain, such as from the Internet, this property provides a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e8007-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e8007-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e8007-121">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="e8007-121">Header files</span></span>

<span data-ttu-id="e8007-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e8007-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="e8007-123">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e8007-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="e8007-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e8007-124">Mapitags.h</span></span>
  
> <span data-ttu-id="e8007-125">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e8007-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e8007-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8007-126">See also</span></span>



[<span data-ttu-id="e8007-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e8007-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e8007-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e8007-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e8007-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e8007-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e8007-130">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e8007-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

