---
title: PidTagRulesTable (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fc520720-8190-4dff-8f6c-1bebf7080b57
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4b4b60084b8cb53a0a245b502b8fe70241fb4eb7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591689"
---
# <a name="pidtagrulestable-canonical-property"></a><span data-ttu-id="957b9-103">PidTagRulesTable (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="957b9-103">PidTagRulesTable Canonical Property</span></span>

  
  
<span data-ttu-id="957b9-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="957b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="957b9-105">Enthält eine Tabelle mit allen Regeln in einen Ordner angewendet.</span><span class="sxs-lookup"><span data-stu-id="957b9-105">Contains a table with all rules applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="957b9-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="957b9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="957b9-107">PR_RULES_TABLE</span><span class="sxs-lookup"><span data-stu-id="957b9-107">PR_RULES_TABLE</span></span>  <br/> |
|<span data-ttu-id="957b9-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="957b9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="957b9-109">0x3FE1</span><span class="sxs-lookup"><span data-stu-id="957b9-109">0x3FE1</span></span>  <br/> |
|<span data-ttu-id="957b9-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="957b9-110">Data type:</span></span>  <br/> |<span data-ttu-id="957b9-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="957b9-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="957b9-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="957b9-112">Area:</span></span>  <br/> |<span data-ttu-id="957b9-113">Serverseitige Regeln</span><span class="sxs-lookup"><span data-stu-id="957b9-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="957b9-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="957b9-114">Remarks</span></span>

<span data-ttu-id="957b9-115">Diese Eigenschaft ist auf alle Ordnerobjekte auf einem Exchange-Server, denen Regeln vorhanden.</span><span class="sxs-lookup"><span data-stu-id="957b9-115">This property is present on all folder objects on an Exchange Server that have rules.</span></span> <span data-ttu-id="957b9-116">Werte enthalten, die in dieser Eigenschaft werden beim Lesen und Ändern der Regeln verwendet.</span><span class="sxs-lookup"><span data-stu-id="957b9-116">Values included in this property are used for reading and modifying rules.</span></span> <span data-ttu-id="957b9-117">Sie können die [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode mit der **IID_IExchangeModifyTable** Interface Identifier verwenden, erhalten eine [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) -Schnittstelle für die Regeltabelle für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="957b9-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the rules table on a folder.</span></span> <span data-ttu-id="957b9-118">Sie können diese Schnittstelle zum Lesen und ändern diese Regeln verwenden.</span><span class="sxs-lookup"><span data-stu-id="957b9-118">You can use this interface to read and modify those rules.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="957b9-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="957b9-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="957b9-120">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="957b9-120">Header files</span></span>

<span data-ttu-id="957b9-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="957b9-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="957b9-122">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="957b9-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="957b9-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="957b9-123">Mapitags.h</span></span>
  
> <span data-ttu-id="957b9-124">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="957b9-124">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="957b9-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="957b9-125">See also</span></span>



[<span data-ttu-id="957b9-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="957b9-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="957b9-127">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="957b9-127">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)


[<span data-ttu-id="957b9-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="957b9-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="957b9-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="957b9-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="957b9-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="957b9-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="957b9-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="957b9-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

