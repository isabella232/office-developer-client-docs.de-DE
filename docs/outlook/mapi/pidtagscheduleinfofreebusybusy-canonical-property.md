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
ms.openlocfilehash: 1f068ce2e8d98caa7d8733a182c051a820848333
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579809"
---
# <a name="pidtagscheduleinfofreebusybusy-canonical-property"></a><span data-ttu-id="9cc5e-103">PidTagScheduleInfoFreeBusyBusy (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9cc5e-103">PidTagScheduleInfoFreeBusyBusy Canonical Property</span></span>

  
  
<span data-ttu-id="9cc5e-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9cc5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9cc5e-105">Enthält die Blöcke mit Zeit, die für die der Status beschäftigt ist.</span><span class="sxs-lookup"><span data-stu-id="9cc5e-105">Contains the blocks of time for which the status is busy.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9cc5e-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9cc5e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9cc5e-107">PR_SCHDINFO_FREEBUSY_BUSY</span><span class="sxs-lookup"><span data-stu-id="9cc5e-107">PR_SCHDINFO_FREEBUSY_BUSY</span></span>  <br/> |
|<span data-ttu-id="9cc5e-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="9cc5e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9cc5e-109">0x6854</span><span class="sxs-lookup"><span data-stu-id="9cc5e-109">0x6854</span></span>  <br/> |
|<span data-ttu-id="9cc5e-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9cc5e-110">Data type:</span></span>  <br/> |<span data-ttu-id="9cc5e-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="9cc5e-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="9cc5e-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9cc5e-112">Area:</span></span>  <br/> |<span data-ttu-id="9cc5e-113">Frei/Gebucht-Informationen</span><span class="sxs-lookup"><span data-stu-id="9cc5e-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9cc5e-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="9cc5e-114">Remarks</span></span>

<span data-ttu-id="9cc5e-115">Das Format, Berechnung und Einschränkungen dieser Eigenschaft werden die gleichen, die von **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)), aber finden Sie unter Termine, die auf das zugehörige Calendar-Objekt gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="9cc5e-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked busy on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9cc5e-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9cc5e-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9cc5e-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="9cc5e-117">Protocol specifications</span></span>

<span data-ttu-id="9cc5e-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9cc5e-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9cc5e-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="9cc5e-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9cc5e-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9cc5e-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9cc5e-121">Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="9cc5e-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9cc5e-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="9cc5e-122">Header files</span></span>

<span data-ttu-id="9cc5e-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9cc5e-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="9cc5e-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9cc5e-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="9cc5e-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9cc5e-125">Mapitags.h</span></span>
  
> <span data-ttu-id="9cc5e-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9cc5e-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9cc5e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9cc5e-127">See also</span></span>



[<span data-ttu-id="9cc5e-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9cc5e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9cc5e-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9cc5e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9cc5e-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9cc5e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9cc5e-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9cc5e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

