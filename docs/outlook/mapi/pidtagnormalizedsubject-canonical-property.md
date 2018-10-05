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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393229"
---
# <a name="pidtagnormalizedsubject-canonical-property"></a><span data-ttu-id="47b31-103">PidTagNormalizedSubject (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="47b31-103">PidTagNormalizedSubject Canonical Property</span></span>

  
  
<span data-ttu-id="47b31-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47b31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47b31-105">Enthält den Betreff der Nachricht mit dem Präfix entfernt.</span><span class="sxs-lookup"><span data-stu-id="47b31-105">Contains the message subject with any prefix removed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="47b31-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="47b31-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="47b31-107">PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="47b31-107">PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="47b31-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="47b31-108">Identifier:</span></span>  <br/> |<span data-ttu-id="47b31-109">0x0E1D</span><span class="sxs-lookup"><span data-stu-id="47b31-109">0x0E1D</span></span>  <br/> |
|<span data-ttu-id="47b31-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="47b31-110">Data type:</span></span>  <br/> |<span data-ttu-id="47b31-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="47b31-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="47b31-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="47b31-112">Area:</span></span>  <br/> |<span data-ttu-id="47b31-113">E-Mail</span><span class="sxs-lookup"><span data-stu-id="47b31-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="47b31-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="47b31-114">Remarks</span></span>

<span data-ttu-id="47b31-115">Diese Eigenschaften werden berechnet, indem Nachrichtenspeicher oder transport-Anbieter aus der **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) und **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md))-Eigenschaften auf folgende Weise.</span><span class="sxs-lookup"><span data-stu-id="47b31-115">These properties are computed by message store or transport providers from the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) and **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) properties in the following manner.</span></span>
  
- <span data-ttu-id="47b31-116">Wenn die **PR_SUBJECT_PREFIX** vorhanden ist und eine anfängliche Teilzeichenfolge **PR_SUBJECT**ist, werden **PR_NORMALIZED_SUBJECT** und die zugehörigen Eigenschaften auf den Inhalt der **PR_SUBJECT** mit dem Präfix entfernt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="47b31-116">If the **PR_SUBJECT_PREFIX** is present and is an initial substring of **PR_SUBJECT**, **PR_NORMALIZED_SUBJECT** and associated properties are set to the contents of **PR_SUBJECT** with the prefix removed.</span></span> 
    
- <span data-ttu-id="47b31-117">Wenn es sich nicht um eine anfängliche Teilzeichenfolge **PR_SUBJECT**, aber **PR_SUBJECT_PREFIX** vorhanden ist, wird **PR_SUBJECT_PREFIX** gelöscht und neu berechnet aus **PR_SUBJECT** mithilfe der folgenden Regel: Wenn die Zeichenfolge in **PR_SUBJECT** enthalten beginnt mit ein bis drei numerische Zeichen, gefolgt von einem Doppelpunkt und ein Leerzeichen ein, und klicken Sie dann die Zeichenfolge zusammen mit dem Doppelpunkt und die leere das Präfix wird.</span><span class="sxs-lookup"><span data-stu-id="47b31-117">If **PR_SUBJECT_PREFIX** is present, but it is not an initial substring of **PR_SUBJECT**, **PR_SUBJECT_PREFIX** is deleted and recalculated from **PR_SUBJECT** using the following rule: If the string contained in **PR_SUBJECT** begins with one to three non-numeric characters followed by a colon and a space, then the string together with the colon and the blank becomes the prefix.</span></span> <span data-ttu-id="47b31-118">Zahlen, Leerzeichen und Interpunktionszeichen sind keine gültigen Präfixzeichen.</span><span class="sxs-lookup"><span data-stu-id="47b31-118">Numbers, blanks, and punctuation characters are not valid prefix characters.</span></span> 
    
