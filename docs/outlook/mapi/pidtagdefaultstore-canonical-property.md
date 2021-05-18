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
ms.openlocfilehash: 0cbcc8185f6f46a1bfceb2dd6d0aaf9c5d7cab2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270105"
---
# <a name="pidtagdefaultstore-canonical-property"></a><span data-ttu-id="f43d6-103">PidTagDefaultStore (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f43d6-103">PidTagDefaultStore Canonical Property</span></span>

  
  
<span data-ttu-id="f43d6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f43d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f43d6-105">Enthält TRUE, wenn ein Nachrichtenspeicher der Standardnachrichtenspeicher in der Nachrichtenspeichertabelle ist.</span><span class="sxs-lookup"><span data-stu-id="f43d6-105">Contains TRUE if a message store is the default message store in the message store table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f43d6-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f43d6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f43d6-107">PR_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="f43d6-107">PR_DEFAULT_STORE</span></span>  <br/> |
|<span data-ttu-id="f43d6-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="f43d6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f43d6-109">0x3400</span><span class="sxs-lookup"><span data-stu-id="f43d6-109">0x3400</span></span>  <br/> |
|<span data-ttu-id="f43d6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f43d6-110">Data type:</span></span>  <br/> |<span data-ttu-id="f43d6-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f43d6-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f43d6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f43d6-112">Area:</span></span>  <br/> |<span data-ttu-id="f43d6-113">MAPI-Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="f43d6-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f43d6-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f43d6-114">Remarks</span></span>

<span data-ttu-id="f43d6-115">Diese Eigenschaft wird als Spalte in der Nachrichtenspeichertabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f43d6-115">This property appears as a column in the message store table.</span></span> <span data-ttu-id="f43d6-116">Der Wert basiert auf **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f43d6-116">The value is based on **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f43d6-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f43d6-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f43d6-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f43d6-118">Protocol specifications</span></span>

<span data-ttu-id="f43d6-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f43d6-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f43d6-120">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="f43d6-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f43d6-121">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="f43d6-121">Header files</span></span>

<span data-ttu-id="f43d6-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f43d6-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="f43d6-123">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f43d6-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="f43d6-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f43d6-124">Mapitags.h</span></span>
  
> <span data-ttu-id="f43d6-125">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="f43d6-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f43d6-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f43d6-126">See also</span></span>



[<span data-ttu-id="f43d6-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f43d6-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f43d6-128">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="f43d6-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f43d6-129">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f43d6-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f43d6-130">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f43d6-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

