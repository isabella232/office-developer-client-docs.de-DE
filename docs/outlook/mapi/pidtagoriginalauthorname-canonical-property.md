---
title: Kanonische Pidtagoriginalauthorname (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorNam
api_type:
- COM
ms.assetid: beb23742-d844-4d90-9b13-1ad376d4206c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: bb62f3a44c9f17070db969683891fb2e2d62eb5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355776"
---
# <a name="pidtagoriginalauthorname-canonical-property"></a><span data-ttu-id="78fe1-103">Kanonische Pidtagoriginalauthorname (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="78fe1-103">PidTagOriginalAuthorName Canonical Property</span></span>

  
  
<span data-ttu-id="78fe1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78fe1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78fe1-105">Enthält den Anzeigenamen des Autors der ersten Version einer Nachricht, also die Nachricht, bevor Sie weitergeleitet oder darauf geantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="78fe1-105">Contains the display name of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="78fe1-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="78fe1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="78fe1-107">PR_ORIGINAL_AUTHOR_NAME, PR_ORIGINAL_AUTHOR_NAME_A, PR_ORIGINAL_AUTHOR_NAME_W</span><span class="sxs-lookup"><span data-stu-id="78fe1-107">PR_ORIGINAL_AUTHOR_NAME, PR_ORIGINAL_AUTHOR_NAME_A, PR_ORIGINAL_AUTHOR_NAME_W</span></span>  <br/> |
|<span data-ttu-id="78fe1-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="78fe1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="78fe1-109">0x004D</span><span class="sxs-lookup"><span data-stu-id="78fe1-109">0x004D</span></span>  <br/> |
|<span data-ttu-id="78fe1-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="78fe1-110">Data type:</span></span>  <br/> |<span data-ttu-id="78fe1-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="78fe1-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="78fe1-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="78fe1-112">Area:</span></span>  <br/> |<span data-ttu-id="78fe1-113">E-Mail</span><span class="sxs-lookup"><span data-stu-id="78fe1-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78fe1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78fe1-114">Remarks</span></span>

<span data-ttu-id="78fe1-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den Autor einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="78fe1-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="78fe1-116">Bei der ersten Übermittlung der Nachricht sollte die Clientanwendung diese Eigenschaften auf den Wert von **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) festlegen.</span><span class="sxs-lookup"><span data-stu-id="78fe1-116">At first submission of the message, the client application should set these properties to the value of **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)).</span></span> <span data-ttu-id="78fe1-117">Sie wird nie geändert, wenn die Nachricht weitergeleitet oder beantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="78fe1-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="78fe1-118">Die ursprünglichen Autoren Eigenschaften ermöglichen die Aufbewahrung von Informationen außerhalb der lokalen Messaging Domäne.</span><span class="sxs-lookup"><span data-stu-id="78fe1-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="78fe1-119">Wenn eine Nachricht von einer anderen Messaging Domäne eingeht, beispielsweise aus dem Internet, bieten diese Eigenschaften eine Möglichkeit, um sicherzustellen, dass die ursprünglichen Informationen nicht verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="78fe1-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="78fe1-120">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="78fe1-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="78fe1-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="78fe1-121">Protocol specifications</span></span>

<span data-ttu-id="78fe1-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="78fe1-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="78fe1-123">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="78fe1-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="78fe1-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="78fe1-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="78fe1-125">Konvertiert zwischen IETF-RFC2445, RFC2446 und RFC2447 sowie Termin-und Besprechungs Objekten.</span><span class="sxs-lookup"><span data-stu-id="78fe1-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="78fe1-126">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="78fe1-126">Header files</span></span>

<span data-ttu-id="78fe1-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="78fe1-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="78fe1-128">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="78fe1-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="78fe1-129">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="78fe1-129">Mapitags.h</span></span>
  
> <span data-ttu-id="78fe1-130">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="78fe1-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="78fe1-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78fe1-131">See also</span></span>



[<span data-ttu-id="78fe1-132">Kanonische PidTagDisplayName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="78fe1-132">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="78fe1-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="78fe1-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="78fe1-134">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="78fe1-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="78fe1-135">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="78fe1-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="78fe1-136">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="78fe1-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

