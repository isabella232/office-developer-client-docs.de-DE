---
title: PidTagNormalizedSubject (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 54a0f438dacc8a1c7838eb538ec05c5c263f1b0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329274"
---
# <a name="pidtagnormalizedsubject-canonical-property"></a><span data-ttu-id="67e08-103">PidTagNormalizedSubject (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="67e08-103">PidTagNormalizedSubject Canonical Property</span></span>

  
  
<span data-ttu-id="67e08-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67e08-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67e08-105">Enthält den Nachrichtenbe betreff mit einem beliebigen entfernten Präfix.</span><span class="sxs-lookup"><span data-stu-id="67e08-105">Contains the message subject with any prefix removed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="67e08-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="67e08-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="67e08-107">PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="67e08-107">PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="67e08-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="67e08-108">Identifier:</span></span>  <br/> |<span data-ttu-id="67e08-109">0x0E1D</span><span class="sxs-lookup"><span data-stu-id="67e08-109">0x0E1D</span></span>  <br/> |
|<span data-ttu-id="67e08-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="67e08-110">Data type:</span></span>  <br/> |<span data-ttu-id="67e08-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="67e08-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="67e08-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="67e08-112">Area:</span></span>  <br/> |<span data-ttu-id="67e08-113">E-Mails</span><span class="sxs-lookup"><span data-stu-id="67e08-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="67e08-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="67e08-114">Remarks</span></span>

<span data-ttu-id="67e08-115">Diese Eigenschaften werden von Nachrichtenspeicher oder Transportanbietern aus den **Eigenschaften PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) und PR_SUBJECT_PREFIX ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) auf folgende **Weise** berechnet.</span><span class="sxs-lookup"><span data-stu-id="67e08-115">These properties are computed by message store or transport providers from the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) and **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) properties in the following manner.</span></span>
  
- <span data-ttu-id="67e08-116">Wenn die  **PR_SUBJECT_PREFIX** vorhanden ist und eine anfängliche Teilzeichenfolge von **PR_SUBJECT** ist, werden **PR_NORMALIZED_SUBJECT** und zugeordnete Eigenschaften auf den Inhalt von PR_SUBJECT festgelegt, deren Präfix entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="67e08-116">If the **PR_SUBJECT_PREFIX** is present and is an initial substring of **PR_SUBJECT**, **PR_NORMALIZED_SUBJECT** and associated properties are set to the contents of **PR_SUBJECT** with the prefix removed.</span></span> 
    
- <span data-ttu-id="67e08-117">Wenn **PR_SUBJECT_PREFIX** vorhanden ist, es sich jedoch nicht um eine anfängliche Teilzeichenfolge von **PR_SUBJECT** handelt, wird **PR_SUBJECT_PREFIX** mithilfe der folgenden Regel aus **PR_SUBJECT** gelöscht und neu berechnet: Wenn die in **PR_SUBJECT** enthaltene Zeichenfolge mit ein bis drei nicht numerischen Zeichen beginnt, gefolgt von einem Doppelpunkt und einem Leerzeichen, wird die Zeichenfolge zusammen mit dem Doppelpunkt und dem Leeren zum Präfix.</span><span class="sxs-lookup"><span data-stu-id="67e08-117">If **PR_SUBJECT_PREFIX** is present, but it is not an initial substring of **PR_SUBJECT**, **PR_SUBJECT_PREFIX** is deleted and recalculated from **PR_SUBJECT** using the following rule: If the string contained in **PR_SUBJECT** begins with one to three non-numeric characters followed by a colon and a space, then the string together with the colon and the blank becomes the prefix.</span></span> <span data-ttu-id="67e08-118">Zahlen, Leerzeichen und Interpunktionszeichen sind keine gültigen Präfixzeichen.</span><span class="sxs-lookup"><span data-stu-id="67e08-118">Numbers, blanks, and punctuation characters are not valid prefix characters.</span></span> 
    
