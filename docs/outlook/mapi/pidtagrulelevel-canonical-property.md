---
title: PidTagRuleLevel (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleLevel
api_type:
- COM
ms.assetid: b1a30543-250d-4afb-87f2-448d90ee7cf9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3de5093f1fa395b1fba061f88a9b67b5dedf4740
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359528"
---
# <a name="pidtagrulelevel-canonical-property"></a><span data-ttu-id="d0a36-103">PidTagRuleLevel (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d0a36-103">PidTagRuleLevel Canonical Property</span></span>

  
  
<span data-ttu-id="d0a36-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0a36-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0a36-105">Enthält die Beendigungsebene einer Regel.</span><span class="sxs-lookup"><span data-stu-id="d0a36-105">Contains the exit level of a rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d0a36-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d0a36-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d0a36-107">PR_RULE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="d0a36-107">PR_RULE_LEVEL</span></span>  <br/> |
|<span data-ttu-id="d0a36-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="d0a36-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d0a36-109">0x6683</span><span class="sxs-lookup"><span data-stu-id="d0a36-109">0x6683</span></span>  <br/> |
|<span data-ttu-id="d0a36-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d0a36-110">Data type:</span></span>  <br/> |<span data-ttu-id="d0a36-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d0a36-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d0a36-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d0a36-112">Area:</span></span>  <br/> |<span data-ttu-id="d0a36-113">Serverseitige Regeln</span><span class="sxs-lookup"><span data-stu-id="d0a36-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0a36-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d0a36-114">Remarks</span></span>

<span data-ttu-id="d0a36-115">Wenn Sie diese Eigenschaft festlegen, muss der Client die 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="d0a36-115">If setting this property, the client must pass in 0x00000000.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d0a36-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d0a36-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d0a36-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d0a36-117">Protocol specifications</span></span>

<span data-ttu-id="d0a36-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0a36-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0a36-119">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="d0a36-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d0a36-120">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0a36-120">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0a36-121">Gibt Methoden zum Herstellen und Konfigurieren von Postfächern als Stellvertreter sowie Interaktionen mit Nachrichten- und Kalenderelementen an, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="d0a36-121">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
<span data-ttu-id="d0a36-122">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0a36-122">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0a36-123">Bearbeitet eingehende E-Mail-Nachrichten auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="d0a36-123">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d0a36-124">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="d0a36-124">Header files</span></span>

<span data-ttu-id="d0a36-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d0a36-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="d0a36-126">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d0a36-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="d0a36-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d0a36-127">Mapitags.h</span></span>
  
> <span data-ttu-id="d0a36-128">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="d0a36-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d0a36-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0a36-129">See also</span></span>



[<span data-ttu-id="d0a36-130">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d0a36-130">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="d0a36-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d0a36-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d0a36-132">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="d0a36-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d0a36-133">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d0a36-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d0a36-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d0a36-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

