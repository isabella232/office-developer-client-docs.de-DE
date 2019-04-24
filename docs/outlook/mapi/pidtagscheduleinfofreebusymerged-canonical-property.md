---
title: Kanonische Pidtagscheduleinfofreebusymerged (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyMerged
api_type:
- COM
ms.assetid: 3ebfccb6-967a-4f8e-9d94-94c50ba65438
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8d15c6cb256fb1e80e3c94bdfe7e71bd8625aa35
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338717"
---
# <a name="pidtagscheduleinfofreebusymerged-canonical-property"></a><span data-ttu-id="8c2a8-103">Kanonische Pidtagscheduleinfofreebusymerged (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8c2a8-103">PidTagScheduleInfoFreeBusyMerged Canonical Property</span></span>

  
  
<span data-ttu-id="8c2a8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c2a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c2a8-105">Enthält die Zeiten, für die der Frei/Gebucht-Status auf beschäftigt oder OOF festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8c2a8-105">Contains the times for which the free/busy status is set to busy or OOF.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8c2a8-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8c2a8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8c2a8-107">PR_SCHDINFO_FREEBUSY_MERGED</span><span class="sxs-lookup"><span data-stu-id="8c2a8-107">PR_SCHDINFO_FREEBUSY_MERGED</span></span>  <br/> |
|<span data-ttu-id="8c2a8-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="8c2a8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8c2a8-109">0x6850</span><span class="sxs-lookup"><span data-stu-id="8c2a8-109">0x6850</span></span>  <br/> |
|<span data-ttu-id="8c2a8-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8c2a8-110">Data type:</span></span>  <br/> |<span data-ttu-id="8c2a8-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="8c2a8-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="8c2a8-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8c2a8-112">Area:</span></span>  <br/> |<span data-ttu-id="8c2a8-113">Frei/Gebucht</span><span class="sxs-lookup"><span data-stu-id="8c2a8-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c2a8-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c2a8-114">Remarks</span></span>

<span data-ttu-id="8c2a8-115">Ereignisse mit dem Typ "frei/gebucht" sind in dieser Eigenschaft nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="8c2a8-115">Events of free/busy type tentative are not included in this property.</span></span> <span data-ttu-id="8c2a8-116">Das Format, die Berechnung und die Einschränkungen dieser Eigenschaft sind identisch mit denen von **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([pidtagscheduleinfofreebusytentative (](pidtagscheduleinfofreebusytentative-canonical-property.md)), beziehen sich jedoch auf Termine, die als OOF oder busy im zugeordneten Kalender gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="8c2a8-116">The format, computation and the restrictions of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked OOF or busy on the associated calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8c2a8-117">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8c2a8-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8c2a8-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="8c2a8-118">Protocol specifications</span></span>

<span data-ttu-id="8c2a8-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c2a8-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c2a8-120">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="8c2a8-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8c2a8-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c2a8-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c2a8-122">Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="8c2a8-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8c2a8-123">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="8c2a8-123">Header files</span></span>

<span data-ttu-id="8c2a8-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8c2a8-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="8c2a8-125">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="8c2a8-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="8c2a8-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="8c2a8-126">Mapitags.h</span></span>
  
> <span data-ttu-id="8c2a8-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="8c2a8-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8c2a8-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c2a8-128">See also</span></span>



[<span data-ttu-id="8c2a8-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8c2a8-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8c2a8-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8c2a8-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8c2a8-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8c2a8-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8c2a8-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8c2a8-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

