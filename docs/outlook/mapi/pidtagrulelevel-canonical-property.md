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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 55627161010996d59cf495845e73515da2a75fcf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795035"
---
# <a name="pidtagrulelevel-canonical-property"></a><span data-ttu-id="cf21d-103">PidTagRuleLevel (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="cf21d-103">PidTagRuleLevel Canonical Property</span></span>

  
  
<span data-ttu-id="cf21d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cf21d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cf21d-105">Die Exit-Ebene einer Regel enthält.</span><span class="sxs-lookup"><span data-stu-id="cf21d-105">Contains the exit level of a rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cf21d-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="cf21d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cf21d-107">PR_RULE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="cf21d-107">PR_RULE_LEVEL</span></span>  <br/> |
|<span data-ttu-id="cf21d-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="cf21d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cf21d-109">0x6683</span><span class="sxs-lookup"><span data-stu-id="cf21d-109">0x6683</span></span>  <br/> |
|<span data-ttu-id="cf21d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="cf21d-110">Data type:</span></span>  <br/> |<span data-ttu-id="cf21d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cf21d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cf21d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="cf21d-112">Area:</span></span>  <br/> |<span data-ttu-id="cf21d-113">Serverseitige Regeln</span><span class="sxs-lookup"><span data-stu-id="cf21d-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cf21d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf21d-114">Remarks</span></span>

<span data-ttu-id="cf21d-115">Wenn diese Eigenschaft festlegen, muss der Client 0 x 00000000 übergeben.</span><span class="sxs-lookup"><span data-stu-id="cf21d-115">If setting this property, the client must pass in 0x00000000.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cf21d-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cf21d-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cf21d-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="cf21d-117">Protocol specifications</span></span>

<span data-ttu-id="cf21d-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cf21d-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cf21d-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="cf21d-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cf21d-120">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cf21d-120">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cf21d-121">Gibt die Methoden zum Verbinden mit und Postfächer als Stellvertreter und Interaktionen mit Nachrichten und Kalenderelemente konfigurieren, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="cf21d-121">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
<span data-ttu-id="cf21d-122">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cf21d-122">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cf21d-123">Eingehende e-Mail-Nachrichten auf einem Server bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="cf21d-123">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cf21d-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="cf21d-124">Header files</span></span>

<span data-ttu-id="cf21d-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cf21d-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="cf21d-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="cf21d-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="cf21d-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cf21d-127">Mapitags.h</span></span>
  
> <span data-ttu-id="cf21d-128">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="cf21d-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cf21d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf21d-129">See also</span></span>



[<span data-ttu-id="cf21d-130">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cf21d-130">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="cf21d-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cf21d-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cf21d-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cf21d-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cf21d-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="cf21d-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cf21d-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="cf21d-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

