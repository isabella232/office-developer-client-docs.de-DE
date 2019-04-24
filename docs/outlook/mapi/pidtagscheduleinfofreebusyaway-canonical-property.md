---
title: Kanonische Pidtagscheduleinfofreebusyaway (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyAway
api_type:
- COM
ms.assetid: 7b5d013a-15ac-469a-98c8-3ed1e80f6faf
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7520c473ee9373f8c23c4f5b4bb020291e2be007
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338507"
---
# <a name="pidtagscheduleinfofreebusyaway-canonical-property"></a><span data-ttu-id="e307a-103">Kanonische Pidtagscheduleinfofreebusyaway (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e307a-103">PidTagScheduleInfoFreeBusyAway Canonical Property</span></span>

  
  
<span data-ttu-id="e307a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e307a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e307a-105">Enthält die Zeiten, für die der Frei/Gebucht-Status auf OOF festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e307a-105">Contains the times for which the free/busy status is set to OOF.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e307a-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e307a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e307a-107">PR_SCHDINFO_FREEBUSY_OOF</span><span class="sxs-lookup"><span data-stu-id="e307a-107">PR_SCHDINFO_FREEBUSY_OOF</span></span>  <br/> |
|<span data-ttu-id="e307a-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="e307a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e307a-109">0x6856</span><span class="sxs-lookup"><span data-stu-id="e307a-109">0x6856</span></span>  <br/> |
|<span data-ttu-id="e307a-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e307a-110">Data type:</span></span>  <br/> |<span data-ttu-id="e307a-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="e307a-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="e307a-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e307a-112">Area:</span></span>  <br/> |<span data-ttu-id="e307a-113">Frei/Gebucht</span><span class="sxs-lookup"><span data-stu-id="e307a-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e307a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e307a-114">Remarks</span></span>

<span data-ttu-id="e307a-115">Das Format, die Berechnung und die Einschränkungen dieser Eigenschaft entsprechen denen von **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([pidtagscheduleinfofreebusytentative (](pidtagscheduleinfofreebusytentative-canonical-property.md)), beziehen sich jedoch auf Termine, die als OOF im zugeordneten Kalender gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="e307a-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked OOF on the associated calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e307a-116">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e307a-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e307a-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e307a-117">Protocol specifications</span></span>

<span data-ttu-id="e307a-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e307a-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e307a-119">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e307a-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e307a-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e307a-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e307a-121">Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="e307a-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e307a-122">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="e307a-122">Header files</span></span>

<span data-ttu-id="e307a-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e307a-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="e307a-124">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="e307a-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="e307a-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e307a-125">Mapitags.h</span></span>
  
> <span data-ttu-id="e307a-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e307a-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e307a-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e307a-127">See also</span></span>



[<span data-ttu-id="e307a-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e307a-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e307a-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e307a-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e307a-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e307a-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e307a-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e307a-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

