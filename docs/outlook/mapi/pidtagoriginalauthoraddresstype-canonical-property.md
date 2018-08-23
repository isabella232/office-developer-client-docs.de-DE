---
title: PidTagOriginalAuthorAddressType (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorAddressType
api_type:
- COM
ms.assetid: 7cdedb1a-e441-469b-be50-2f18203eb30d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bc3c06c38f8ff8121a8503341cdd1084c036e52d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589973"
---
# <a name="pidtagoriginalauthoraddresstype-canonical-property"></a><span data-ttu-id="ca73f-103">PidTagOriginalAuthorAddressType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ca73f-103">PidTagOriginalAuthorAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="ca73f-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca73f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca73f-105">Enthält den Adresstyp des Autors der ersten Version einer Nachricht, d. h., die Nachricht vor dem weitergeleitet oder darauf geantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="ca73f-105">Contains the address type of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ca73f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ca73f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ca73f-107">PR_ORIGINAL_AUTHOR_ADDRTYPE, PR_ORIGINAL_AUTHOR_ADDRTYPE_A, PR_ORIGINAL_AUTHOR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="ca73f-107">PR_ORIGINAL_AUTHOR_ADDRTYPE, PR_ORIGINAL_AUTHOR_ADDRTYPE_A, PR_ORIGINAL_AUTHOR_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="ca73f-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="ca73f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ca73f-109">0x0079</span><span class="sxs-lookup"><span data-stu-id="ca73f-109">0x0079</span></span>  <br/> |
|<span data-ttu-id="ca73f-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ca73f-110">Data type:</span></span>  <br/> |<span data-ttu-id="ca73f-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ca73f-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ca73f-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ca73f-112">Area:</span></span>  <br/> |<span data-ttu-id="ca73f-113">Server</span><span class="sxs-lookup"><span data-stu-id="ca73f-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca73f-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="ca73f-114">Remarks</span></span>

<span data-ttu-id="ca73f-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den Autor einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="ca73f-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="ca73f-116">Am ersten Übermittlung der Nachricht sollte die Clientanwendung diese Eigenschaft auf den Wert der Eigenschaft **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ca73f-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) property.</span></span> <span data-ttu-id="ca73f-117">Es wird nie geändert, wenn die Nachricht weitergeleitet oder darauf geantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="ca73f-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="ca73f-118">Ursprüngliche Autor der Eigenschaften können zur Aufbewahrung von Informationen von außerhalb der lokalen Domäne messaging.</span><span class="sxs-lookup"><span data-stu-id="ca73f-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="ca73f-119">Beim Empfang einer Nachricht aus einer anderen Domäne messaging bieten wie beispielsweise aus dem Internet diese Eigenschaften eine Möglichkeit, stellen Sie sicher, dass die ursprünglichen Informationen nicht verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="ca73f-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ca73f-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ca73f-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ca73f-121">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="ca73f-121">Header files</span></span>

<span data-ttu-id="ca73f-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ca73f-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="ca73f-123">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ca73f-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="ca73f-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ca73f-124">Mapitags.h</span></span>
  
> <span data-ttu-id="ca73f-125">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ca73f-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ca73f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca73f-126">See also</span></span>



[<span data-ttu-id="ca73f-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ca73f-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ca73f-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ca73f-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ca73f-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ca73f-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ca73f-130">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ca73f-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

