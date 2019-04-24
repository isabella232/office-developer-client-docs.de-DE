---
title: Kanonische PidTagNormalizedSubject-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNormalizedSubject
api_type:
- HeaderDef
ms.assetid: 2000e6e8-d908-4814-8093-28f8011250c8
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 54a0f438dacc8a1c7838eb538ec05c5c263f1b0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329274"
---
# <a name="pidtagnormalizedsubject-canonical-property"></a><span data-ttu-id="f8c3d-103">Kanonische PidTagNormalizedSubject-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f8c3d-103">PidTagNormalizedSubject Canonical Property</span></span>

  
  
<span data-ttu-id="f8c3d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8c3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8c3d-105">Enthält den Betreff der Nachricht mit einem beliebigen Präfix entfernt.</span><span class="sxs-lookup"><span data-stu-id="f8c3d-105">Contains the message subject with any prefix removed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f8c3d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f8c3d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f8c3d-107">PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="f8c3d-107">PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="f8c3d-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="f8c3d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f8c3d-109">0x0E1D</span><span class="sxs-lookup"><span data-stu-id="f8c3d-109">0x0E1D</span></span>  <br/> |
|<span data-ttu-id="f8c3d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f8c3d-110">Data type:</span></span>  <br/> |<span data-ttu-id="f8c3d-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f8c3d-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f8c3d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f8c3d-112">Area:</span></span>  <br/> |<span data-ttu-id="f8c3d-113">E-Mail</span><span class="sxs-lookup"><span data-stu-id="f8c3d-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8c3d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8c3d-114">Remarks</span></span>

<span data-ttu-id="f8c3d-115">Diese Eigenschaften werden von den Nachrichtenspeicher-oder Transportanbietern aus den Eigenschaften **PR_Subject** ([PidTagSubject](pidtagsubject-canonical-property.md)) und **PR_SUBJECT_PREFIX** ([pidtagsubjectprefix (](pidtagsubjectprefix-canonical-property.md)) auf folgende Weise berechnet.</span><span class="sxs-lookup"><span data-stu-id="f8c3d-115">These properties are computed by message store or transport providers from the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) and **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) properties in the following manner.</span></span>
  
- <span data-ttu-id="f8c3d-116">Wenn **PR_SUBJECT_PREFIX** vorhanden ist und eine anfängliche Teilzeichenfolge von **PR_Subject**ist, werden **PR_NORMALIZED_SUBJECT** und zugehörige Eigenschaften auf den Inhalt von **PR_Subject** festgelegt, wobei das Präfix entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="f8c3d-116">If the **PR_SUBJECT_PREFIX** is present and is an initial substring of **PR_SUBJECT**, **PR_NORMALIZED_SUBJECT** and associated properties are set to the contents of **PR_SUBJECT** with the prefix removed.</span></span> 
    
- <span data-ttu-id="f8c3d-117">Wenn **PR_SUBJECT_PREFIX** vorhanden ist, aber keine anfängliche Teilzeichenfolge von **PR_Subject**ist, wird **PR_SUBJECT_PREFIX** gelöscht und von **PR_Subject** mithilfe der folgenden Regel neu berechnet: Wenn die in **PR_Subject** enthaltene Zeichenfolge beginnt mit einem bis drei nicht-numerischen Zeichen, gefolgt von einem Doppelpunkt und einem Raum, dann wird die Zeichenfolge zusammen mit dem Doppelpunkt und dem leeren das Präfix.</span><span class="sxs-lookup"><span data-stu-id="f8c3d-117">If **PR_SUBJECT_PREFIX** is present, but it is not an initial substring of **PR_SUBJECT**, **PR_SUBJECT_PREFIX** is deleted and recalculated from **PR_SUBJECT** using the following rule: If the string contained in **PR_SUBJECT** begins with one to three non-numeric characters followed by a colon and a space, then the string together with the colon and the blank becomes the prefix.</span></span> <span data-ttu-id="f8c3d-118">Zahlen, Leerzeichen und Interpunktionen sind keine gültigen Präfixzeichen.</span><span class="sxs-lookup"><span data-stu-id="f8c3d-118">Numbers, blanks, and punctuation characters are not valid prefix characters.</span></span> 
    
