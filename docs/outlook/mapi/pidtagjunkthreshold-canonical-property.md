---
title: Kanonische PidTagJunkThreshold-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkThreshold
api_type:
- HeaderDef
ms.assetid: 8067e2b5-02df-4b96-8f66-509f5a48c8aa
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0f8484e195b1cda8e1d633133cdff89c571d8ecd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794538"
---
# <a name="pidtagjunkthreshold-canonical-property"></a><span data-ttu-id="2b344-103">Kanonische PidTagJunkThreshold-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2b344-103">PidTagJunkThreshold Canonical Property</span></span>

  
  
<span data-ttu-id="2b344-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2b344-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2b344-105">Gibt an, wie aggressiv eingehenden e-Mail-Nachrichten in den Junk-e-Mail-Ordner gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b344-105">Indicates how aggressively incoming mail should be sent to the Junk Email folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2b344-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2b344-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2b344-107">PR_JUNK_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="2b344-107">PR_JUNK_THRESHOLD</span></span>  <br/> |
|<span data-ttu-id="2b344-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="2b344-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2b344-109">0x6101</span><span class="sxs-lookup"><span data-stu-id="2b344-109">0x6101</span></span>  <br/> |
|<span data-ttu-id="2b344-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="2b344-110">Data type:</span></span>  <br/> |<span data-ttu-id="2b344-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2b344-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2b344-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2b344-112">Area:</span></span>  <br/> |<span data-ttu-id="2b344-113">Spam</span><span class="sxs-lookup"><span data-stu-id="2b344-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b344-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2b344-114">Remarks</span></span>

<span data-ttu-id="2b344-115">Diese Eigenschaft entspricht der hoch / niedrig / keine Einstellung filtern.</span><span class="sxs-lookup"><span data-stu-id="2b344-115">This property corresponds to the high / low / none filter setting.</span></span> <span data-ttu-id="2b344-116">Der Wert "0xFFFFFFFF" gibt an, dass Spam-Filterung nicht angewendet werden soll, jedoch Sperrlisten weiterhin angewendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="2b344-116">A value of "0xFFFFFFFF" indicates that spam filtering should not be applied, however block lists must still be applied.</span></span> <span data-ttu-id="2b344-117">Der Wert "0 x 80000000" gibt an, dass alle e-Mails Spam außer diese Nachrichten von Absendern in der Liste vertrauenswürdiger Absender oder an Empfänger in der Liste vertrauenswürdiger Empfänger gesendet.</span><span class="sxs-lookup"><span data-stu-id="2b344-117">A value of "0x80000000" indicates that all mail is spam except those messages from senders on the trusted senders list or sent to recipients on the trusted recipients list.</span></span> <span data-ttu-id="2b344-118">Werte für dieses sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2b344-118">Values for this are as follows:</span></span>
  
|<span data-ttu-id="2b344-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2b344-119">**Value**</span></span>|<span data-ttu-id="2b344-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2b344-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2b344-121">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="2b344-121">0xFFFFFFFF</span></span>  <br/> |<span data-ttu-id="2b344-122">Keine Spamfilterung</span><span class="sxs-lookup"><span data-stu-id="2b344-122">No spam filtering</span></span>  <br/> |
|<span data-ttu-id="2b344-123">0 x 00000006</span><span class="sxs-lookup"><span data-stu-id="2b344-123">0x00000006</span></span>  <br/> |<span data-ttu-id="2b344-124">Niedrige Spamfilterung</span><span class="sxs-lookup"><span data-stu-id="2b344-124">Low spam filtering</span></span>  <br/> |
|<span data-ttu-id="2b344-125">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="2b344-125">0x00000003</span></span>  <br/> |<span data-ttu-id="2b344-126">Hohe Spamfilterung</span><span class="sxs-lookup"><span data-stu-id="2b344-126">High spam filtering</span></span>  <br/> |
|<span data-ttu-id="2b344-127">0 x 80000000</span><span class="sxs-lookup"><span data-stu-id="2b344-127">0x80000000</span></span>  <br/> |<span data-ttu-id="2b344-128">Nur vertrauenswürdige Listen</span><span class="sxs-lookup"><span data-stu-id="2b344-128">Trusted Lists Only</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="2b344-129">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2b344-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2b344-130">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="2b344-130">Protocol specifications</span></span>

<span data-ttu-id="2b344-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2b344-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2b344-132">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="2b344-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2b344-133">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2b344-133">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2b344-134">Ermöglicht die Behandlung von zulassen/blockieren-Listen und die Bestimmung des junk-e-Mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="2b344-134">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2b344-135">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="2b344-135">Header files</span></span>

<span data-ttu-id="2b344-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2b344-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="2b344-137">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="2b344-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="2b344-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2b344-138">Mapitags.h</span></span>
  
> <span data-ttu-id="2b344-139">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2b344-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2b344-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b344-140">See also</span></span>



[<span data-ttu-id="2b344-141">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2b344-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2b344-142">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2b344-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2b344-143">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2b344-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2b344-144">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2b344-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

