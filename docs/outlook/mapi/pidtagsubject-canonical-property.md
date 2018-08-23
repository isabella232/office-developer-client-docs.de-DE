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
ms.openlocfilehash: 9d37e4ee32cb5db623cece3061012ae4df0173a8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586942"
---
# <a name="pidtagsubject-canonical-property"></a><span data-ttu-id="3cd46-103">PidTagSubject (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3cd46-103">PidTagSubject Canonical Property</span></span>

  
  
<span data-ttu-id="3cd46-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3cd46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3cd46-105">Enthält den vollständigen Betreff einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="3cd46-105">Contains the full subject of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3cd46-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="3cd46-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3cd46-107">PR_SUBJECT, PR_SUBJECT_A, PR_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="3cd46-107">PR_SUBJECT, PR_SUBJECT_A, PR_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="3cd46-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="3cd46-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3cd46-109">0 x 0037</span><span class="sxs-lookup"><span data-stu-id="3cd46-109">0x0037</span></span>  <br/> |
|<span data-ttu-id="3cd46-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="3cd46-110">Data type:</span></span>  <br/> |<span data-ttu-id="3cd46-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3cd46-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3cd46-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="3cd46-112">Area:</span></span>  <br/> |<span data-ttu-id="3cd46-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="3cd46-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3cd46-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="3cd46-114">Remarks</span></span>

<span data-ttu-id="3cd46-115">Diese Eigenschaften werden für alle Objekte, die Meldung empfohlen.</span><span class="sxs-lookup"><span data-stu-id="3cd46-115">These properties are recommended on all message objects.</span></span> 
  
<span data-ttu-id="3cd46-116">Diese Eigenschaften sind immer den vollständigen Betreff, d. h., die Verkettung von das Präfix und den normalisierten Betreff.</span><span class="sxs-lookup"><span data-stu-id="3cd46-116">These properties are always the full subject text, that is, the concatenation of the prefix and the normalized subject.</span></span> <span data-ttu-id="3cd46-117">Wenn kein Präfix vorhanden ist, sollte der normalisierte Betreff den Betreff identisch sein.</span><span class="sxs-lookup"><span data-stu-id="3cd46-117">If there is no prefix, the normalized subject should be the same as the subject.</span></span> <span data-ttu-id="3cd46-118">Eine Nachricht speichern oder transport-Anbieter verwendet, die diese Eigenschaften und die Eigenschaften zum Berechnen des normalisierten Betreffs mithilfe der Regel **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) unter **PR_NORMALIZED_SUBJECT** ([ beschrieben PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3cd46-118">A message store or transport provider uses both these properties and **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) properties to compute the normalized subject using the rule described under **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).</span></span>
  
<span data-ttu-id="3cd46-119">Die Subject-Eigenschaften in der Regel kleine Zeichenfolgen von weniger als 256 Zeichen sind, und eine Nachricht Speicheranbieter ist nicht verpflichtet, klicken sie auf die **IStream** -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3cd46-119">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the **IStream** interface on them.</span></span> <span data-ttu-id="3cd46-120">Der Client sollte immer Zugriff über die Schnittstelle **IMAPIProp** zuerst versuchen, und greifen auf **IStream** nur, wenn **MAPI_E_NOT_ENOUGH_MEMORY** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3cd46-120">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
<span data-ttu-id="3cd46-121">Für einen Bericht enthält diese Eigenschaft die ursprüngliche Nachricht Betreff eine Zeichenfolge, die angibt, wo der Nachricht vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="3cd46-121">For a report, this property contains the original message's subject preceded by a string indicating what has happened to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3cd46-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3cd46-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3cd46-123">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="3cd46-123">Protocol specifications</span></span>

<span data-ttu-id="3cd46-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3cd46-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3cd46-125">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="3cd46-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3cd46-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3cd46-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3cd46-127">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="3cd46-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3cd46-128">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="3cd46-128">Header files</span></span>

<span data-ttu-id="3cd46-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3cd46-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="3cd46-130">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="3cd46-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="3cd46-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3cd46-131">Mapitags.h</span></span>
  
> <span data-ttu-id="3cd46-132">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="3cd46-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3cd46-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3cd46-133">See also</span></span>



[<span data-ttu-id="3cd46-134">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3cd46-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3cd46-135">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3cd46-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3cd46-136">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="3cd46-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3cd46-137">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="3cd46-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