- <span data-ttu-id="47b31-119">Wenn **PR_SUBJECT_PREFIX** nicht vorhanden ist, wird es von **PR_SUBJECT** mithilfe der Regel, die im vorherigen Schritt beschrieben berechnet.</span><span class="sxs-lookup"><span data-stu-id="47b31-119">If **PR_SUBJECT_PREFIX** is not present, it is calculated from **PR_SUBJECT** using the rule outlined in the previous step.</span></span> <span data-ttu-id="47b31-120">Diese Eigenschaft wird auf den Inhalt der **PR_SUBJECT** mit dem Präfix entfernt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="47b31-120">This property then is set to the contents of **PR_SUBJECT** with the prefix removed.</span></span> 
    
 <span data-ttu-id="47b31-121">**Hinweis** Wenn **PR_SUBJECT_PREFIX** eine leere Zeichenfolge ist, sind **PR_SUBJECT** und diese Eigenschaft identisch.</span><span class="sxs-lookup"><span data-stu-id="47b31-121">**Note** When **PR_SUBJECT_PREFIX** is an empty string, **PR_SUBJECT** and this property are the same.</span></span> 
  
<span data-ttu-id="47b31-122">Schließlich sollte diese Eigenschaft den Teil des **PR_SUBJECT** hinter dem Präfix sein.</span><span class="sxs-lookup"><span data-stu-id="47b31-122">Ultimately, this property should be the part of **PR_SUBJECT** following the prefix.</span></span> <span data-ttu-id="47b31-123">Wenn kein Präfix vorhanden ist, wird diese Eigenschaft **PR_SUBJECT**identisch.</span><span class="sxs-lookup"><span data-stu-id="47b31-123">If there is no prefix, this property becomes the same as **PR_SUBJECT**.</span></span>
  
 <span data-ttu-id="47b31-124">**PR_SUBJECT_PREFIX** und diese Eigenschaft sollte als Teil der Implementierung des [IMAPIProp::SaveChanges](imapiprop-savechanges.md) berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="47b31-124">**PR_SUBJECT_PREFIX** and this property should be computed as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) implementation.</span></span> <span data-ttu-id="47b31-125">Eine Clientanwendung sollte nicht die [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode für ihre Werte aufgefordert, bis sie gespeichert wurden durch einen Aufruf von **IMAPIProp::SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="47b31-125">A client application should not prompt the [IMAPIProp::GetProps](imapiprop-getprops.md) method for their values until they have been committed by an **IMAPIProp::SaveChanges** call.</span></span> 
  
<span data-ttu-id="47b31-126">Die Subject-Eigenschaften in der Regel kleine Zeichenfolgen von weniger als 256 Zeichen sind, und eine Nachricht Speicheranbieter ist nicht verpflichtet, klicken sie auf die Object Linking and Embedding (OLE) **IStream** -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="47b31-126">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the Object Linking and Embedding (OLE) **IStream** interface on them.</span></span> <span data-ttu-id="47b31-127">Der Client sollte immer Zugriff über die Schnittstelle **IMAPIProp** zuerst versuchen, und greifen auf **IStream** nur, wenn MAPI_E_NOT_ENOUGH_MEMORY zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="47b31-127">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if MAPI_E_NOT_ENOUGH_MEMORY is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="47b31-128">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="47b31-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="47b31-129">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="47b31-129">Protocol specifications</span></span>

<span data-ttu-id="47b31-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47b31-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47b31-131">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="47b31-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="47b31-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47b31-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47b31-133">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="47b31-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="47b31-134">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47b31-134">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47b31-135">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="47b31-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="47b31-136">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="47b31-136">Header files</span></span>

<span data-ttu-id="47b31-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="47b31-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="47b31-138">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="47b31-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="47b31-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="47b31-139">Mapitags.h</span></span>
  
> <span data-ttu-id="47b31-140">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="47b31-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="47b31-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47b31-141">See also</span></span>



[<span data-ttu-id="47b31-142">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="47b31-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="47b31-143">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="47b31-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="47b31-144">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="47b31-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="47b31-145">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="47b31-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

