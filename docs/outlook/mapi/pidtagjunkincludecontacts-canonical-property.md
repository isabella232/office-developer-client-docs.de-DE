---
title: Kanonische Pidtagjunkincludecontacts (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkIncludeContacts
api_type:
- HeaderDef
ms.assetid: 25368f6c-4fba-4381-840c-ca122bd31b5f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7e61e98d1db1ab3acb958da353d8d22870937632
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328714"
---
# <a name="pidtagjunkincludecontacts-canonical-property"></a><span data-ttu-id="4f79b-103">Kanonische Pidtagjunkincludecontacts (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4f79b-103">PidTagJunkIncludeContacts Canonical Property</span></span>

  
  
<span data-ttu-id="4f79b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f79b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f79b-105">Gibt an, ob die e-Mail-Adressen der Kontakte im Ordner "Kontakte" speziell im Hinblick auf den Spamfilter behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="4f79b-105">Indicates whether email addresses of the contacts in the Contacts folder are treated specially with respect to the spam filter.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4f79b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4f79b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4f79b-107">PR_JUNK_INCLUDE_CONTACTS</span><span class="sxs-lookup"><span data-stu-id="4f79b-107">PR_JUNK_INCLUDE_CONTACTS</span></span>  <br/> |
|<span data-ttu-id="4f79b-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="4f79b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4f79b-109">0x6100</span><span class="sxs-lookup"><span data-stu-id="4f79b-109">0x6100</span></span>  <br/> |
|<span data-ttu-id="4f79b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4f79b-110">Data type:</span></span>  <br/> |<span data-ttu-id="4f79b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4f79b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4f79b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4f79b-112">Area:</span></span>  <br/> |<span data-ttu-id="4f79b-113">Spam</span><span class="sxs-lookup"><span data-stu-id="4f79b-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f79b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f79b-114">Remarks</span></span>

<span data-ttu-id="4f79b-115">Bei Festlegung auf "0x00000001" müssen diese e-Mail-Adressen den Teil "vertrauenswürdige" Kontakt-e-Mail-Adresse der Junk-e-Mail-Regel Einschränkung auffüllen, sodass e-Mails von diesen Adressen als "kein Junk" behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="4f79b-115">If set to "0x00000001", these email addresses must populate the "trusted" contact email address portion of the Junk E-Mail Rule Restriction such that mail from these addresses is treated as "not junk".</span></span> <span data-ttu-id="4f79b-116">Bei Festlegung auf "0x00000000" dürfen e-Mail-Adressen aus dem Ordner "Kontakte" nicht der Junk-e-Mail-Regel hinzugefügt werden, und der Abschnitt der Regel muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="4f79b-116">If set to "0x00000000", email addresses from the Contacts folder must not be added to the Junk E-Mail Rule, and the section of the rule must be NULL.</span></span>
  
<span data-ttu-id="4f79b-117">Wenn diese Eigenschaft mit dem Wert "0x00000001" vorhanden ist und der hinzugefügte Kontakt über e-Mail-Adressen verfügt, die noch nicht im Abschnitt vertrauenswürdige Kontakte der Junk-e-Mail-Regel enthalten sind, müssen diese e-Mail-Adressen der Einschränkung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="4f79b-117">If this property is present with a value of "0x00000001" and if the added contact has email addresses that are not yet included in the trusted contacts section of the Junk E-Mail Rule, those email addresses must be added to the restriction.</span></span> <span data-ttu-id="4f79b-118">Wenn diese Eigenschaft "0x00000000" ist, ist keine Aktion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4f79b-118">If this property is "0x00000000", no action is required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4f79b-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4f79b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4f79b-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4f79b-120">Protocol specifications</span></span>

<span data-ttu-id="4f79b-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f79b-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f79b-122">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="4f79b-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4f79b-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f79b-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f79b-124">Ermöglicht die Behandlung von Allow/Block-Listen und die Bestimmung von Junk-e-Mails.</span><span class="sxs-lookup"><span data-stu-id="4f79b-124">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4f79b-125">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="4f79b-125">Header files</span></span>

<span data-ttu-id="4f79b-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4f79b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="4f79b-127">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="4f79b-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="4f79b-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="4f79b-128">Mapitags.h</span></span>
  
> <span data-ttu-id="4f79b-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="4f79b-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4f79b-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f79b-130">See also</span></span>



[<span data-ttu-id="4f79b-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4f79b-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4f79b-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4f79b-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4f79b-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4f79b-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4f79b-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4f79b-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

