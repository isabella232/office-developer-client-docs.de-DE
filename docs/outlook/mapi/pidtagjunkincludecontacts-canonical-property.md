---
title: Kanonische PidTagJunkIncludeContacts-Eigenschaft
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
ms.openlocfilehash: 4dde93bbec2594804ab18a3ee4eb3e116a57e528
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794537"
---
# <a name="pidtagjunkincludecontacts-canonical-property"></a><span data-ttu-id="d73bb-103">Kanonische PidTagJunkIncludeContacts-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d73bb-103">PidTagJunkIncludeContacts Canonical Property</span></span>

  
  
<span data-ttu-id="d73bb-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d73bb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d73bb-105">Gibt an, ob e-Mail-Adressen der Kontakte im Ordner Kontakte speziell in Bezug auf den Spam-Filter behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="d73bb-105">Indicates whether email addresses of the contacts in the Contacts folder are treated specially with respect to the spam filter.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d73bb-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d73bb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d73bb-107">PR_JUNK_INCLUDE_CONTACTS</span><span class="sxs-lookup"><span data-stu-id="d73bb-107">PR_JUNK_INCLUDE_CONTACTS</span></span>  <br/> |
|<span data-ttu-id="d73bb-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="d73bb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d73bb-109">0x6100</span><span class="sxs-lookup"><span data-stu-id="d73bb-109">0x6100</span></span>  <br/> |
|<span data-ttu-id="d73bb-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d73bb-110">Data type:</span></span>  <br/> |<span data-ttu-id="d73bb-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d73bb-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d73bb-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d73bb-112">Area:</span></span>  <br/> |<span data-ttu-id="d73bb-113">Spam</span><span class="sxs-lookup"><span data-stu-id="d73bb-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d73bb-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d73bb-114">Remarks</span></span>

<span data-ttu-id="d73bb-115">Wenn Sie auf "0 x 00000001" festgelegt ist, diese e-Mail-Adressen den "vertrauenswürdigen" Kontakt-e-Mail-Adressteil der Junk-e-Mail Regel Einschränkung auffüllen müssen so, dass e-Mails von diesen Adressen als "kein junk" behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="d73bb-115">If set to "0x00000001", these email addresses must populate the "trusted" contact email address portion of the Junk E-Mail Rule Restriction such that mail from these addresses is treated as "not junk".</span></span> <span data-ttu-id="d73bb-116">Wenn auf "0 x 00000000" gesetzt, e-Mail-Adressen aus dem Ordner Kontakte nicht hinzugefügt werden die Regel für Junk-e-Mail müssen und im Abschnitt der Regel muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="d73bb-116">If set to "0x00000000", email addresses from the Contacts folder must not be added to the Junk E-Mail Rule, and the section of the rule must be NULL.</span></span>
  
<span data-ttu-id="d73bb-117">Wenn diese Eigenschaft vorhanden, mit dem Wert "0 x 00000001" und ist weist der hinzugefügte Kontakt e-Mail-Adressen, die noch nicht im Abschnitt vertrauenswürdige Kontakte von der Regel für Junk-e-Mail enthalten sind, müssen diese e-Mail-Adressen die Beschränkung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d73bb-117">If this property is present with a value of "0x00000001" and if the added contact has email addresses that are not yet included in the trusted contacts section of the Junk E-Mail Rule, those email addresses must be added to the restriction.</span></span> <span data-ttu-id="d73bb-118">Wenn diese Eigenschaft auf "0 x 00000000" ist, ist keine Aktion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d73bb-118">If this property is "0x00000000", no action is required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d73bb-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d73bb-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d73bb-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d73bb-120">Protocol specifications</span></span>

<span data-ttu-id="d73bb-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d73bb-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d73bb-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="d73bb-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d73bb-123">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d73bb-123">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d73bb-124">Ermöglicht die Behandlung von zulassen/blockieren-Listen und die Bestimmung des junk-e-Mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="d73bb-124">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d73bb-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="d73bb-125">Header files</span></span>

<span data-ttu-id="d73bb-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d73bb-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="d73bb-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d73bb-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="d73bb-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d73bb-128">Mapitags.h</span></span>
  
> <span data-ttu-id="d73bb-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d73bb-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d73bb-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d73bb-130">See also</span></span>



[<span data-ttu-id="d73bb-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d73bb-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d73bb-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d73bb-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d73bb-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d73bb-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d73bb-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d73bb-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

