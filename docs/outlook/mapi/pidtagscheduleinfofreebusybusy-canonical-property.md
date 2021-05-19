---
title: PidTagScheduleInfoFreeBusyBusy (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyBusy
api_type:
- COM
ms.assetid: 84d9c5b5-e734-4c07-b4cc-1d7b13c1ed19
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4fbf0d8b80fdb48e44480b2739a71aec43b88a05
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338654"
---
# <a name="pidtagscheduleinfofreebusybusy-canonical-property"></a><span data-ttu-id="5a9e0-103">PidTagScheduleInfoFreeBusyBusy (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5a9e0-103">PidTagScheduleInfoFreeBusyBusy Canonical Property</span></span>

  
  
<span data-ttu-id="5a9e0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a9e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a9e0-105">Enthält die Zeitblöcke, für die der Status ausgelastet ist.</span><span class="sxs-lookup"><span data-stu-id="5a9e0-105">Contains the blocks of time for which the status is busy.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5a9e0-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5a9e0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5a9e0-107">PR_SCHDINFO_FREEBUSY_BUSY</span><span class="sxs-lookup"><span data-stu-id="5a9e0-107">PR_SCHDINFO_FREEBUSY_BUSY</span></span>  <br/> |
|<span data-ttu-id="5a9e0-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="5a9e0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5a9e0-109">0x6854</span><span class="sxs-lookup"><span data-stu-id="5a9e0-109">0x6854</span></span>  <br/> |
|<span data-ttu-id="5a9e0-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5a9e0-110">Data type:</span></span>  <br/> |<span data-ttu-id="5a9e0-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="5a9e0-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="5a9e0-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5a9e0-112">Area:</span></span>  <br/> |<span data-ttu-id="5a9e0-113">Frei/Gebucht</span><span class="sxs-lookup"><span data-stu-id="5a9e0-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a9e0-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5a9e0-114">Remarks</span></span>

<span data-ttu-id="5a9e0-115">Das Format, die Berechnung und die Einschränkungen dieser Eigenschaft sind mit denen von **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) identisch, beziehen sich jedoch auf Termine, die im zugeordneten Kalenderobjekt als ausgelastet markiert sind.</span><span class="sxs-lookup"><span data-stu-id="5a9e0-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked busy on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5a9e0-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5a9e0-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5a9e0-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5a9e0-117">Protocol specifications</span></span>

<span data-ttu-id="5a9e0-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a9e0-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a9e0-119">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="5a9e0-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5a9e0-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a9e0-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a9e0-121">Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="5a9e0-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5a9e0-122">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="5a9e0-122">Header files</span></span>

<span data-ttu-id="5a9e0-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5a9e0-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="5a9e0-124">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5a9e0-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="5a9e0-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5a9e0-125">Mapitags.h</span></span>
  
> <span data-ttu-id="5a9e0-126">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="5a9e0-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5a9e0-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a9e0-127">See also</span></span>



[<span data-ttu-id="5a9e0-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5a9e0-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5a9e0-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="5a9e0-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5a9e0-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5a9e0-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5a9e0-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5a9e0-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

