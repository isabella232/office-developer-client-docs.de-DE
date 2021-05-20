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
ms.openlocfilehash: 7918c5d5b585ffb199bfbc140edfb8286b499b40
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436167"
---
# <a name="pidtagoriginalauthoremailaddress-canonical-property"></a><span data-ttu-id="41ed9-103">PidTagOriginalAuthorEmailAddress (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="41ed9-103">PidTagOriginalAuthorEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="41ed9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41ed9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41ed9-105">Enthält die E-Mail-Adresse des Autors der ersten Version einer Nachricht, d. h. die Nachricht, bevor sie weitergeleitet oder beantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="41ed9-105">Contains the email address of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="41ed9-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="41ed9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="41ed9-107">PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_A, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="41ed9-107">PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_A, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="41ed9-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="41ed9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="41ed9-109">0x007A</span><span class="sxs-lookup"><span data-stu-id="41ed9-109">0x007A</span></span>  <br/> |
|<span data-ttu-id="41ed9-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="41ed9-110">Data type:</span></span>  <br/> |<span data-ttu-id="41ed9-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="41ed9-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="41ed9-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="41ed9-112">Area:</span></span>  <br/> |<span data-ttu-id="41ed9-113">Server</span><span class="sxs-lookup"><span data-stu-id="41ed9-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41ed9-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="41ed9-114">Remarks</span></span>

<span data-ttu-id="41ed9-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den Autor einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="41ed9-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="41ed9-116">Bei der ersten Übermittlung der Nachricht sollte die Clientanwendung diese Eigenschaften auf den Wert der **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) -Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="41ed9-116">At first submission of the message, the client application should set these properties to the value of the **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="41ed9-117">Sie wird nie geändert, wenn die Nachricht weitergeleitet oder beantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="41ed9-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="41ed9-118">Die ursprünglichen Autoreneigenschaften ermöglichen die Aufbewahrung von Informationen außerhalb der lokalen Messagingdomäne.</span><span class="sxs-lookup"><span data-stu-id="41ed9-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="41ed9-119">Wenn eine Nachricht von einer anderen Messagingdomäne, z. B. aus dem Internet, eintrifft, stellen diese Eigenschaften eine Möglichkeit zur Verfügung, um sicherzustellen, dass ursprüngliche Informationen nicht verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="41ed9-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="41ed9-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="41ed9-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="41ed9-121">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="41ed9-121">Header files</span></span>

<span data-ttu-id="41ed9-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="41ed9-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="41ed9-123">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="41ed9-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="41ed9-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="41ed9-124">Mapitags.h</span></span>
  
> <span data-ttu-id="41ed9-125">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="41ed9-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="41ed9-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41ed9-126">See also</span></span>



[<span data-ttu-id="41ed9-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41ed9-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="41ed9-128">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="41ed9-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="41ed9-129">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="41ed9-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="41ed9-130">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="41ed9-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

