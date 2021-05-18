---
title: PidTagFreeBusyRangeTimestamp (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyRangeTimestamp
api_type:
- HeaderDef
ms.assetid: 142d955f-f92d-485a-80c9-9c72e82af0f2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 24c3369d1d6db4977d26e4d31678a4f2cc5808a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316177"
---
# <a name="pidtagfreebusyrangetimestamp-canonical-property"></a><span data-ttu-id="e2e3e-103">PidTagFreeBusyRangeTimestamp (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e2e3e-103">PidTagFreeBusyRangeTimestamp Canonical Property</span></span>

  
  
<span data-ttu-id="e2e3e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2e3e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2e3e-105">Enthält den Zeitpunkt, zu dem die Daten veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="e2e3e-105">Contains the time when the data was published.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e2e3e-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e2e3e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e2e3e-107">PR_FREEBUSY_RANGE_TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="e2e3e-107">PR_FREEBUSY_RANGE_TIMESTAMP</span></span>  <br/> |
|<span data-ttu-id="e2e3e-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e2e3e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e2e3e-109">0x6868</span><span class="sxs-lookup"><span data-stu-id="e2e3e-109">0x6868</span></span>  <br/> |
|<span data-ttu-id="e2e3e-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e2e3e-110">Data type:</span></span>  <br/> |<span data-ttu-id="e2e3e-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="e2e3e-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="e2e3e-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e2e3e-112">Area:</span></span>  <br/> |<span data-ttu-id="e2e3e-113">Frei/Gebucht</span><span class="sxs-lookup"><span data-stu-id="e2e3e-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2e3e-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e2e3e-114">Remarks</span></span>

<span data-ttu-id="e2e3e-115">Diese Eigenschaft ist die Anzahl der Minuten seit Mitternacht, dem 1. Januar 1601 in koordinierter Weltzeit (UTC).</span><span class="sxs-lookup"><span data-stu-id="e2e3e-115">This property is the number of minutes since midnight, January 1, 1601 in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e2e3e-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e2e3e-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e2e3e-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e2e3e-117">Protocol specifications</span></span>

<span data-ttu-id="e2e3e-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2e3e-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2e3e-119">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e2e3e-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e2e3e-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2e3e-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2e3e-121">Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="e2e3e-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e2e3e-122">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="e2e3e-122">Header files</span></span>

<span data-ttu-id="e2e3e-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e2e3e-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="e2e3e-124">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e2e3e-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="e2e3e-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e2e3e-125">Mapitags.h</span></span>
  
> <span data-ttu-id="e2e3e-126">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e2e3e-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e2e3e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2e3e-127">See also</span></span>



[<span data-ttu-id="e2e3e-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e2e3e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e2e3e-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="e2e3e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e2e3e-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e2e3e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e2e3e-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e2e3e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

