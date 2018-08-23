---
title: PidTagOriginalAuthorSearchKey (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorSearchKey
api_type:
- COM
ms.assetid: 4a10cf99-c5e6-4a24-b531-3aebb7800bfe
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 225c0813139a74b735b5b8a3d5a729e630cd3511
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563338"
---
# <a name="pidtagoriginalauthorsearchkey-canonical-property"></a><span data-ttu-id="47fce-103">PidTagOriginalAuthorSearchKey (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="47fce-103">PidTagOriginalAuthorSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="47fce-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47fce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47fce-105">Enthält den Suchschlüssel des Autors der ersten Version einer Nachricht, d. h., die Nachricht vor dem weitergeleitet oder darauf geantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="47fce-105">Contains the search key of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="47fce-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="47fce-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="47fce-107">PR_ORIGINAL_AUTHOR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="47fce-107">PR_ORIGINAL_AUTHOR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="47fce-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="47fce-108">Identifier:</span></span>  <br/> |<span data-ttu-id="47fce-109">0x0056</span><span class="sxs-lookup"><span data-stu-id="47fce-109">0x0056</span></span>  <br/> |
|<span data-ttu-id="47fce-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="47fce-110">Data type:</span></span>  <br/> |<span data-ttu-id="47fce-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="47fce-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="47fce-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="47fce-112">Area:</span></span>  <br/> |<span data-ttu-id="47fce-113">Server</span><span class="sxs-lookup"><span data-stu-id="47fce-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="47fce-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="47fce-114">Remarks</span></span>

<span data-ttu-id="47fce-115">Diese Eigenschaft ist eine der Adresseigenschaften für den Autor einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="47fce-115">This property is one of the address properties for the author of a message.</span></span> <span data-ttu-id="47fce-116">Am ersten Übermittlung der Nachricht sollte die Client-Anwendung diese Eigenschaft auf den Wert der **PR_SENDER_SEARCH_KEY**[PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md) -Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="47fce-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_SEARCH_KEY**[PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md) property.</span></span> <span data-ttu-id="47fce-117">Es wird nie geändert, wenn die Nachricht weitergeleitet oder darauf geantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="47fce-117">It is never changed when the message is forwarded or replied to.</span></span> 
  
<span data-ttu-id="47fce-118">Ursprüngliche Autor der Eigenschaften können zur Aufbewahrung von Informationen von außerhalb der lokalen Domäne messaging.</span><span class="sxs-lookup"><span data-stu-id="47fce-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="47fce-119">Beim Empfang einer Nachricht aus einer anderen Domäne messaging bieten wie beispielsweise aus dem Internet diese Eigenschaften eine Möglichkeit, stellen Sie sicher, dass die ursprünglichen Informationen nicht verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="47fce-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="47fce-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="47fce-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="47fce-121">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="47fce-121">Header files</span></span>

<span data-ttu-id="47fce-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="47fce-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="47fce-123">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="47fce-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="47fce-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="47fce-124">Mapitags.h</span></span>
  
> <span data-ttu-id="47fce-125">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="47fce-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="47fce-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47fce-126">See also</span></span>



[<span data-ttu-id="47fce-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="47fce-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="47fce-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="47fce-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="47fce-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="47fce-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="47fce-130">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="47fce-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

