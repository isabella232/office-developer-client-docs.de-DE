---
title: Kanonische Pidtagoriginalauthoremailaddress (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7918c5d5b585ffb199bfbc140edfb8286b499b40
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329239"
---
# <a name="pidtagoriginalauthoremailaddress-canonical-property"></a><span data-ttu-id="4eafd-103">Kanonische Pidtagoriginalauthoremailaddress (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4eafd-103">PidTagOriginalAuthorEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="4eafd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4eafd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4eafd-105">Enthält die e-Mail-Adresse des Autors der ersten Version einer Nachricht, also die Nachricht, bevor Sie weitergeleitet oder darauf geantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="4eafd-105">Contains the email address of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4eafd-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4eafd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4eafd-107">PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_A, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="4eafd-107">PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_A, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="4eafd-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="4eafd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4eafd-109">0x007A</span><span class="sxs-lookup"><span data-stu-id="4eafd-109">0x007A</span></span>  <br/> |
|<span data-ttu-id="4eafd-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4eafd-110">Data type:</span></span>  <br/> |<span data-ttu-id="4eafd-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4eafd-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4eafd-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4eafd-112">Area:</span></span>  <br/> |<span data-ttu-id="4eafd-113">Server</span><span class="sxs-lookup"><span data-stu-id="4eafd-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4eafd-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4eafd-114">Remarks</span></span>

<span data-ttu-id="4eafd-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den Autor einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="4eafd-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="4eafd-116">Bei der ersten Übermittlung der Nachricht sollte die Clientanwendung diese Eigenschaften auf den Wert der **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="4eafd-116">At first submission of the message, the client application should set these properties to the value of the **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="4eafd-117">Sie wird nie geändert, wenn die Nachricht weitergeleitet oder beantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="4eafd-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="4eafd-118">Die ursprünglichen Autoren Eigenschaften ermöglichen die Aufbewahrung von Informationen außerhalb der lokalen Messaging Domäne.</span><span class="sxs-lookup"><span data-stu-id="4eafd-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="4eafd-119">Wenn eine Nachricht von einer anderen Messaging Domäne eingeht, beispielsweise aus dem Internet, bieten diese Eigenschaften eine Möglichkeit, um sicherzustellen, dass die ursprünglichen Informationen nicht verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="4eafd-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4eafd-120">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4eafd-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4eafd-121">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="4eafd-121">Header files</span></span>

<span data-ttu-id="4eafd-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4eafd-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="4eafd-123">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="4eafd-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="4eafd-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="4eafd-124">Mapitags.h</span></span>
  
> <span data-ttu-id="4eafd-125">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="4eafd-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4eafd-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4eafd-126">See also</span></span>



[<span data-ttu-id="4eafd-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4eafd-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4eafd-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4eafd-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4eafd-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4eafd-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4eafd-130">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4eafd-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

