---
title: PidTagOriginalAuthorEmailAddress (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorEmailAddress
api_type:
- COM
ms.assetid: 67cda756-ba71-4f29-a601-55359e44d93b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bd019378a8db7b2e356f0c8b2f30a59e685b9e8a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595433"
---
# <a name="pidtagoriginalauthoremailaddress-canonical-property"></a><span data-ttu-id="fac5f-103">PidTagOriginalAuthorEmailAddress (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fac5f-103">PidTagOriginalAuthorEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="fac5f-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fac5f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fac5f-105">Enthält die e-Mail-Adresse des Autors der ersten Version einer Nachricht, d. h., die Nachricht vor dem weitergeleitet oder darauf geantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="fac5f-105">Contains the email address of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fac5f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="fac5f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fac5f-107">PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_A, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="fac5f-107">PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_A, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="fac5f-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="fac5f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fac5f-109">0x007A</span><span class="sxs-lookup"><span data-stu-id="fac5f-109">0x007A</span></span>  <br/> |
|<span data-ttu-id="fac5f-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="fac5f-110">Data type:</span></span>  <br/> |<span data-ttu-id="fac5f-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fac5f-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fac5f-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="fac5f-112">Area:</span></span>  <br/> |<span data-ttu-id="fac5f-113">Server</span><span class="sxs-lookup"><span data-stu-id="fac5f-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fac5f-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="fac5f-114">Remarks</span></span>

<span data-ttu-id="fac5f-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den Autor einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="fac5f-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="fac5f-116">Am ersten Übermittlung der Nachricht sollte die Client-Anwendung diese Eigenschaften auf den Wert der Eigenschaft **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fac5f-116">At first submission of the message, the client application should set these properties to the value of the **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="fac5f-117">Es wird nie geändert, wenn die Nachricht weitergeleitet oder darauf geantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="fac5f-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="fac5f-118">Ursprüngliche Autor der Eigenschaften können zur Aufbewahrung von Informationen von außerhalb der lokalen Domäne messaging.</span><span class="sxs-lookup"><span data-stu-id="fac5f-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="fac5f-119">Beim Empfang einer Nachricht aus einer anderen Domäne messaging bieten wie beispielsweise aus dem Internet diese Eigenschaften eine Möglichkeit, stellen Sie sicher, dass die ursprünglichen Informationen nicht verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="fac5f-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fac5f-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fac5f-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="fac5f-121">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="fac5f-121">Header files</span></span>

<span data-ttu-id="fac5f-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fac5f-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="fac5f-123">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="fac5f-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="fac5f-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fac5f-124">Mapitags.h</span></span>
  
> <span data-ttu-id="fac5f-125">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="fac5f-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fac5f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fac5f-126">See also</span></span>



[<span data-ttu-id="fac5f-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fac5f-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fac5f-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fac5f-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fac5f-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="fac5f-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fac5f-130">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="fac5f-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

