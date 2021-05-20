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
ms.openlocfilehash: e1c670cd566e838104ae3d5480c2297f8632d899
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428501"
---
# <a name="pidtagrulestable-canonical-property"></a><span data-ttu-id="9fd66-103">PidTagRulesTable (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9fd66-103">PidTagRulesTable Canonical Property</span></span>

  
  
<span data-ttu-id="9fd66-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9fd66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9fd66-105">Enthält eine Tabelle mit allen Regeln, die auf einen Ordner angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="9fd66-105">Contains a table with all rules applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9fd66-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9fd66-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9fd66-107">PR_RULES_TABLE</span><span class="sxs-lookup"><span data-stu-id="9fd66-107">PR_RULES_TABLE</span></span>  <br/> |
|<span data-ttu-id="9fd66-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="9fd66-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9fd66-109">0x3FE1</span><span class="sxs-lookup"><span data-stu-id="9fd66-109">0x3FE1</span></span>  <br/> |
|<span data-ttu-id="9fd66-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9fd66-110">Data type:</span></span>  <br/> |<span data-ttu-id="9fd66-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="9fd66-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="9fd66-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9fd66-112">Area:</span></span>  <br/> |<span data-ttu-id="9fd66-113">Serverseitige Regeln</span><span class="sxs-lookup"><span data-stu-id="9fd66-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9fd66-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9fd66-114">Remarks</span></span>

<span data-ttu-id="9fd66-115">Diese Eigenschaft ist für alle Ordnerobjekte auf einer Exchange Server vorhanden, die Regeln haben.</span><span class="sxs-lookup"><span data-stu-id="9fd66-115">This property is present on all folder objects on an Exchange Server that have rules.</span></span> <span data-ttu-id="9fd66-116">In dieser Eigenschaft enthaltene Werte werden zum Lesen und Ändern von Regeln verwendet.</span><span class="sxs-lookup"><span data-stu-id="9fd66-116">Values included in this property are used for reading and modifying rules.</span></span> <span data-ttu-id="9fd66-117">Sie können die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) mit der IID_IExchangeModifyTable-Schnittstellen-ID verwenden, um eine [IExchangeModifyTable : IUnknown-Schnittstelle](iexchangemodifytableiunknown.md) zur Regeltabelle eines Ordners zu erhalten. </span><span class="sxs-lookup"><span data-stu-id="9fd66-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the rules table on a folder.</span></span> <span data-ttu-id="9fd66-118">Sie können diese Schnittstelle verwenden, um diese Regeln zu lesen und zu ändern.</span><span class="sxs-lookup"><span data-stu-id="9fd66-118">You can use this interface to read and modify those rules.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9fd66-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9fd66-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9fd66-120">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="9fd66-120">Header files</span></span>

<span data-ttu-id="9fd66-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9fd66-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="9fd66-122">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9fd66-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="9fd66-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9fd66-123">Mapitags.h</span></span>
  
> <span data-ttu-id="9fd66-124">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="9fd66-124">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="9fd66-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fd66-125">See also</span></span>



[<span data-ttu-id="9fd66-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9fd66-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="9fd66-127">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="9fd66-127">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)


[<span data-ttu-id="9fd66-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9fd66-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9fd66-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="9fd66-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9fd66-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9fd66-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9fd66-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9fd66-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

