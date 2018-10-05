---
title: PidTagSearchFolderExpiration (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderExpiration
api_type:
- COM
ms.assetid: e5746090-c850-4e95-b1e7-a07e42c87179
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a119bb735f752719d292371d4dc43e72450b33c0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385945"
---
# <a name="pidtagsearchfolderexpiration-canonical-property"></a><span data-ttu-id="de3a2-103">PidTagSearchFolderExpiration (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="de3a2-103">PidTagSearchFolderExpiration Canonical Property</span></span>

  
  
<span data-ttu-id="de3a2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de3a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de3a2-105">Enthält die Uhrzeit, an dem der Suche Ordnercontainer veraltete werden, und aktualisiert oder neu erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="de3a2-105">Contains the time at which the search folder container will be stale and should be updated or recreated.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="de3a2-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="de3a2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="de3a2-107">PR_WB_SF_EXPIRATION</span><span class="sxs-lookup"><span data-stu-id="de3a2-107">PR_WB_SF_EXPIRATION</span></span>  <br/> |
|<span data-ttu-id="de3a2-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="de3a2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="de3a2-109">0x683A</span><span class="sxs-lookup"><span data-stu-id="de3a2-109">0x683A</span></span>  <br/> |
|<span data-ttu-id="de3a2-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="de3a2-110">Data type:</span></span>  <br/> |<span data-ttu-id="de3a2-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="de3a2-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="de3a2-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="de3a2-112">Area:</span></span>  <br/> |<span data-ttu-id="de3a2-113">Suche</span><span class="sxs-lookup"><span data-stu-id="de3a2-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de3a2-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="de3a2-114">Remarks</span></span>

<span data-ttu-id="de3a2-115">Diese Eigenschaft muss als die Anzahl der Minuten seit Mitternacht (Coordinated Universal Time, UTC) 1. Januar 1601 formatiert werden.</span><span class="sxs-lookup"><span data-stu-id="de3a2-115">This property must be formatted as the number of minutes since midnight Coordinated Universal Time (UTC) January 1, 1601.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="de3a2-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="de3a2-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="de3a2-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="de3a2-117">Protocol specifications</span></span>

<span data-ttu-id="de3a2-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de3a2-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de3a2-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="de3a2-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="de3a2-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de3a2-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de3a2-121">Gibt die Eigenschaften und Operationen für das Bearbeiten der Liste einer Suchkonfiguration-Ordner.</span><span class="sxs-lookup"><span data-stu-id="de3a2-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="de3a2-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="de3a2-122">Header files</span></span>

<span data-ttu-id="de3a2-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="de3a2-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="de3a2-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="de3a2-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="de3a2-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="de3a2-125">Mapitags.h</span></span>
  
> <span data-ttu-id="de3a2-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="de3a2-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="de3a2-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de3a2-127">See also</span></span>



[<span data-ttu-id="de3a2-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="de3a2-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="de3a2-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="de3a2-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="de3a2-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="de3a2-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="de3a2-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="de3a2-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

