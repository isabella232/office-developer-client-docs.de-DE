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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fb30f2b29691984614891e2345fe97abe6316f58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794667"
---
# <a name="pidtagoriginalauthoraddresstype-canonical-property"></a><span data-ttu-id="ef71e-103">PidTagOriginalAuthorAddressType (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ef71e-103">PidTagOriginalAuthorAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="ef71e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ef71e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ef71e-105">Enthält den Adresstyp des Autors der ersten Version einer Nachricht, d. h., die Nachricht vor dem weitergeleitet oder darauf geantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="ef71e-105">Contains the address type of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ef71e-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ef71e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ef71e-107">PR_ORIGINAL_AUTHOR_ADDRTYPE, PR_ORIGINAL_AUTHOR_ADDRTYPE_A, PR_ORIGINAL_AUTHOR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="ef71e-107">PR_ORIGINAL_AUTHOR_ADDRTYPE, PR_ORIGINAL_AUTHOR_ADDRTYPE_A, PR_ORIGINAL_AUTHOR_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="ef71e-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="ef71e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ef71e-109">0x0079</span><span class="sxs-lookup"><span data-stu-id="ef71e-109">0x0079</span></span>  <br/> |
|<span data-ttu-id="ef71e-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ef71e-110">Data type:</span></span>  <br/> |<span data-ttu-id="ef71e-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ef71e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ef71e-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ef71e-112">Area:</span></span>  <br/> |<span data-ttu-id="ef71e-113">Server</span><span class="sxs-lookup"><span data-stu-id="ef71e-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef71e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef71e-114">Remarks</span></span>

<span data-ttu-id="ef71e-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den Autor einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="ef71e-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="ef71e-116">Am ersten Übermittlung der Nachricht sollte die Clientanwendung diese Eigenschaft auf den Wert der Eigenschaft **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ef71e-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) property.</span></span> <span data-ttu-id="ef71e-117">Es wird nie geändert, wenn die Nachricht weitergeleitet oder darauf geantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="ef71e-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="ef71e-118">Ursprüngliche Autor der Eigenschaften können zur Aufbewahrung von Informationen von außerhalb der lokalen Domäne messaging.</span><span class="sxs-lookup"><span data-stu-id="ef71e-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="ef71e-119">Beim Empfang einer Nachricht aus einer anderen Domäne messaging bieten wie beispielsweise aus dem Internet diese Eigenschaften eine Möglichkeit, stellen Sie sicher, dass die ursprünglichen Informationen nicht verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="ef71e-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ef71e-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ef71e-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ef71e-121">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="ef71e-121">Header files</span></span>

<span data-ttu-id="ef71e-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ef71e-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="ef71e-123">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ef71e-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="ef71e-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ef71e-124">Mapitags.h</span></span>
  
> <span data-ttu-id="ef71e-125">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ef71e-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ef71e-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef71e-126">See also</span></span>



[<span data-ttu-id="ef71e-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ef71e-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ef71e-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ef71e-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ef71e-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ef71e-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ef71e-130">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ef71e-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

