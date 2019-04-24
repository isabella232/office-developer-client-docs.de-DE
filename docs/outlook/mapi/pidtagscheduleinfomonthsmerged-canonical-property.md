---
title: Kanonische Pidtagscheduleinfomonthsmerged (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsMerged
api_type:
- COM
ms.assetid: b13b5d7b-413e-4405-8a35-0422477a9e86
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 53bc27b4ddd05b4a52328c605a6d4f673c91afd2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336477"
---
# <a name="pidtagscheduleinfomonthsmerged-canonical-property"></a><span data-ttu-id="2348e-103">Kanonische Pidtagscheduleinfomonthsmerged (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2348e-103">PidTagScheduleInfoMonthsMerged Canonical Property</span></span>

  
  
<span data-ttu-id="2348e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2348e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2348e-105">Enthält eine Liste der Monate, für die Frei/Gebucht-Daten des Typs busy oder eine ABWESENHEITsnachricht (abwesend) in der Frei/Gebucht-Nachricht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="2348e-105">Contains a list of the months for which free/busy data of type busy or an out of office (OOF) message is present in the free/busy message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2348e-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2348e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2348e-107">PR_SCHDINFO_MONTHS_MERGED</span><span class="sxs-lookup"><span data-stu-id="2348e-107">PR_SCHDINFO_MONTHS_MERGED</span></span>  <br/> |
|<span data-ttu-id="2348e-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="2348e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2348e-109">0x684F</span><span class="sxs-lookup"><span data-stu-id="2348e-109">0x684F</span></span>  <br/> |
|<span data-ttu-id="2348e-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="2348e-110">Data type:</span></span>  <br/> |<span data-ttu-id="2348e-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="2348e-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="2348e-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2348e-112">Area:</span></span>  <br/> |<span data-ttu-id="2348e-113">Frei/Gebucht</span><span class="sxs-lookup"><span data-stu-id="2348e-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2348e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2348e-114">Remarks</span></span>

<span data-ttu-id="2348e-115">Ereignisse mit dem Typ "frei/gebucht" sind in dieser Eigenschaft nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="2348e-115">Events of free/busy type tentative are not included in this property.</span></span> <span data-ttu-id="2348e-116">Die Syntax/das Format und die Einschränkungen dieser Eigenschaft entsprechen denen von **PR_SCHDINFO_MONTHS_TENTATIVE** ([pidtagscheduleinfomonthstentative (](pidtagscheduleinfomonthstentative-canonical-property.md)), beziehen sich jedoch auf Termine, die im zugeordneten Calendar-Objekt OOF oder busy markiert sind.</span><span class="sxs-lookup"><span data-stu-id="2348e-116">The syntax/format and constraints of this property are the same as those of **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) but refer to appointments that are marked OOF or Busy on the associated calendar object.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2348e-117">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2348e-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2348e-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="2348e-118">Protocol specifications</span></span>

<span data-ttu-id="2348e-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2348e-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2348e-120">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="2348e-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2348e-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2348e-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2348e-122">Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="2348e-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2348e-123">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="2348e-123">Header files</span></span>

<span data-ttu-id="2348e-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2348e-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="2348e-125">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="2348e-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="2348e-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="2348e-126">Mapitags.h</span></span>
  
> <span data-ttu-id="2348e-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="2348e-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2348e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2348e-128">See also</span></span>



[<span data-ttu-id="2348e-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2348e-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2348e-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2348e-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2348e-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2348e-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2348e-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2348e-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

