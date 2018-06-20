---
title: Kanonische PidTagDefaultStore-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 573ac849bba026ec6a5988220a7e49688393440d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794285"
---
# <a name="pidtagdefaultstore-canonical-property"></a><span data-ttu-id="9035f-103">Kanonische PidTagDefaultStore-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9035f-103">PidTagDefaultStore Canonical Property</span></span>

  
  
<span data-ttu-id="9035f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9035f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9035f-105">Enthält True, wenn ein Nachrichtenspeicher Standard-Informationsspeicher in der Nachricht Store-Tabelle ist.</span><span class="sxs-lookup"><span data-stu-id="9035f-105">Contains TRUE if a message store is the default message store in the message store table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9035f-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9035f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9035f-107">PR_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="9035f-107">PR_DEFAULT_STORE</span></span>  <br/> |
|<span data-ttu-id="9035f-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="9035f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9035f-109">0x3400</span><span class="sxs-lookup"><span data-stu-id="9035f-109">0x3400</span></span>  <br/> |
|<span data-ttu-id="9035f-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9035f-110">Data type:</span></span>  <br/> |<span data-ttu-id="9035f-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="9035f-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="9035f-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9035f-112">Area:</span></span>  <br/> |<span data-ttu-id="9035f-113">MAPI-Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="9035f-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9035f-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9035f-114">Remarks</span></span>

<span data-ttu-id="9035f-115">Diese Eigenschaft wird als eine Spalte in der Nachricht Store Tabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9035f-115">This property appears as a column in the message store table.</span></span> <span data-ttu-id="9035f-116">Der Wert basiert auf **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9035f-116">The value is based on **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9035f-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9035f-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9035f-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="9035f-118">Protocol specifications</span></span>

<span data-ttu-id="9035f-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9035f-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9035f-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="9035f-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9035f-121">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="9035f-121">Header files</span></span>

<span data-ttu-id="9035f-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9035f-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="9035f-123">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9035f-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="9035f-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9035f-124">Mapitags.h</span></span>
  
> <span data-ttu-id="9035f-125">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9035f-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9035f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9035f-126">See also</span></span>



[<span data-ttu-id="9035f-127">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9035f-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9035f-128">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9035f-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9035f-129">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9035f-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9035f-130">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9035f-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

