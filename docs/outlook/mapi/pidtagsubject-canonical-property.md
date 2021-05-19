---
title: PidTagSubject (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubject
api_type:
- COM
ms.assetid: aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0cf9e9f8c10f8d27bd174b8b6f2bf19812dc269d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339256"
---
# <a name="pidtagsubject-canonical-property"></a><span data-ttu-id="c4c9b-103">PidTagSubject (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c4c9b-103">PidTagSubject Canonical Property</span></span>

  
  
<span data-ttu-id="c4c9b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4c9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4c9b-105">Enthält den vollständigen Betreff einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c4c9b-105">Contains the full subject of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c4c9b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c4c9b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c4c9b-107">PR_SUBJECT, PR_SUBJECT_A, PR_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="c4c9b-107">PR_SUBJECT, PR_SUBJECT_A, PR_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="c4c9b-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="c4c9b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c4c9b-109">0x0037</span><span class="sxs-lookup"><span data-stu-id="c4c9b-109">0x0037</span></span>  <br/> |
|<span data-ttu-id="c4c9b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c4c9b-110">Data type:</span></span>  <br/> |<span data-ttu-id="c4c9b-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c4c9b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c4c9b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c4c9b-112">Area:</span></span>  <br/> |<span data-ttu-id="c4c9b-113">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="c4c9b-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4c9b-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c4c9b-114">Remarks</span></span>

<span data-ttu-id="c4c9b-115">Diese Eigenschaften werden für alle Nachrichtenobjekte empfohlen.</span><span class="sxs-lookup"><span data-stu-id="c4c9b-115">These properties are recommended on all message objects.</span></span> 
  
<span data-ttu-id="c4c9b-116">Diese Eigenschaften sind immer der vollständige Betrefftext, d. h. die Verkettung des Präfixes und des normalisierten Betreffs.</span><span class="sxs-lookup"><span data-stu-id="c4c9b-116">These properties are always the full subject text, that is, the concatenation of the prefix and the normalized subject.</span></span> <span data-ttu-id="c4c9b-117">Wenn es kein Präfix gibt, sollte der normalisierte Betreff mit dem Betreff identisch sein.</span><span class="sxs-lookup"><span data-stu-id="c4c9b-117">If there is no prefix, the normalized subject should be the same as the subject.</span></span> <span data-ttu-id="c4c9b-118">Ein Nachrichtenspeicher oder Transportanbieter verwendet diese Eigenschaften und **PR_SUBJECT_PREFIX** -[PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)-Eigenschaften, um den normalisierten Betreff mithilfe der unter **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) beschriebenen Regel zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="c4c9b-118">A message store or transport provider uses both these properties and **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) properties to compute the normalized subject using the rule described under **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).</span></span>
  
<span data-ttu-id="c4c9b-119">Die Betreffeigenschaften sind in der Regel kleine Zeichenfolgen mit weniger als 256 Zeichen, und ein Nachrichtenspeicheranbieter ist nicht verpflichtet, die **IStream-Schnittstelle** für sie zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c4c9b-119">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the **IStream** interface on them.</span></span> <span data-ttu-id="c4c9b-120">Der Client sollte immer zuerst den Zugriff über die **IMAPIProp-Schnittstelle** versuchen und nur dann auf **IStream** zugreifen, **MAPI_E_NOT_ENOUGH_MEMORY** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c4c9b-120">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
<span data-ttu-id="c4c9b-121">Für einen Bericht enthält diese Eigenschaft den Betreff der ursprünglichen Nachricht vor einer Zeichenfolge, die angibt, was mit der Nachricht passiert ist.</span><span class="sxs-lookup"><span data-stu-id="c4c9b-121">For a report, this property contains the original message's subject preceded by a string indicating what has happened to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c4c9b-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c4c9b-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c4c9b-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c4c9b-123">Protocol specifications</span></span>

<span data-ttu-id="c4c9b-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4c9b-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4c9b-125">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="c4c9b-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c4c9b-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4c9b-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4c9b-127">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="c4c9b-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c4c9b-128">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="c4c9b-128">Header files</span></span>

<span data-ttu-id="c4c9b-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c4c9b-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="c4c9b-130">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c4c9b-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="c4c9b-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c4c9b-131">Mapitags.h</span></span>
  
> <span data-ttu-id="c4c9b-132">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="c4c9b-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c4c9b-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4c9b-133">See also</span></span>



[<span data-ttu-id="c4c9b-134">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c4c9b-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c4c9b-135">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="c4c9b-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c4c9b-136">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c4c9b-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c4c9b-137">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c4c9b-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