- <span data-ttu-id="67e08-119">Wenn **PR_SUBJECT_PREFIX** nicht vorhanden ist, wird  sie anhand PR_SUBJECT regel berechnet, die im vorherigen Schritt beschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="67e08-119">If **PR_SUBJECT_PREFIX** is not present, it is calculated from **PR_SUBJECT** using the rule outlined in the previous step.</span></span> <span data-ttu-id="67e08-120">Diese Eigenschaft wird dann auf den Inhalt der PR_SUBJECT **das** Präfix entfernt.</span><span class="sxs-lookup"><span data-stu-id="67e08-120">This property then is set to the contents of **PR_SUBJECT** with the prefix removed.</span></span> 
    
 <span data-ttu-id="67e08-121">**Hinweis** Wenn **PR_SUBJECT_PREFIX** eine leere Zeichenfolge ist, **sind PR_SUBJECT** und diese Eigenschaft identisch.</span><span class="sxs-lookup"><span data-stu-id="67e08-121">**Note** When **PR_SUBJECT_PREFIX** is an empty string, **PR_SUBJECT** and this property are the same.</span></span> 
  
<span data-ttu-id="67e08-122">Letztendlich sollte diese Eigenschaft teil der PR_SUBJECT **dem** Präfix folgen.</span><span class="sxs-lookup"><span data-stu-id="67e08-122">Ultimately, this property should be the part of **PR_SUBJECT** following the prefix.</span></span> <span data-ttu-id="67e08-123">Wenn es kein Präfix gibt, wird diese Eigenschaft mit **PR_SUBJECT.**</span><span class="sxs-lookup"><span data-stu-id="67e08-123">If there is no prefix, this property becomes the same as **PR_SUBJECT**.</span></span>
  
 <span data-ttu-id="67e08-124">**PR_SUBJECT_PREFIX** und diese Eigenschaft sollte als Teil der [IMAPIProp::SaveChanges-Implementierung berechnet](imapiprop-savechanges.md) werden.</span><span class="sxs-lookup"><span data-stu-id="67e08-124">**PR_SUBJECT_PREFIX** and this property should be computed as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) implementation.</span></span> <span data-ttu-id="67e08-125">Eine Clientanwendung sollte die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) erst dann zur Eingabe ihrer Werte aufrufen, wenn sie von einem **IMAPIProp::SaveChanges-Aufruf** ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="67e08-125">A client application should not prompt the [IMAPIProp::GetProps](imapiprop-getprops.md) method for their values until they have been committed by an **IMAPIProp::SaveChanges** call.</span></span> 
  
<span data-ttu-id="67e08-126">Die Betreffeigenschaften sind in der Regel kleine Zeichenfolgen mit weniger als 256 Zeichen, und ein Nachrichtenspeicheranbieter ist nicht verpflichtet, die **Ole-IStream-Schnittstelle** (Object Linking and Embedding) zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="67e08-126">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the Object Linking and Embedding (OLE) **IStream** interface on them.</span></span> <span data-ttu-id="67e08-127">Der Client sollte immer zuerst versuchen, über die **IMAPIProp-Schnittstelle** auf IStream zu zugreifen, und nur dann auf **IStream** zugreifen, MAPI_E_NOT_ENOUGH_MEMORY zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="67e08-127">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if MAPI_E_NOT_ENOUGH_MEMORY is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="67e08-128">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="67e08-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="67e08-129">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="67e08-129">Protocol specifications</span></span>

<span data-ttu-id="67e08-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67e08-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67e08-131">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="67e08-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="67e08-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67e08-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67e08-133">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="67e08-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="67e08-134">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67e08-134">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67e08-135">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="67e08-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="67e08-136">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="67e08-136">Header files</span></span>

<span data-ttu-id="67e08-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="67e08-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="67e08-138">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="67e08-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="67e08-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="67e08-139">Mapitags.h</span></span>
  
> <span data-ttu-id="67e08-140">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="67e08-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="67e08-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67e08-141">See also</span></span>



[<span data-ttu-id="67e08-142">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="67e08-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="67e08-143">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="67e08-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="67e08-144">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="67e08-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="67e08-145">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="67e08-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

