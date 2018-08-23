---
title: PidTagScheduleInfoFreeBusyMerged (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5b83a4acf30f498a0d17cc2c3c76f40c2c3c4b96
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582014"
---
# <a name="pidtagscheduleinfofreebusymerged-canonical-property"></a><span data-ttu-id="9288b-103">PidTagScheduleInfoFreeBusyMerged (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9288b-103">PidTagScheduleInfoFreeBusyMerged Canonical Property</span></span>

  
  
<span data-ttu-id="9288b-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9288b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9288b-105">Enthält die Zeiten, der Frei/Gebucht-Status festgelegt wird, beschäftigt oder ABWESEND.</span><span class="sxs-lookup"><span data-stu-id="9288b-105">Contains the times for which the free/busy status is set to busy or OOF.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9288b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9288b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9288b-107">PR_SCHDINFO_FREEBUSY_MERGED</span><span class="sxs-lookup"><span data-stu-id="9288b-107">PR_SCHDINFO_FREEBUSY_MERGED</span></span>  <br/> |
|<span data-ttu-id="9288b-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="9288b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9288b-109">0x6850</span><span class="sxs-lookup"><span data-stu-id="9288b-109">0x6850</span></span>  <br/> |
|<span data-ttu-id="9288b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9288b-110">Data type:</span></span>  <br/> |<span data-ttu-id="9288b-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="9288b-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="9288b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9288b-112">Area:</span></span>  <br/> |<span data-ttu-id="9288b-113">Frei/Gebucht-Informationen</span><span class="sxs-lookup"><span data-stu-id="9288b-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9288b-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="9288b-114">Remarks</span></span>

<span data-ttu-id="9288b-115">Ereignisse vom Typ mit Vorbehalt Frei/Gebucht-Informationen sind nicht in dieser Eigenschaft enthalten.</span><span class="sxs-lookup"><span data-stu-id="9288b-115">Events of free/busy type tentative are not included in this property.</span></span> <span data-ttu-id="9288b-116">Das Format, Berechnung und die Einschränkungen dieser Eigenschaft werden die gleichen, die von **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)), aber finden Sie unter Termine, die im zugeordneten Kalender gebucht oder ABWESEND markiert sind.</span><span class="sxs-lookup"><span data-stu-id="9288b-116">The format, computation and the restrictions of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked OOF or busy on the associated calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9288b-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9288b-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9288b-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="9288b-118">Protocol specifications</span></span>

<span data-ttu-id="9288b-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9288b-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9288b-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="9288b-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9288b-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9288b-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9288b-122">Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="9288b-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9288b-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="9288b-123">Header files</span></span>

<span data-ttu-id="9288b-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9288b-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="9288b-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9288b-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="9288b-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9288b-126">Mapitags.h</span></span>
  
> <span data-ttu-id="9288b-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9288b-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9288b-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9288b-128">See also</span></span>



[<span data-ttu-id="9288b-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9288b-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9288b-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9288b-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9288b-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9288b-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9288b-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9288b-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

