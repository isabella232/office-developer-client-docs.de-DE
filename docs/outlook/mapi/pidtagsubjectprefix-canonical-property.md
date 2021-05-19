---
title: PidTagSubjectPrefix (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8257c3c3583072d16e96e6ea9bba4632fc78f9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339228"
---
# <a name="pidtagsubjectprefix-canonical-property"></a><span data-ttu-id="b1db8-103">PidTagSubjectPrefix (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b1db8-103">PidTagSubjectPrefix Canonical Property</span></span>

  
  
<span data-ttu-id="b1db8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1db8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1db8-105">Enthält ein Betreffpräfix, das in der Regel eine Aktion für eine Nachricht angibt, z. B. "FW: " für die Weiterleitung.</span><span class="sxs-lookup"><span data-stu-id="b1db8-105">Contains a subject prefix that typically indicates some action on a message, such as "FW: " for forwarding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b1db8-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b1db8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b1db8-107">PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W</span><span class="sxs-lookup"><span data-stu-id="b1db8-107">PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W</span></span>  <br/> |
|<span data-ttu-id="b1db8-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="b1db8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b1db8-109">0x003D</span><span class="sxs-lookup"><span data-stu-id="b1db8-109">0x003D</span></span>  <br/> |
|<span data-ttu-id="b1db8-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b1db8-110">Data type:</span></span>  <br/> |<span data-ttu-id="b1db8-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b1db8-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b1db8-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b1db8-112">Area:</span></span>  <br/> |<span data-ttu-id="b1db8-113">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="b1db8-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1db8-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b1db8-114">Remarks</span></span>

<span data-ttu-id="b1db8-115">Diese Eigenschaften werden für alle Nachrichtenobjekte empfohlen.</span><span class="sxs-lookup"><span data-stu-id="b1db8-115">These properties are recommended on all message objects.</span></span> 
  
<span data-ttu-id="b1db8-116">Das Betreffpräfix besteht aus einem oder mehreren alphanumerischen Zeichen, gefolgt von einem Doppelpunkt und einem Leerzeichen (die Teil des Präfixes sind).</span><span class="sxs-lookup"><span data-stu-id="b1db8-116">The subject prefix consists of one or more alphanumeric characters, followed by a colon and a space (which are part of the prefix).</span></span> <span data-ttu-id="b1db8-117">Er darf keine nichtalphanumerischen Zeichen vor dem Doppelpunkt enthalten.</span><span class="sxs-lookup"><span data-stu-id="b1db8-117">It must not contain any nonalphanumeric characters before the colon.</span></span> <span data-ttu-id="b1db8-118">Das Fehlen eines Präfixes kann durch eine leere Zeichenfolge dargestellt werden oder durch diese Eigenschaft, die nicht festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="b1db8-118">Absence of a prefix can be represented by an empty string or by this property not being set.</span></span> 
  
<span data-ttu-id="b1db8-119">Wenn diese Eigenschaften explizit festgelegt werden, kann die Zeichenfolge eine beliebige Länge haben und alphanumerische Zeichen verwenden, sie muss jedoch mit einer Teilzeichenfolge am Anfang der **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))-Eigenschaft übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b1db8-119">If these properties are set explicitly, the string can be of any length and use any alphanumeric characters, but it must match a substring at the beginning of the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span> <span data-ttu-id="b1db8-120">Wenn diese Eigenschaften nicht vom Absender festgelegt werden und berechnet werden müssen, sind ihre Inhalte eingeschränkter.</span><span class="sxs-lookup"><span data-stu-id="b1db8-120">If these properties are not set by the sender and must be computed, their contents are more restricted.</span></span> <span data-ttu-id="b1db8-121">Die Regel zum Berechnen des Präfixes **ist, dass PR_SUBJECT** mit einem, zwei oder drei Buchstaben (nur alphabetisch) gefolgt von einem Doppelpunkt und einem Leerzeichen beginnen muss.</span><span class="sxs-lookup"><span data-stu-id="b1db8-121">The rule for computing the prefix is that **PR_SUBJECT** must begin with one, two, or three letters (alphabetic only) followed by a colon and a space.</span></span> <span data-ttu-id="b1db8-122">Wenn eine solche Teilzeichenfolge am Anfang von **PR_SUBJECT** gefunden wird, wird sie dann zur Zeichenfolge für diese Eigenschaften (und bleibt auch am Anfang PR_SUBJECT **).**</span><span class="sxs-lookup"><span data-stu-id="b1db8-122">If such a substring is found at the beginning of **PR_SUBJECT**, it then becomes the string for these properties (and also stays at the beginning of **PR_SUBJECT**).</span></span> <span data-ttu-id="b1db8-123">Andernfalls bleiben diese Eigenschaften nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b1db8-123">Otherwise, these properties remain unset.</span></span> 
  
<span data-ttu-id="b1db8-124">Diese Eigenschaften und **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) sollten als Teil der [IMAPIProp::SaveChanges-Implementierung berechnet](imapiprop-savechanges.md) werden.</span><span class="sxs-lookup"><span data-stu-id="b1db8-124">These properties and **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) should be computed as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) implementation.</span></span> <span data-ttu-id="b1db8-125">Ein Client sollte [IMAPIProp::GetProps](imapiprop-getprops.md) erst dann zur Eingabe seiner Werte aufrufen, wenn er von einem **IMAPIProp::SaveChanges-Aufruf ausgeführt** wurde.</span><span class="sxs-lookup"><span data-stu-id="b1db8-125">A client should not prompt [IMAPIProp::GetProps](imapiprop-getprops.md) for their values until they have been committed by an **IMAPIProp::SaveChanges** call.</span></span> 
  
<span data-ttu-id="b1db8-126">Die Betreffeigenschaften sind in der Regel kleine Zeichenfolgen mit weniger als 256 Zeichen, und ein Nachrichtenspeicheranbieter ist nicht verpflichtet, die OLE **IStream-Schnittstelle** für sie zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b1db8-126">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the OLE **IStream** interface on them.</span></span> <span data-ttu-id="b1db8-127">Ein Client sollte immer zuerst den Zugriff über die **IMAPIProp-Schnittstelle** versuchen und nur dann auf **IStream** zugreifen, **MAPI_E_NOT_ENOUGH_MEMORY** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b1db8-127">A client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b1db8-128">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b1db8-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b1db8-129">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b1db8-129">Protocol specifications</span></span>

<span data-ttu-id="b1db8-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1db8-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1db8-131">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="b1db8-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b1db8-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1db8-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1db8-133">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="b1db8-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="b1db8-134">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1db8-134">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1db8-135">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="b1db8-135">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b1db8-136">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="b1db8-136">Header files</span></span>

<span data-ttu-id="b1db8-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b1db8-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="b1db8-138">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="b1db8-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="b1db8-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b1db8-139">Mapitags.h</span></span>
  
> <span data-ttu-id="b1db8-140">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b1db8-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b1db8-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1db8-141">See also</span></span>



[<span data-ttu-id="b1db8-142">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b1db8-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b1db8-143">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="b1db8-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b1db8-144">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b1db8-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b1db8-145">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b1db8-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

