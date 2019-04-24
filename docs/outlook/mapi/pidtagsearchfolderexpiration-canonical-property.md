---
title: Kanonische Pidtagsearchfolderexpiration (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a119bb735f752719d292371d4dc43e72450b33c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336470"
---
# <a name="pidtagsearchfolderexpiration-canonical-property"></a><span data-ttu-id="390ee-103">Kanonische Pidtagsearchfolderexpiration (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="390ee-103">PidTagSearchFolderExpiration Canonical Property</span></span>

  
  
<span data-ttu-id="390ee-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="390ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="390ee-105">Enthält die Zeit, zu der der Container für den Suchordner veraltet ist und aktualisiert oder neu erstellt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="390ee-105">Contains the time at which the search folder container will be stale and should be updated or recreated.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="390ee-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="390ee-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="390ee-107">PR_WB_SF_EXPIRATION</span><span class="sxs-lookup"><span data-stu-id="390ee-107">PR_WB_SF_EXPIRATION</span></span>  <br/> |
|<span data-ttu-id="390ee-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="390ee-108">Identifier:</span></span>  <br/> |<span data-ttu-id="390ee-109">0x683A</span><span class="sxs-lookup"><span data-stu-id="390ee-109">0x683A</span></span>  <br/> |
|<span data-ttu-id="390ee-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="390ee-110">Data type:</span></span>  <br/> |<span data-ttu-id="390ee-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="390ee-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="390ee-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="390ee-112">Area:</span></span>  <br/> |<span data-ttu-id="390ee-113">Suche</span><span class="sxs-lookup"><span data-stu-id="390ee-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="390ee-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="390ee-114">Remarks</span></span>

<span data-ttu-id="390ee-115">Diese Eigenschaft muss als Anzahl von Minuten seit Mitternacht koordinierter weltZeit (UTC) 1. Januar 1601 formatiert werden.</span><span class="sxs-lookup"><span data-stu-id="390ee-115">This property must be formatted as the number of minutes since midnight Coordinated Universal Time (UTC) January 1, 1601.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="390ee-116">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="390ee-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="390ee-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="390ee-117">Protocol specifications</span></span>

<span data-ttu-id="390ee-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="390ee-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="390ee-119">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="390ee-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="390ee-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="390ee-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="390ee-121">Gibt die Eigenschaften und Vorgänge zum Bearbeiten einer Suchordner Listen Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="390ee-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="390ee-122">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="390ee-122">Header files</span></span>

<span data-ttu-id="390ee-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="390ee-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="390ee-124">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="390ee-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="390ee-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="390ee-125">Mapitags.h</span></span>
  
> <span data-ttu-id="390ee-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="390ee-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="390ee-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="390ee-127">See also</span></span>



[<span data-ttu-id="390ee-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="390ee-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="390ee-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="390ee-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="390ee-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="390ee-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="390ee-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="390ee-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

