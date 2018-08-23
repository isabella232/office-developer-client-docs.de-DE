---
title: PidTagDefaultStore (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultStore
api_type:
- HeaderDef
ms.assetid: 6314d91c-4948-4fd1-bacc-932d4bb2c22f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d544c741685d401aaf36fe19be50ab402c9e5604
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592682"
---
# <a name="pidtagdefaultstore-canonical-property"></a><span data-ttu-id="f4daa-103">PidTagDefaultStore (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f4daa-103">PidTagDefaultStore Canonical Property</span></span>

  
  
<span data-ttu-id="f4daa-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4daa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4daa-105">Enthält True, wenn ein Nachrichtenspeicher Standard-Informationsspeicher in der Nachricht Store-Tabelle ist.</span><span class="sxs-lookup"><span data-stu-id="f4daa-105">Contains TRUE if a message store is the default message store in the message store table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f4daa-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f4daa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f4daa-107">PR_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="f4daa-107">PR_DEFAULT_STORE</span></span>  <br/> |
|<span data-ttu-id="f4daa-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="f4daa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f4daa-109">0x3400</span><span class="sxs-lookup"><span data-stu-id="f4daa-109">0x3400</span></span>  <br/> |
|<span data-ttu-id="f4daa-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f4daa-110">Data type:</span></span>  <br/> |<span data-ttu-id="f4daa-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f4daa-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f4daa-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f4daa-112">Area:</span></span>  <br/> |<span data-ttu-id="f4daa-113">MAPI-Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="f4daa-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4daa-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="f4daa-114">Remarks</span></span>

<span data-ttu-id="f4daa-115">Diese Eigenschaft wird als eine Spalte in der Nachricht Store Tabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f4daa-115">This property appears as a column in the message store table.</span></span> <span data-ttu-id="f4daa-116">Der Wert basiert auf **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f4daa-116">The value is based on **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f4daa-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f4daa-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f4daa-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f4daa-118">Protocol specifications</span></span>

<span data-ttu-id="f4daa-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4daa-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4daa-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="f4daa-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f4daa-121">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="f4daa-121">Header files</span></span>

<span data-ttu-id="f4daa-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f4daa-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="f4daa-123">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f4daa-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="f4daa-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f4daa-124">Mapitags.h</span></span>
  
> <span data-ttu-id="f4daa-125">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f4daa-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f4daa-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4daa-126">See also</span></span>



[<span data-ttu-id="f4daa-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f4daa-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f4daa-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f4daa-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f4daa-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f4daa-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f4daa-130">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f4daa-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