- <span data-ttu-id="f8c3d-119">Wenn **PR_SUBJECT_PREFIX** nicht vorhanden ist, wird es aus **PR_Subject** mithilfe der im vorherigen Schritt beschriebenen Regel berechnet.</span><span class="sxs-lookup"><span data-stu-id="f8c3d-119">If **PR_SUBJECT_PREFIX** is not present, it is calculated from **PR_SUBJECT** using the rule outlined in the previous step.</span></span> <span data-ttu-id="f8c3d-120">Diese Eigenschaft wird dann auf den Inhalt von **PR_Subject** festgelegt, wobei das Präfix entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="f8c3d-120">This property then is set to the contents of **PR_SUBJECT** with the prefix removed.</span></span> 
    
 <span data-ttu-id="f8c3d-121">**Hinweis** Wenn **PR_SUBJECT_PREFIX** eine leere Zeichenfolge ist, sind **PR_Subject** und diese Eigenschaft identisch.</span><span class="sxs-lookup"><span data-stu-id="f8c3d-121">**Note** When **PR_SUBJECT_PREFIX** is an empty string, **PR_SUBJECT** and this property are the same.</span></span> 
  
<span data-ttu-id="f8c3d-122">Schließlich sollte diese Eigenschaft der Teil von **PR_Subject** sein, der dem Präfix folgt.</span><span class="sxs-lookup"><span data-stu-id="f8c3d-122">Ultimately, this property should be the part of **PR_SUBJECT** following the prefix.</span></span> <span data-ttu-id="f8c3d-123">Wenn kein Präfix vorliegt, wird diese Eigenschaft mit **PR_Subject**identisch.</span><span class="sxs-lookup"><span data-stu-id="f8c3d-123">If there is no prefix, this property becomes the same as **PR_SUBJECT**.</span></span>
  
 <span data-ttu-id="f8c3d-124">**PR_SUBJECT_PREFIX** und diese Eigenschaft sollten als Teil der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Implementierung berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="f8c3d-124">**PR_SUBJECT_PREFIX** and this property should be computed as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) implementation.</span></span> <span data-ttu-id="f8c3d-125">Eine Clientanwendung sollte die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode für ihre Werte erst auffordern, nachdem Sie von einem **IMAPIProp:: SaveChanges** -Aufruf übergeben wurden.</span><span class="sxs-lookup"><span data-stu-id="f8c3d-125">A client application should not prompt the [IMAPIProp::GetProps](imapiprop-getprops.md) method for their values until they have been committed by an **IMAPIProp::SaveChanges** call.</span></span> 
  
<span data-ttu-id="f8c3d-126">Die Subject-Eigenschaften sind in der Regel kleine Zeichenfolgen mit weniger als 256 Zeichen, und ein Nachrichtenspeicher Anbieter ist nicht zur Unterstützung der OLE- **IStream** -Schnittstelle (Object Linking and Embedding) für Sie verpflichtet.</span><span class="sxs-lookup"><span data-stu-id="f8c3d-126">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the Object Linking and Embedding (OLE) **IStream** interface on them.</span></span> <span data-ttu-id="f8c3d-127">Der Client sollte immer versuchen, zuerst über die **IMAPIProp** -Schnittstelle zuzugreifen, und nur dann auf **IStream** zurückgreifen, wenn MAPI_E_NOT_ENOUGH_MEMORY wird.</span><span class="sxs-lookup"><span data-stu-id="f8c3d-127">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if MAPI_E_NOT_ENOUGH_MEMORY is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f8c3d-128">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f8c3d-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f8c3d-129">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f8c3d-129">Protocol specifications</span></span>

<span data-ttu-id="f8c3d-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f8c3d-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f8c3d-131">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="f8c3d-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f8c3d-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f8c3d-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f8c3d-133">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="f8c3d-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="f8c3d-134">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f8c3d-134">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f8c3d-135">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="f8c3d-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f8c3d-136">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="f8c3d-136">Header files</span></span>

<span data-ttu-id="f8c3d-137">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f8c3d-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="f8c3d-138">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="f8c3d-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="f8c3d-139">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="f8c3d-139">Mapitags.h</span></span>
  
> <span data-ttu-id="f8c3d-140">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="f8c3d-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f8c3d-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8c3d-141">See also</span></span>



[<span data-ttu-id="f8c3d-142">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f8c3d-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f8c3d-143">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f8c3d-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f8c3d-144">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f8c3d-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f8c3d-145">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f8c3d-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

