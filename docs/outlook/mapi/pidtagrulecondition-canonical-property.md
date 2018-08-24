---
title: PidTagRuleCondition (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleCondition
api_type:
- COM
ms.assetid: 8a11e846-c62f-4c06-876f-94623d50cc3b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 81dbd097523f4cb5016a3e846f63cfbe1c643de2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575861"
---
# <a name="pidtagrulecondition-canonical-property"></a><span data-ttu-id="324a5-103">PidTagRuleCondition (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="324a5-103">PidTagRuleCondition Canonical Property</span></span>

  
  
<span data-ttu-id="324a5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="324a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="324a5-105">Die Bedingung verwendet, wenn Sie die Regel ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="324a5-105">The condition used when you evaluate the rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="324a5-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="324a5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="324a5-107">PR_RULE_CONDITION</span><span class="sxs-lookup"><span data-stu-id="324a5-107">PR_RULE_CONDITION</span></span>  <br/> |
|<span data-ttu-id="324a5-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="324a5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="324a5-109">0x6679</span><span class="sxs-lookup"><span data-stu-id="324a5-109">0x6679</span></span>  <br/> |
|<span data-ttu-id="324a5-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="324a5-110">Data type:</span></span>  <br/> |<span data-ttu-id="324a5-111">PT_SRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="324a5-111">PT_SRESTRICTION</span></span>  <br/> |
|<span data-ttu-id="324a5-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="324a5-112">Area:</span></span>  <br/> |<span data-ttu-id="324a5-113">Serverseitige Regeln</span><span class="sxs-lookup"><span data-stu-id="324a5-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="324a5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="324a5-114">Remarks</span></span>

<span data-ttu-id="324a5-115">Die Bedingung ist als eine **Einschränkung** und **PropertyValue** Puffer enthält die **Einschränkung** Struktur gepackt wie in [[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)angegeben.</span><span class="sxs-lookup"><span data-stu-id="324a5-115">The condition is expressed as a **Restriction** and the **PropertyValue** buffer contains the **Restriction** structure packaged as specified in [[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="324a5-116">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="324a5-116">MFCMAPI reference</span></span>

<span data-ttu-id="324a5-117">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="324a5-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="324a5-118">**Datei**</span><span class="sxs-lookup"><span data-stu-id="324a5-118">**File**</span></span>|<span data-ttu-id="324a5-119">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="324a5-119">**Function**</span></span>|<span data-ttu-id="324a5-120">**Comment**</span><span class="sxs-lookup"><span data-stu-id="324a5-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="324a5-121">ImportProcs.cpp</span><span class="sxs-lookup"><span data-stu-id="324a5-121">ImportProcs.cpp</span></span>  <br/> |<span data-ttu-id="324a5-122">PropCopyMore HrCopyRestriction</span><span class="sxs-lookup"><span data-stu-id="324a5-122">PropCopyMore, HrCopyRestriction</span></span>  <br/> |<span data-ttu-id="324a5-123">Diese Funktionen wird gezeigt, wie eine **PT_SRESTRICTION** -Eigenschaft im Zusammenhang mit einer anderen Eigenschaft kopieren von analysieren.</span><span class="sxs-lookup"><span data-stu-id="324a5-123">These functions demonstrate how to parse a **PT_SRESTRICTION** property for the purposes of copying to another property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="324a5-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="324a5-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="324a5-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="324a5-125">Protocol specifications</span></span>

<span data-ttu-id="324a5-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="324a5-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="324a5-127">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="324a5-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="324a5-128">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="324a5-128">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="324a5-129">Eingehende e-Mail-Nachrichten auf einem Server bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="324a5-129">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="324a5-130">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="324a5-130">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="324a5-131">Definiert die grundlegende Datenstrukturen, die verwendet werden remote-Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="324a5-131">Defines the basic data structures that are used in remote operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="324a5-132">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="324a5-132">Header files</span></span>

<span data-ttu-id="324a5-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="324a5-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="324a5-134">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="324a5-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="324a5-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="324a5-135">Mapitags.h</span></span>
  
> <span data-ttu-id="324a5-136">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="324a5-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="324a5-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="324a5-137">See also</span></span>



[<span data-ttu-id="324a5-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="324a5-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="324a5-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="324a5-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="324a5-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="324a5-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="324a5-141">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="324a5-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

