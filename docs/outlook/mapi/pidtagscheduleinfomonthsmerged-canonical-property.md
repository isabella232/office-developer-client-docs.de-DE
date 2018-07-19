---
title: PidTagScheduleInfoMonthsMerged (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c1096df0eff4b43239978620f4ccf2e9d221095a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795108"
---
# <a name="pidtagscheduleinfomonthsmerged-canonical-property"></a><span data-ttu-id="dbe7b-103">PidTagScheduleInfoMonthsMerged (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="dbe7b-103">PidTagScheduleInfoMonthsMerged Canonical Property</span></span>

  
  
<span data-ttu-id="dbe7b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dbe7b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dbe7b-105">Enthält eine Liste der, die Monate, für welche Frei/Gebucht-Daten vom Typ beschäftigt oder einen außerhalb von Office (OOF) Nachricht in der Frei/Gebucht-Nachricht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="dbe7b-105">Contains a list of the months for which free/busy data of type busy or an out of office (OOF) message is present in the free/busy message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dbe7b-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="dbe7b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dbe7b-107">PR_SCHDINFO_MONTHS_MERGED</span><span class="sxs-lookup"><span data-stu-id="dbe7b-107">PR_SCHDINFO_MONTHS_MERGED</span></span>  <br/> |
|<span data-ttu-id="dbe7b-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="dbe7b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dbe7b-109">0x684F</span><span class="sxs-lookup"><span data-stu-id="dbe7b-109">0x684F</span></span>  <br/> |
|<span data-ttu-id="dbe7b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="dbe7b-110">Data type:</span></span>  <br/> |<span data-ttu-id="dbe7b-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="dbe7b-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="dbe7b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="dbe7b-112">Area:</span></span>  <br/> |<span data-ttu-id="dbe7b-113">Frei/Gebucht-Informationen</span><span class="sxs-lookup"><span data-stu-id="dbe7b-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dbe7b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dbe7b-114">Remarks</span></span>

<span data-ttu-id="dbe7b-115">Ereignisse vom Typ mit Vorbehalt Frei/Gebucht-Informationen sind nicht in dieser Eigenschaft enthalten.</span><span class="sxs-lookup"><span data-stu-id="dbe7b-115">Events of free/busy type tentative are not included in this property.</span></span> <span data-ttu-id="dbe7b-116">Die Syntax der-Format und Integritätsregeln dieser Eigenschaft werden die gleichen, die von **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)), aber finden Sie unter Termine, die auf das zugehörige Calendar-Objekt ABWESEND oder beschäftigt gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="dbe7b-116">The syntax/format and constraints of this property are the same as those of **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) but refer to appointments that are marked OOF or Busy on the associated calendar object.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="dbe7b-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="dbe7b-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dbe7b-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="dbe7b-118">Protocol specifications</span></span>

<span data-ttu-id="dbe7b-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dbe7b-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dbe7b-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="dbe7b-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dbe7b-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dbe7b-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dbe7b-122">Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="dbe7b-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dbe7b-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="dbe7b-123">Header files</span></span>

<span data-ttu-id="dbe7b-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dbe7b-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="dbe7b-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="dbe7b-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="dbe7b-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dbe7b-126">Mapitags.h</span></span>
  
> <span data-ttu-id="dbe7b-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="dbe7b-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dbe7b-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dbe7b-128">See also</span></span>



[<span data-ttu-id="dbe7b-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dbe7b-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dbe7b-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dbe7b-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dbe7b-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="dbe7b-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dbe7b-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="dbe7b-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

