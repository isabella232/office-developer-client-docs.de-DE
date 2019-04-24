---
title: Kanonische Pidtagjunkthreshold (-Eigenschaft
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
ms.openlocfilehash: 078dfcc7c24870cf95a2a4b2385c34fbeb64fac0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326852"
---
# <a name="pidtagjunkthreshold-canonical-property"></a><span data-ttu-id="a95f8-103">Kanonische Pidtagjunkthreshold (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a95f8-103">PidTagJunkThreshold Canonical Property</span></span>

  
  
<span data-ttu-id="a95f8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a95f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a95f8-105">Gibt an, wie aggressiv eingehende e-Mails an den Junk-e-Mail-Ordner gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a95f8-105">Indicates how aggressively incoming mail should be sent to the Junk Email folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a95f8-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a95f8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a95f8-107">PR_JUNK_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="a95f8-107">PR_JUNK_THRESHOLD</span></span>  <br/> |
|<span data-ttu-id="a95f8-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="a95f8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a95f8-109">0x6101</span><span class="sxs-lookup"><span data-stu-id="a95f8-109">0x6101</span></span>  <br/> |
|<span data-ttu-id="a95f8-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a95f8-110">Data type:</span></span>  <br/> |<span data-ttu-id="a95f8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a95f8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a95f8-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a95f8-112">Area:</span></span>  <br/> |<span data-ttu-id="a95f8-113">Spam</span><span class="sxs-lookup"><span data-stu-id="a95f8-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a95f8-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a95f8-114">Remarks</span></span>

<span data-ttu-id="a95f8-115">Diese Eigenschaft entspricht der Filtereinstellung High/Low/None.</span><span class="sxs-lookup"><span data-stu-id="a95f8-115">This property corresponds to the high / low / none filter setting.</span></span> <span data-ttu-id="a95f8-116">Der Wert "0xFFFFFFFF" gibt an, dass keine Spamfilterung angewendet werden soll, es müssen jedoch weiterhin Sperrlisten angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="a95f8-116">A value of "0xFFFFFFFF" indicates that spam filtering should not be applied, however block lists must still be applied.</span></span> <span data-ttu-id="a95f8-117">Der Wert "0x80000000" gibt an, dass alle e-Mails Spam sind, mit Ausnahme der Nachrichten von Absendern in der Liste der vertrauenswürdigen Absender oder an Empfänger in der Liste der vertrauenswürdigen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="a95f8-117">A value of "0x80000000" indicates that all mail is spam except those messages from senders on the trusted senders list or sent to recipients on the trusted recipients list.</span></span> <span data-ttu-id="a95f8-118">Dafür gibt es folgende Werte:</span><span class="sxs-lookup"><span data-stu-id="a95f8-118">Values for this are as follows:</span></span>
  
|<span data-ttu-id="a95f8-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a95f8-119">**Value**</span></span>|<span data-ttu-id="a95f8-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a95f8-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a95f8-121">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="a95f8-121">0xFFFFFFFF</span></span>  <br/> |<span data-ttu-id="a95f8-122">Keine Spamfilterung</span><span class="sxs-lookup"><span data-stu-id="a95f8-122">No spam filtering</span></span>  <br/> |
|<span data-ttu-id="a95f8-123">0x00000006</span><span class="sxs-lookup"><span data-stu-id="a95f8-123">0x00000006</span></span>  <br/> |<span data-ttu-id="a95f8-124">Niedrige Spamfilterung</span><span class="sxs-lookup"><span data-stu-id="a95f8-124">Low spam filtering</span></span>  <br/> |
|<span data-ttu-id="a95f8-125">0x00000003</span><span class="sxs-lookup"><span data-stu-id="a95f8-125">0x00000003</span></span>  <br/> |<span data-ttu-id="a95f8-126">Hohe Spamfilterung</span><span class="sxs-lookup"><span data-stu-id="a95f8-126">High spam filtering</span></span>  <br/> |
|<span data-ttu-id="a95f8-127">0x80000000</span><span class="sxs-lookup"><span data-stu-id="a95f8-127">0x80000000</span></span>  <br/> |<span data-ttu-id="a95f8-128">Nur vertrauenswürdige Listen</span><span class="sxs-lookup"><span data-stu-id="a95f8-128">Trusted Lists Only</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a95f8-129">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a95f8-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a95f8-130">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a95f8-130">Protocol specifications</span></span>

<span data-ttu-id="a95f8-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a95f8-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a95f8-132">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="a95f8-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a95f8-133">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a95f8-133">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a95f8-134">Ermöglicht die Behandlung von Allow/Block-Listen und die Bestimmung von Junk-e-Mails.</span><span class="sxs-lookup"><span data-stu-id="a95f8-134">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a95f8-135">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="a95f8-135">Header files</span></span>

<span data-ttu-id="a95f8-136">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a95f8-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="a95f8-137">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="a95f8-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="a95f8-138">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="a95f8-138">Mapitags.h</span></span>
  
> <span data-ttu-id="a95f8-139">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="a95f8-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a95f8-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a95f8-140">See also</span></span>



[<span data-ttu-id="a95f8-141">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a95f8-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a95f8-142">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a95f8-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a95f8-143">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a95f8-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a95f8-144">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a95f8-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

