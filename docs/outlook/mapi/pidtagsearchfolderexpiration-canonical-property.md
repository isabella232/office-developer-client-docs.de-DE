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
ms.openlocfilehash: a2f72f68926665087ee8e3a0c9e8394042a8f955
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590771"
---
# <a name="pidtagsearchfolderexpiration-canonical-property"></a><span data-ttu-id="91e35-103">PidTagSearchFolderExpiration (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="91e35-103">PidTagSearchFolderExpiration Canonical Property</span></span>

  
  
<span data-ttu-id="91e35-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91e35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91e35-105">Enthält die Uhrzeit, an dem der Suche Ordnercontainer veraltete werden, und aktualisiert oder neu erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="91e35-105">Contains the time at which the search folder container will be stale and should be updated or recreated.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="91e35-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="91e35-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="91e35-107">PR_WB_SF_EXPIRATION</span><span class="sxs-lookup"><span data-stu-id="91e35-107">PR_WB_SF_EXPIRATION</span></span>  <br/> |
|<span data-ttu-id="91e35-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="91e35-108">Identifier:</span></span>  <br/> |<span data-ttu-id="91e35-109">0x683A</span><span class="sxs-lookup"><span data-stu-id="91e35-109">0x683A</span></span>  <br/> |
|<span data-ttu-id="91e35-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="91e35-110">Data type:</span></span>  <br/> |<span data-ttu-id="91e35-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="91e35-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="91e35-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="91e35-112">Area:</span></span>  <br/> |<span data-ttu-id="91e35-113">Suche</span><span class="sxs-lookup"><span data-stu-id="91e35-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91e35-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="91e35-114">Remarks</span></span>

<span data-ttu-id="91e35-115">Diese Eigenschaft muss als die Anzahl der Minuten seit Mitternacht (Coordinated Universal Time, UTC) 1. Januar 1601 formatiert werden.</span><span class="sxs-lookup"><span data-stu-id="91e35-115">This property must be formatted as the number of minutes since midnight Coordinated Universal Time (UTC) January 1, 1601.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="91e35-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="91e35-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="91e35-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="91e35-117">Protocol specifications</span></span>

<span data-ttu-id="91e35-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91e35-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91e35-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="91e35-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="91e35-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91e35-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91e35-121">Gibt die Eigenschaften und Operationen für das Bearbeiten der Liste einer Suchkonfiguration-Ordner.</span><span class="sxs-lookup"><span data-stu-id="91e35-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="91e35-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="91e35-122">Header files</span></span>

<span data-ttu-id="91e35-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="91e35-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="91e35-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="91e35-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="91e35-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="91e35-125">Mapitags.h</span></span>
  
> <span data-ttu-id="91e35-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="91e35-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="91e35-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91e35-127">See also</span></span>



[<span data-ttu-id="91e35-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="91e35-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="91e35-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="91e35-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="91e35-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="91e35-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="91e35-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="91e35-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

