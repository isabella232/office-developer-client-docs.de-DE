---
title: Kanonische PidTagOriginalAuthorSearchKey-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e5b283376d018b7b2675e05f994d586126437590
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794675"
---
# <a name="pidtagoriginalauthorsearchkey-canonical-property"></a><span data-ttu-id="299a0-103">Kanonische PidTagOriginalAuthorSearchKey-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="299a0-103">PidTagOriginalAuthorSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="299a0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="299a0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="299a0-105">Enthält den Suchschlüssel des Autors der ersten Version einer Nachricht, d. h., die Nachricht vor dem weitergeleitet oder darauf geantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="299a0-105">Contains the search key of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="299a0-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="299a0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="299a0-107">PR_ORIGINAL_AUTHOR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="299a0-107">PR_ORIGINAL_AUTHOR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="299a0-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="299a0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="299a0-109">0x0056</span><span class="sxs-lookup"><span data-stu-id="299a0-109">0x0056</span></span>  <br/> |
|<span data-ttu-id="299a0-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="299a0-110">Data type:</span></span>  <br/> |<span data-ttu-id="299a0-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="299a0-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="299a0-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="299a0-112">Area:</span></span>  <br/> |<span data-ttu-id="299a0-113">Server</span><span class="sxs-lookup"><span data-stu-id="299a0-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="299a0-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="299a0-114">Remarks</span></span>

<span data-ttu-id="299a0-115">Diese Eigenschaft ist eine der Adresseigenschaften für den Autor einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="299a0-115">This property is one of the address properties for the author of a message.</span></span> <span data-ttu-id="299a0-116">Am ersten Übermittlung der Nachricht sollte die Client-Anwendung diese Eigenschaft auf den Wert der **PR_SENDER_SEARCH_KEY**[PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md) -Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="299a0-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_SEARCH_KEY**[PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md) property.</span></span> <span data-ttu-id="299a0-117">Es wird nie geändert, wenn die Nachricht weitergeleitet oder darauf geantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="299a0-117">It is never changed when the message is forwarded or replied to.</span></span> 
  
<span data-ttu-id="299a0-118">Ursprüngliche Autor der Eigenschaften können zur Aufbewahrung von Informationen von außerhalb der lokalen Domäne messaging.</span><span class="sxs-lookup"><span data-stu-id="299a0-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="299a0-119">Beim Empfang einer Nachricht aus einer anderen Domäne messaging bieten wie beispielsweise aus dem Internet diese Eigenschaften eine Möglichkeit, stellen Sie sicher, dass die ursprünglichen Informationen nicht verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="299a0-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="299a0-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="299a0-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="299a0-121">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="299a0-121">Header files</span></span>

<span data-ttu-id="299a0-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="299a0-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="299a0-123">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="299a0-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="299a0-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="299a0-124">Mapitags.h</span></span>
  
> <span data-ttu-id="299a0-125">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="299a0-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="299a0-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="299a0-126">See also</span></span>



[<span data-ttu-id="299a0-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="299a0-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="299a0-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="299a0-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="299a0-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="299a0-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="299a0-130">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="299a0-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

