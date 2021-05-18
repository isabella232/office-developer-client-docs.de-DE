---
title: PidTagJunkIncludeContacts (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7e61e98d1db1ab3acb958da353d8d22870937632
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328714"
---
# <a name="pidtagjunkincludecontacts-canonical-property"></a><span data-ttu-id="53684-103">PidTagJunkIncludeContacts (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="53684-103">PidTagJunkIncludeContacts Canonical Property</span></span>

  
  
<span data-ttu-id="53684-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53684-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53684-105">Gibt an, ob E-Mail-Adressen der Kontakte im Ordner Kontakte speziell im Hinblick auf den Spamfilter behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="53684-105">Indicates whether email addresses of the contacts in the Contacts folder are treated specially with respect to the spam filter.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="53684-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="53684-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="53684-107">PR_JUNK_INCLUDE_CONTACTS</span><span class="sxs-lookup"><span data-stu-id="53684-107">PR_JUNK_INCLUDE_CONTACTS</span></span>  <br/> |
|<span data-ttu-id="53684-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="53684-108">Identifier:</span></span>  <br/> |<span data-ttu-id="53684-109">0x6100</span><span class="sxs-lookup"><span data-stu-id="53684-109">0x6100</span></span>  <br/> |
|<span data-ttu-id="53684-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="53684-110">Data type:</span></span>  <br/> |<span data-ttu-id="53684-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="53684-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="53684-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="53684-112">Area:</span></span>  <br/> |<span data-ttu-id="53684-113">Spam</span><span class="sxs-lookup"><span data-stu-id="53684-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53684-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="53684-114">Remarks</span></span>

<span data-ttu-id="53684-115">Wenn "0x00000001" festgelegt ist, müssen diese E-Mail-Adressen den Teil "vertrauenswürdige" Kontakt-E-Mail-Adresse der Junk-E-Mail-Regeleinschränkung auffüllen, damit E-Mails von diesen Adressen als "kein Junk" behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="53684-115">If set to "0x00000001", these email addresses must populate the "trusted" contact email address portion of the Junk E-Mail Rule Restriction such that mail from these addresses is treated as "not junk".</span></span> <span data-ttu-id="53684-116">Wenn "0x00000000" festgelegt ist, dürfen E-Mail-Adressen aus dem Ordner Kontakte nicht der Junk-E-Mail-Regel hinzugefügt werden, und der Abschnitt der Regel muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="53684-116">If set to "0x00000000", email addresses from the Contacts folder must not be added to the Junk E-Mail Rule, and the section of the rule must be NULL.</span></span>
  
<span data-ttu-id="53684-117">Wenn diese Eigenschaft mit dem Wert "0x00000001" vorhanden ist und der hinzugefügte Kontakt E-Mail-Adressen enthält, die noch nicht im Abschnitt vertrauenswürdige Kontakte der Junk-E-Mail-Regel enthalten sind, müssen diese E-Mail-Adressen der Einschränkung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="53684-117">If this property is present with a value of "0x00000001" and if the added contact has email addresses that are not yet included in the trusted contacts section of the Junk E-Mail Rule, those email addresses must be added to the restriction.</span></span> <span data-ttu-id="53684-118">Wenn diese Eigenschaft "0x00000000" ist, ist keine Aktion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="53684-118">If this property is "0x00000000", no action is required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="53684-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="53684-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="53684-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="53684-120">Protocol specifications</span></span>

<span data-ttu-id="53684-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53684-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53684-122">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="53684-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="53684-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53684-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53684-124">Ermöglicht die Behandlung von Zulässig-/Sperrlisten und die Ermittlung von Junk-E-Mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="53684-124">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="53684-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="53684-125">Header files</span></span>

<span data-ttu-id="53684-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="53684-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="53684-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="53684-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="53684-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="53684-128">Mapitags.h</span></span>
  
> <span data-ttu-id="53684-129">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="53684-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="53684-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53684-130">See also</span></span>



[<span data-ttu-id="53684-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="53684-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="53684-132">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="53684-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="53684-133">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="53684-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="53684-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="53684-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

