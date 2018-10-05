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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385648"
---
# <a name="pidtagsubjectprefix-canonical-property"></a><span data-ttu-id="c2763-103">PidTagSubjectPrefix (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c2763-103">PidTagSubjectPrefix Canonical Property</span></span>

  
  
<span data-ttu-id="c2763-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2763-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c2763-105">Enthält eine Betreffpräfix, der in der Regel eine Aktion für eine Nachricht wie angibt "Firmware:" für die Weiterleitung.</span><span class="sxs-lookup"><span data-stu-id="c2763-105">Contains a subject prefix that typically indicates some action on a message, such as "FW: " for forwarding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c2763-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c2763-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c2763-107">PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W</span><span class="sxs-lookup"><span data-stu-id="c2763-107">PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W</span></span>  <br/> |
|<span data-ttu-id="c2763-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="c2763-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c2763-109">0x003D</span><span class="sxs-lookup"><span data-stu-id="c2763-109">0x003D</span></span>  <br/> |
|<span data-ttu-id="c2763-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c2763-110">Data type:</span></span>  <br/> |<span data-ttu-id="c2763-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c2763-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c2763-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c2763-112">Area:</span></span>  <br/> |<span data-ttu-id="c2763-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="c2763-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2763-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c2763-114">Remarks</span></span>

<span data-ttu-id="c2763-115">Diese Eigenschaften werden für alle Objekte, die Meldung empfohlen.</span><span class="sxs-lookup"><span data-stu-id="c2763-115">These properties are recommended on all message objects.</span></span> 
  
<span data-ttu-id="c2763-116">Das Betreffpräfix besteht aus einem oder mehreren alphanumerische Zeichen, gefolgt von einem Doppelpunkt und ein Leerzeichen (die Teil des Präfixes sind).</span><span class="sxs-lookup"><span data-stu-id="c2763-116">The subject prefix consists of one or more alphanumeric characters, followed by a colon and a space (which are part of the prefix).</span></span> <span data-ttu-id="c2763-117">Es muss nicht vor dem Doppelpunkt nicht alphanumerischen Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="c2763-117">It must not contain any nonalphanumeric characters before the colon.</span></span> <span data-ttu-id="c2763-118">Fehlen ein Präfix kann von dieser Eigenschaft nicht festgelegt oder eine leere Zeichenfolge dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c2763-118">Absence of a prefix can be represented by an empty string or by this property not being set.</span></span> 
  
<span data-ttu-id="c2763-119">Wenn diese Eigenschaften explizit festgelegt sind, die Zeichenfolge kann beliebig lang sein und beliebige alphanumerischen Zeichen verwenden, aber eine Teilzeichenfolge am Anfang der Eigenschaft **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) muss übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="c2763-119">If these properties are set explicitly, the string can be of any length and use any alphanumeric characters, but it must match a substring at the beginning of the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span> <span data-ttu-id="c2763-120">Wenn diese Eigenschaften nicht vom Absender festgelegt sind und berechnet werden müssen, werden ihre Inhalte eingegrenzte.</span><span class="sxs-lookup"><span data-stu-id="c2763-120">If these properties are not set by the sender and must be computed, their contents are more restricted.</span></span> <span data-ttu-id="c2763-121">Die Regel für das Präfix computing besteht darin, dass **PR_SUBJECT** mit einem, zwei oder drei Buchstaben beginnen müssen (alphabetische nur) gefolgt von einem Doppelpunkt und einem Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="c2763-121">The rule for computing the prefix is that **PR_SUBJECT** must begin with one, two, or three letters (alphabetic only) followed by a colon and a space.</span></span> <span data-ttu-id="c2763-122">Wenn eine solche eine Teilzeichenfolge am Anfang des **PR_SUBJECT**gefunden wird, es dann wird die Zeichenfolge für diese Eigenschaften (und bleibt auch am Anfang des **PR_SUBJECT**).</span><span class="sxs-lookup"><span data-stu-id="c2763-122">If such a substring is found at the beginning of **PR_SUBJECT**, it then becomes the string for these properties (and also stays at the beginning of **PR_SUBJECT**).</span></span> <span data-ttu-id="c2763-123">Andernfalls, bleiben diese Eigenschaften nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c2763-123">Otherwise, these properties remain unset.</span></span> 
  
<span data-ttu-id="c2763-124">Diese Eigenschaften und **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) sollte als Teil der Implementierung des [IMAPIProp::SaveChanges](imapiprop-savechanges.md) berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="c2763-124">These properties and **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) should be computed as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) implementation.</span></span> <span data-ttu-id="c2763-125">Ein Client sollte [IMAPIProp::GetProps](imapiprop-getprops.md) nicht für ihre Werte aufgefordert werden, bis sie gespeichert wurden durch einen Aufruf von **IMAPIProp::SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="c2763-125">A client should not prompt [IMAPIProp::GetProps](imapiprop-getprops.md) for their values until they have been committed by an **IMAPIProp::SaveChanges** call.</span></span> 
  
<span data-ttu-id="c2763-126">Subject-Eigenschaften in der Regel kleine Zeichenfolgen von weniger als 256 Zeichen sind, und eine Nachricht Speicheranbieter ist nicht verpflichtet, die OLE- **IStream** -Schnittstelle auf diese unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c2763-126">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the OLE **IStream** interface on them.</span></span> <span data-ttu-id="c2763-127">Ein Client sollte immer Zugriff über die Schnittstelle **IMAPIProp** zuerst versuchen, und greifen auf **IStream** nur, wenn **MAPI_E_NOT_ENOUGH_MEMORY** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c2763-127">A client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c2763-128">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c2763-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c2763-129">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c2763-129">Protocol specifications</span></span>

<span data-ttu-id="c2763-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c2763-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c2763-131">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="c2763-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c2763-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c2763-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c2763-133">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="c2763-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="c2763-134">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c2763-134">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c2763-135">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="c2763-135">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c2763-136">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="c2763-136">Header files</span></span>

<span data-ttu-id="c2763-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c2763-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="c2763-138">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c2763-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="c2763-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c2763-139">Mapitags.h</span></span>
  
> <span data-ttu-id="c2763-140">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c2763-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c2763-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2763-141">See also</span></span>



[<span data-ttu-id="c2763-142">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c2763-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c2763-143">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c2763-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c2763-144">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c2763-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c2763-145">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c2763-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

