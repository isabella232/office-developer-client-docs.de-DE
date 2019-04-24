---
title: Kanonische Pidtagsubjectprefix (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubjectPrefix
api_type:
- COM
ms.assetid: 07fcb881-d873-45bf-b048-30f41d0d8d85
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8257c3c3583072d16e96e6ea9bba4632fc78f9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339228"
---
# <a name="pidtagsubjectprefix-canonical-property"></a><span data-ttu-id="6d44c-103">Kanonische Pidtagsubjectprefix (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6d44c-103">PidTagSubjectPrefix Canonical Property</span></span>

  
  
<span data-ttu-id="6d44c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d44c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d44c-105">Enthält einen Betreff-Präfix, der in der Regel eine Aktion für eine Nachricht angibt, beispielsweise "FW:" für die Weiterleitung.</span><span class="sxs-lookup"><span data-stu-id="6d44c-105">Contains a subject prefix that typically indicates some action on a message, such as "FW: " for forwarding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6d44c-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6d44c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6d44c-107">PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W</span><span class="sxs-lookup"><span data-stu-id="6d44c-107">PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W</span></span>  <br/> |
|<span data-ttu-id="6d44c-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="6d44c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6d44c-109">0x003D</span><span class="sxs-lookup"><span data-stu-id="6d44c-109">0x003D</span></span>  <br/> |
|<span data-ttu-id="6d44c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6d44c-110">Data type:</span></span>  <br/> |<span data-ttu-id="6d44c-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6d44c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6d44c-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6d44c-112">Area:</span></span>  <br/> |<span data-ttu-id="6d44c-113">Allgemeine Nachrichtenübermittlung</span><span class="sxs-lookup"><span data-stu-id="6d44c-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d44c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d44c-114">Remarks</span></span>

<span data-ttu-id="6d44c-115">Diese Eigenschaften werden für alle Nachrichtenobjekte empfohlen.</span><span class="sxs-lookup"><span data-stu-id="6d44c-115">These properties are recommended on all message objects.</span></span> 
  
<span data-ttu-id="6d44c-116">Das Betreff-Präfix besteht aus einem oder mehreren alphanumerischen Zeichen, gefolgt von einem Doppelpunkt und einem Raum (die Teil des Präfixes sind).</span><span class="sxs-lookup"><span data-stu-id="6d44c-116">The subject prefix consists of one or more alphanumeric characters, followed by a colon and a space (which are part of the prefix).</span></span> <span data-ttu-id="6d44c-117">Sie darf keine nicht alphanumerische Zeichen vor dem Doppelpunkt enthalten.</span><span class="sxs-lookup"><span data-stu-id="6d44c-117">It must not contain any nonalphanumeric characters before the colon.</span></span> <span data-ttu-id="6d44c-118">Das Fehlen eines Präfixes kann durch eine leere Zeichenfolge oder durch diese Eigenschaft nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6d44c-118">Absence of a prefix can be represented by an empty string or by this property not being set.</span></span> 
  
<span data-ttu-id="6d44c-119">Wenn diese Eigenschaften explizit festgelegt werden, kann die Zeichenfolge eine beliebige Länge aufweisen und alphanumerische Zeichen verwenden, aber Sie muss mit einer Teilzeichenfolge am Anfang der **PR_Subject** ([PidTagSubject](pidtagsubject-canonical-property.md))-Eigenschaft übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="6d44c-119">If these properties are set explicitly, the string can be of any length and use any alphanumeric characters, but it must match a substring at the beginning of the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span> <span data-ttu-id="6d44c-120">Wenn diese Eigenschaften nicht vom Absender festgelegt werden und berechnet werden müssen, sind deren Inhalte eingeschränkter.</span><span class="sxs-lookup"><span data-stu-id="6d44c-120">If these properties are not set by the sender and must be computed, their contents are more restricted.</span></span> <span data-ttu-id="6d44c-121">Die Regel zum Berechnen des Präfixes ist, dass **PR_Subject** mit einem, zwei oder drei Buchstaben (nur alphabetisch) beginnen muss, gefolgt von einem Doppelpunkt und einem Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="6d44c-121">The rule for computing the prefix is that **PR_SUBJECT** must begin with one, two, or three letters (alphabetic only) followed by a colon and a space.</span></span> <span data-ttu-id="6d44c-122">Wenn eine solche Teilzeichenfolge am Anfang von **PR_Subject**gefunden wird, wird Sie die Zeichenfolge für diese Eigenschaften (und bleibt auch am Anfang von **PR_Subject**).</span><span class="sxs-lookup"><span data-stu-id="6d44c-122">If such a substring is found at the beginning of **PR_SUBJECT**, it then becomes the string for these properties (and also stays at the beginning of **PR_SUBJECT**).</span></span> <span data-ttu-id="6d44c-123">Andernfalls bleiben diese Eigenschaften unverändert.</span><span class="sxs-lookup"><span data-stu-id="6d44c-123">Otherwise, these properties remain unset.</span></span> 
  
<span data-ttu-id="6d44c-124">Diese Eigenschaften und **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) sollten als Teil der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Implementierung berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="6d44c-124">These properties and **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) should be computed as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) implementation.</span></span> <span data-ttu-id="6d44c-125">Ein Client sollte [IMAPIProp::](imapiprop-getprops.md) GetProps für seine Werte erst auffordern, nachdem er von einem **IMAPIProp:: SaveChanges** -Aufruf übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="6d44c-125">A client should not prompt [IMAPIProp::GetProps](imapiprop-getprops.md) for their values until they have been committed by an **IMAPIProp::SaveChanges** call.</span></span> 
  
<span data-ttu-id="6d44c-126">Die Subject-Eigenschaften sind in der Regel kleine Zeichenfolgen mit weniger als 256 Zeichen, und ein Nachrichtenspeicher Anbieter ist nicht verpflichtet, die OLE **IStream** -Schnittstelle darauf zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6d44c-126">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the OLE **IStream** interface on them.</span></span> <span data-ttu-id="6d44c-127">Ein Client sollte immer versuchen, zuerst über die **IMAPIProp** -Schnittstelle zuzugreifen, und nur dann auf **IStream** zurückgreifen, wenn **MAPI_E_NOT_ENOUGH_MEMORY** wird.</span><span class="sxs-lookup"><span data-stu-id="6d44c-127">A client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6d44c-128">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6d44c-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6d44c-129">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="6d44c-129">Protocol specifications</span></span>

<span data-ttu-id="6d44c-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d44c-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d44c-131">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="6d44c-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6d44c-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d44c-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d44c-133">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="6d44c-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="6d44c-134">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d44c-134">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d44c-135">Gibt die Eigenschaften und Vorgänge an, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="6d44c-135">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6d44c-136">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="6d44c-136">Header files</span></span>

<span data-ttu-id="6d44c-137">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="6d44c-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="6d44c-138">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="6d44c-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="6d44c-139">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="6d44c-139">Mapitags.h</span></span>
  
> <span data-ttu-id="6d44c-140">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="6d44c-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6d44c-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d44c-141">See also</span></span>



[<span data-ttu-id="6d44c-142">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6d44c-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6d44c-143">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6d44c-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6d44c-144">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6d44c-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6d44c-145">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6d44c-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

