---
title: Kanonische PidTagScheduleInfoMonthsAway-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsAway
api_type:
- COM
ms.assetid: 282a8ba1-b786-4d17-b6c5-17e935e59a6b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6301cd86a81dfbf38666b6fb3ea326bc1f801490
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795102"
---
# <a name="pidtagscheduleinfomonthsaway-canonical-property"></a><span data-ttu-id="967a6-103">Kanonische PidTagScheduleInfoMonthsAway-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="967a6-103">PidTagScheduleInfoMonthsAway Canonical Property</span></span>

  
  
<span data-ttu-id="967a6-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="967a6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="967a6-105">Enthält eine Liste der Monate, für die Frei/Gebucht-Daten vom Typ abwesend (ABWESEND) in der Nachricht Frei/Gebucht-Informationen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="967a6-105">Contains a list of the months for which free/busy data of type out of office (OOF) is present in the free/busy message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="967a6-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="967a6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="967a6-107">PR_SCHDINFO_MONTHS_OOF</span><span class="sxs-lookup"><span data-stu-id="967a6-107">PR_SCHDINFO_MONTHS_OOF</span></span>  <br/> |
|<span data-ttu-id="967a6-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="967a6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="967a6-109">0x6855</span><span class="sxs-lookup"><span data-stu-id="967a6-109">0x6855</span></span>  <br/> |
|<span data-ttu-id="967a6-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="967a6-110">Data type:</span></span>  <br/> |<span data-ttu-id="967a6-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="967a6-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="967a6-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="967a6-112">Area:</span></span>  <br/> |<span data-ttu-id="967a6-113">Frei/Gebucht-Informationen</span><span class="sxs-lookup"><span data-stu-id="967a6-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="967a6-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="967a6-114">Remarks</span></span>

<span data-ttu-id="967a6-115">Das Format, Berechnung und Einschränkungen dieser Eigenschaft werden die gleichen, die von **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)), aber finden Sie unter Termine, die nicht im Büro (OOF) für das zugeordnete gekennzeichnet sind Calendar-Objekt.</span><span class="sxs-lookup"><span data-stu-id="967a6-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked out of office (OOF) on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="967a6-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="967a6-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="967a6-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="967a6-117">Protocol specifications</span></span>

<span data-ttu-id="967a6-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="967a6-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="967a6-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="967a6-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="967a6-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="967a6-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="967a6-121">Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="967a6-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="967a6-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="967a6-122">Header files</span></span>

<span data-ttu-id="967a6-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="967a6-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="967a6-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="967a6-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="967a6-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="967a6-125">Mapitags.h</span></span>
  
> <span data-ttu-id="967a6-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="967a6-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="967a6-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="967a6-127">See also</span></span>



[<span data-ttu-id="967a6-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="967a6-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="967a6-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="967a6-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="967a6-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="967a6-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="967a6-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="967a6-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
