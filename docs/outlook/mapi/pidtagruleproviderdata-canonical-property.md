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
ms.openlocfilehash: e4d209c4f185ff253476beb04913e6a64884f9b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335420"
---
# <a name="pidtagruleproviderdata-canonical-property"></a><span data-ttu-id="9808c-103">PidTagRuleProviderData (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9808c-103">PidTagRuleProviderData Canonical Property</span></span>

  
  
<span data-ttu-id="9808c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9808c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9808c-105">Eine undurchsichtige Eigenschaft, die der Client für die ausschließliche Verwendung des Clients legt.</span><span class="sxs-lookup"><span data-stu-id="9808c-105">An opaque property that the client sets for the exclusive use of the client.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9808c-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9808c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9808c-107">PR_RULE_PROVIDER_DATA</span><span class="sxs-lookup"><span data-stu-id="9808c-107">PR_RULE_PROVIDER_DATA</span></span>  <br/> |
|<span data-ttu-id="9808c-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="9808c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9808c-109">0x6684</span><span class="sxs-lookup"><span data-stu-id="9808c-109">0x6684</span></span>  <br/> |
|<span data-ttu-id="9808c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9808c-110">Data type:</span></span>  <br/> |<span data-ttu-id="9808c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9808c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9808c-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9808c-112">Area:</span></span>  <br/> |<span data-ttu-id="9808c-113">Serverseitige Regeln</span><span class="sxs-lookup"><span data-stu-id="9808c-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9808c-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9808c-114">Remarks</span></span>

<span data-ttu-id="9808c-115">Der Server muss den Wert dieser Eigenschaft beibehalten, wenn er vom Client festgelegt wurde, aber seinen Inhalt während der Regelauswertung und -verarbeitung ignorieren.</span><span class="sxs-lookup"><span data-stu-id="9808c-115">The server must preserve the value of this property if it was set by the client but must ignore its contents during rule evaluation and processing.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9808c-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9808c-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9808c-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="9808c-117">Protocol specifications</span></span>

<span data-ttu-id="9808c-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9808c-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9808c-119">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="9808c-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9808c-120">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9808c-120">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9808c-121">Bearbeitet eingehende E-Mail-Nachrichten auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="9808c-121">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9808c-122">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="9808c-122">Header files</span></span>

<span data-ttu-id="9808c-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9808c-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="9808c-124">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9808c-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="9808c-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9808c-125">Mapitags.h</span></span>
  
> <span data-ttu-id="9808c-126">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="9808c-126">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="9808c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9808c-127">See also</span></span>



[<span data-ttu-id="9808c-128">PidTagRuleProvider (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9808c-128">PidTagRuleProvider Canonical Property</span></span>](pidtagruleprovider-canonical-property.md)


[<span data-ttu-id="9808c-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9808c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9808c-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="9808c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9808c-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9808c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9808c-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9808c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

