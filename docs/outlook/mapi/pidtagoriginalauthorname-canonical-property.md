---
title: PidTagOriginalAuthorName (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4b2f47f503caa32a1bdcd287e2fa5e894d667573
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794672"
---
# <a name="pidtagoriginalauthorname-canonical-property"></a><span data-ttu-id="06620-103">PidTagOriginalAuthorName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="06620-103">PidTagOriginalAuthorName Canonical Property</span></span>

  
  
<span data-ttu-id="06620-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="06620-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="06620-105">Enthält den Anzeigenamen des Autors der ersten Version einer Nachricht, d. h., die Nachricht vor dem weitergeleitet oder darauf geantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="06620-105">Contains the display name of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="06620-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="06620-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="06620-107">PR_ORIGINAL_AUTHOR_NAME, PR_ORIGINAL_AUTHOR_NAME_A, PR_ORIGINAL_AUTHOR_NAME_W</span><span class="sxs-lookup"><span data-stu-id="06620-107">PR_ORIGINAL_AUTHOR_NAME, PR_ORIGINAL_AUTHOR_NAME_A, PR_ORIGINAL_AUTHOR_NAME_W</span></span>  <br/> |
|<span data-ttu-id="06620-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="06620-108">Identifier:</span></span>  <br/> |<span data-ttu-id="06620-109">0x004D</span><span class="sxs-lookup"><span data-stu-id="06620-109">0x004D</span></span>  <br/> |
|<span data-ttu-id="06620-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="06620-110">Data type:</span></span>  <br/> |<span data-ttu-id="06620-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="06620-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="06620-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="06620-112">Area:</span></span>  <br/> |<span data-ttu-id="06620-113">E-Mail</span><span class="sxs-lookup"><span data-stu-id="06620-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06620-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06620-114">Remarks</span></span>

<span data-ttu-id="06620-115">Diese Eigenschaften sind Beispiele für die Adresseigenschaften für den Autor einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="06620-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="06620-116">Am ersten Übermittlung der Nachricht sollte die Clientanwendung diese Eigenschaften auf den Wert der **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="06620-116">At first submission of the message, the client application should set these properties to the value of **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)).</span></span> <span data-ttu-id="06620-117">Es wird nie geändert, wenn die Nachricht weitergeleitet oder darauf geantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="06620-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="06620-118">Ursprüngliche Autor der Eigenschaften können zur Aufbewahrung von Informationen von außerhalb der lokalen Domäne messaging.</span><span class="sxs-lookup"><span data-stu-id="06620-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="06620-119">Beim Empfang einer Nachricht aus einer anderen Domäne messaging bieten wie beispielsweise aus dem Internet diese Eigenschaften eine Möglichkeit, stellen Sie sicher, dass die ursprünglichen Informationen nicht verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="06620-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="06620-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="06620-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="06620-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="06620-121">Protocol specifications</span></span>

<span data-ttu-id="06620-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06620-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06620-123">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="06620-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="06620-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06620-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06620-125">Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.</span><span class="sxs-lookup"><span data-stu-id="06620-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="06620-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="06620-126">Header files</span></span>

<span data-ttu-id="06620-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="06620-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="06620-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="06620-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="06620-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="06620-129">Mapitags.h</span></span>
  
> <span data-ttu-id="06620-130">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="06620-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="06620-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06620-131">See also</span></span>



[<span data-ttu-id="06620-132">PidTagDisplayName (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="06620-132">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="06620-133">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="06620-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="06620-134">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="06620-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="06620-135">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="06620-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="06620-136">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="06620-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

