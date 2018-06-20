---
title: Kanonische PidTagRuleUserFlags-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleUserFlags
api_type:
- COM
ms.assetid: c5dfb21f-b35e-4521-bf2b-e3d03d98d75d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8a44c88cbc971d9d5358fc6b24093e56e9565eb1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795059"
---
# <a name="pidtagruleuserflags-canonical-property"></a><span data-ttu-id="5d6d5-103">Kanonische PidTagRuleUserFlags-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5d6d5-103">PidTagRuleUserFlags Canonical Property</span></span>

  
  
<span data-ttu-id="5d6d5-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5d6d5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5d6d5-105">Diese Eigenschaft wird vom Client für die ausschließliche Verwendung des Clients festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5d6d5-105">This property is set by the client for the exclusive use of the client.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5d6d5-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5d6d5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5d6d5-107">PR_RULE_USER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="5d6d5-107">PR_RULE_USER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="5d6d5-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="5d6d5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5d6d5-109">0x6678</span><span class="sxs-lookup"><span data-stu-id="5d6d5-109">0x6678</span></span>  <br/> |
|<span data-ttu-id="5d6d5-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5d6d5-110">Data type:</span></span>  <br/> |<span data-ttu-id="5d6d5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5d6d5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5d6d5-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5d6d5-112">Area:</span></span>  <br/> |<span data-ttu-id="5d6d5-113">Serverseitige Regeln</span><span class="sxs-lookup"><span data-stu-id="5d6d5-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d6d5-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5d6d5-114">Remarks</span></span>

<span data-ttu-id="5d6d5-115">Der Server muss den Wert dieser Eigenschaft beibehalten, wenn er vom Client festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="5d6d5-115">The server must preserve the value of this property if it was set by the client.</span></span> <span data-ttu-id="5d6d5-116">Der Server muss während Rule Evaluation und Verarbeitung ignorieren.</span><span class="sxs-lookup"><span data-stu-id="5d6d5-116">The server must ignore it during rule evaluation and processing.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5d6d5-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5d6d5-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5d6d5-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5d6d5-118">Protocol specifications</span></span>

<span data-ttu-id="5d6d5-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d6d5-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d6d5-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="5d6d5-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5d6d5-121">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d6d5-121">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d6d5-122">Eingehende e-Mail-Nachrichten auf einem Server bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="5d6d5-122">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5d6d5-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="5d6d5-123">Header files</span></span>

<span data-ttu-id="5d6d5-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5d6d5-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="5d6d5-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5d6d5-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="5d6d5-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5d6d5-126">Mapitags.h</span></span>
  
> <span data-ttu-id="5d6d5-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5d6d5-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5d6d5-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d6d5-128">See also</span></span>



[<span data-ttu-id="5d6d5-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5d6d5-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5d6d5-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5d6d5-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5d6d5-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5d6d5-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5d6d5-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5d6d5-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

