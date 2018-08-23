---
title: PidTagRuleProviderData (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleProviderData
api_type:
- COM
ms.assetid: b04a277c-b483-4f54-b360-311034b9a7ee
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f4f1070b89971c631fd855a6f84d56b699152421
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566845"
---
# <a name="pidtagruleproviderdata-canonical-property"></a><span data-ttu-id="053e2-103">PidTagRuleProviderData (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="053e2-103">PidTagRuleProviderData Canonical Property</span></span>

  
  
<span data-ttu-id="053e2-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="053e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="053e2-105">Eine nicht transparent-Eigenschaft, die der Client für die ausschließliche Verwendung des Clients festgelegt.</span><span class="sxs-lookup"><span data-stu-id="053e2-105">An opaque property that the client sets for the exclusive use of the client.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="053e2-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="053e2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="053e2-107">PR_RULE_PROVIDER_DATA</span><span class="sxs-lookup"><span data-stu-id="053e2-107">PR_RULE_PROVIDER_DATA</span></span>  <br/> |
|<span data-ttu-id="053e2-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="053e2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="053e2-109">0x6684</span><span class="sxs-lookup"><span data-stu-id="053e2-109">0x6684</span></span>  <br/> |
|<span data-ttu-id="053e2-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="053e2-110">Data type:</span></span>  <br/> |<span data-ttu-id="053e2-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="053e2-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="053e2-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="053e2-112">Area:</span></span>  <br/> |<span data-ttu-id="053e2-113">Serverseitige Regeln</span><span class="sxs-lookup"><span data-stu-id="053e2-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="053e2-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="053e2-114">Remarks</span></span>

<span data-ttu-id="053e2-115">Der Server muss den Wert dieser Eigenschaft beibehalten, wenn er vom Client festgelegt wurde aber seinen Inhalt während Rule Evaluation und Verarbeitung ignorieren muss.</span><span class="sxs-lookup"><span data-stu-id="053e2-115">The server must preserve the value of this property if it was set by the client but must ignore its contents during rule evaluation and processing.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="053e2-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="053e2-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="053e2-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="053e2-117">Protocol specifications</span></span>

<span data-ttu-id="053e2-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="053e2-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="053e2-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="053e2-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="053e2-120">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="053e2-120">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="053e2-121">Eingehende e-Mail-Nachrichten auf einem Server bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="053e2-121">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="053e2-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="053e2-122">Header files</span></span>

<span data-ttu-id="053e2-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="053e2-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="053e2-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="053e2-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="053e2-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="053e2-125">Mapitags.h</span></span>
  
> <span data-ttu-id="053e2-126">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="053e2-126">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="053e2-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="053e2-127">See also</span></span>



[<span data-ttu-id="053e2-128">PidTagRuleProvider (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="053e2-128">PidTagRuleProvider Canonical Property</span></span>](pidtagruleprovider-canonical-property.md)


[<span data-ttu-id="053e2-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="053e2-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="053e2-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="053e2-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="053e2-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="053e2-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="053e2-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="053e2-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

