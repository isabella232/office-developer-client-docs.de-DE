---
title: Kanonische Pidtagrulestable (-Eigenschaft
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
# <a name="pidtagrulestable-canonical-property"></a><span data-ttu-id="08b04-103">Kanonische Pidtagrulestable (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="08b04-103">PidTagRulesTable Canonical Property</span></span>

  
  
<span data-ttu-id="08b04-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08b04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08b04-105">Enthält eine Tabelle mit allen Regeln, die auf einen Ordner angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="08b04-105">Contains a table with all rules applied to a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="08b04-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="08b04-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="08b04-107">PR_RULES_TABLE</span><span class="sxs-lookup"><span data-stu-id="08b04-107">PR_RULES_TABLE</span></span>  <br/> |
|<span data-ttu-id="08b04-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="08b04-108">Identifier:</span></span>  <br/> |<span data-ttu-id="08b04-109">0x3FE1</span><span class="sxs-lookup"><span data-stu-id="08b04-109">0x3FE1</span></span>  <br/> |
|<span data-ttu-id="08b04-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="08b04-110">Data type:</span></span>  <br/> |<span data-ttu-id="08b04-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="08b04-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="08b04-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="08b04-112">Area:</span></span>  <br/> |<span data-ttu-id="08b04-113">Server seitige Regeln</span><span class="sxs-lookup"><span data-stu-id="08b04-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08b04-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08b04-114">Remarks</span></span>

<span data-ttu-id="08b04-115">Diese Eigenschaft ist für alle Folder-Objekte auf einem Exchange-Server vorhanden, die Regeln aufweisen.</span><span class="sxs-lookup"><span data-stu-id="08b04-115">This property is present on all folder objects on an Exchange Server that have rules.</span></span> <span data-ttu-id="08b04-116">In dieser Eigenschaft enthaltene Werte werden zum Lesen und Ändern von Regeln verwendet.</span><span class="sxs-lookup"><span data-stu-id="08b04-116">Values included in this property are used for reading and modifying rules.</span></span> <span data-ttu-id="08b04-117">Sie können die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode mit dem **IID_IExchangeModifyTable** -Schnittstellenbezeichner verwenden, um eine [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) -Schnittstelle für die Rules-Tabelle in einem Ordner abzurufen.</span><span class="sxs-lookup"><span data-stu-id="08b04-117">You can use the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with the **IID_IExchangeModifyTable** interface identifier to obtain an [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to the rules table on a folder.</span></span> <span data-ttu-id="08b04-118">Sie können diese Schnittstelle verwenden, um diese Regeln zu lesen und zu ändern.</span><span class="sxs-lookup"><span data-stu-id="08b04-118">You can use this interface to read and modify those rules.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="08b04-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="08b04-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="08b04-120">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="08b04-120">Header files</span></span>

<span data-ttu-id="08b04-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="08b04-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="08b04-122">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="08b04-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="08b04-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="08b04-123">Mapitags.h</span></span>
  
> <span data-ttu-id="08b04-124">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="08b04-124">Contains definitions of properties listed as associated properties.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="08b04-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08b04-125">See also</span></span>



[<span data-ttu-id="08b04-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="08b04-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="08b04-127">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="08b04-127">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)


[<span data-ttu-id="08b04-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08b04-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="08b04-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08b04-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="08b04-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="08b04-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="08b04-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="08b04-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

