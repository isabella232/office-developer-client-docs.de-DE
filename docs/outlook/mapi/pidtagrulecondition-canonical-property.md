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
ms.openlocfilehash: 5b513bc5ff6b95b26a96e36a4d04a49737cf6216
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359507"
---
# <a name="pidtagrulecondition-canonical-property"></a><span data-ttu-id="fdf75-103">PidTagRuleCondition (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fdf75-103">PidTagRuleCondition Canonical Property</span></span>

  
  
<span data-ttu-id="fdf75-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fdf75-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fdf75-105">Die Bedingung, die beim Auswerten der Regel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fdf75-105">The condition used when you evaluate the rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fdf75-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="fdf75-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fdf75-107">PR_RULE_CONDITION</span><span class="sxs-lookup"><span data-stu-id="fdf75-107">PR_RULE_CONDITION</span></span>  <br/> |
|<span data-ttu-id="fdf75-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="fdf75-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fdf75-109">0x6679</span><span class="sxs-lookup"><span data-stu-id="fdf75-109">0x6679</span></span>  <br/> |
|<span data-ttu-id="fdf75-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="fdf75-110">Data type:</span></span>  <br/> |<span data-ttu-id="fdf75-111">PT_SRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="fdf75-111">PT_SRESTRICTION</span></span>  <br/> |
|<span data-ttu-id="fdf75-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="fdf75-112">Area:</span></span>  <br/> |<span data-ttu-id="fdf75-113">Serverseitige Regeln</span><span class="sxs-lookup"><span data-stu-id="fdf75-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fdf75-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fdf75-114">Remarks</span></span>

<span data-ttu-id="fdf75-115">Die Bedingung wird als **Einschränkung ausgedrückt,** und der **PropertyValue-Puffer** enthält die In [[MS-OXCDATA] angegebene Einschränkungsstruktur.](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) </span><span class="sxs-lookup"><span data-stu-id="fdf75-115">The condition is expressed as a **Restriction** and the **PropertyValue** buffer contains the **Restriction** structure packaged as specified in [[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fdf75-116">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="fdf75-116">MFCMAPI reference</span></span>

<span data-ttu-id="fdf75-117">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="fdf75-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fdf75-118">**Datei**</span><span class="sxs-lookup"><span data-stu-id="fdf75-118">**File**</span></span>|<span data-ttu-id="fdf75-119">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="fdf75-119">**Function**</span></span>|<span data-ttu-id="fdf75-120">**Comment**</span><span class="sxs-lookup"><span data-stu-id="fdf75-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fdf75-121">ImportProcs.cpp</span><span class="sxs-lookup"><span data-stu-id="fdf75-121">ImportProcs.cpp</span></span>  <br/> |<span data-ttu-id="fdf75-122">PropCopyMore, HrCopyRestriction</span><span class="sxs-lookup"><span data-stu-id="fdf75-122">PropCopyMore, HrCopyRestriction</span></span>  <br/> |<span data-ttu-id="fdf75-123">Diese Funktionen veranschaulichen, wie eine **PT_SRESTRICTION** zum Kopieren in eine andere Eigenschaft analysiert wird.</span><span class="sxs-lookup"><span data-stu-id="fdf75-123">These functions demonstrate how to parse a **PT_SRESTRICTION** property for the purposes of copying to another property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="fdf75-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fdf75-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fdf75-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="fdf75-125">Protocol specifications</span></span>

<span data-ttu-id="fdf75-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fdf75-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fdf75-127">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="fdf75-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fdf75-128">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fdf75-128">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fdf75-129">Bearbeitet eingehende E-Mail-Nachrichten auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="fdf75-129">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="fdf75-130">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fdf75-130">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fdf75-131">Definiert die grundlegenden Datenstrukturen, die in Remotevorgängen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fdf75-131">Defines the basic data structures that are used in remote operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fdf75-132">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="fdf75-132">Header files</span></span>

<span data-ttu-id="fdf75-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fdf75-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="fdf75-134">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="fdf75-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="fdf75-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fdf75-135">Mapitags.h</span></span>
  
> <span data-ttu-id="fdf75-136">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="fdf75-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fdf75-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fdf75-137">See also</span></span>



[<span data-ttu-id="fdf75-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fdf75-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fdf75-139">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="fdf75-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fdf75-140">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="fdf75-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fdf75-141">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="fdf75-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

