---
title: PidTagSubfolders (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubfolders
api_type:
- COM
ms.assetid: b456b07b-4d83-46bf-a305-4f322ea7dbd1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8de14542c0d2a4e6d95fb4258697b827f82b8d06
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384402"
---
# <a name="pidtagsubfolders-canonical-property"></a><span data-ttu-id="1759c-103">PidTagSubfolders (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1759c-103">PidTagSubfolders Canonical Property</span></span>

  
  
<span data-ttu-id="1759c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1759c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1759c-105">Enthält True, wenn ein Ordner Unterordner enthält.</span><span class="sxs-lookup"><span data-stu-id="1759c-105">Contains TRUE if a folder contains subfolders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1759c-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1759c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1759c-107">PR_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="1759c-107">PR_SUBFOLDERS</span></span>  <br/> |
|<span data-ttu-id="1759c-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="1759c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1759c-109">0x360A</span><span class="sxs-lookup"><span data-stu-id="1759c-109">0x360A</span></span>  <br/> |
|<span data-ttu-id="1759c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1759c-110">Data type:</span></span>  <br/> |<span data-ttu-id="1759c-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="1759c-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="1759c-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1759c-112">Area:</span></span>  <br/> |<span data-ttu-id="1759c-113">MAPI-container</span><span class="sxs-lookup"><span data-stu-id="1759c-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1759c-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1759c-114">Remarks</span></span>

<span data-ttu-id="1759c-115">Nachrichtenspeicher müssen diese Eigenschaft für alle Ordner angeben.</span><span class="sxs-lookup"><span data-stu-id="1759c-115">Message stores must supply this property for all folders.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1759c-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1759c-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1759c-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="1759c-117">Protocol specifications</span></span>

<span data-ttu-id="1759c-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1759c-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1759c-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="1759c-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1759c-120">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1759c-120">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1759c-121">Ordner Vorgänge behandelt.</span><span class="sxs-lookup"><span data-stu-id="1759c-121">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1759c-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="1759c-122">Header files</span></span>

<span data-ttu-id="1759c-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1759c-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="1759c-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1759c-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="1759c-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1759c-125">Mapitags.h</span></span>
  
> <span data-ttu-id="1759c-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1759c-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1759c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1759c-127">See also</span></span>



[<span data-ttu-id="1759c-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1759c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1759c-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1759c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1759c-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1759c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1759c-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1759c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

