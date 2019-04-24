---
title: Kanonische Pidtagfreebusypublishend (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyPublishEnd
api_type:
- HeaderDef
ms.assetid: df239741-6a63-4cd4-9bbb-42c0f5c668a5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3b4a8cb7136eee914dc697d24e0374ccb4b6f8b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316184"
---
# <a name="pidtagfreebusypublishend-canonical-property"></a><span data-ttu-id="b9925-103">Kanonische Pidtagfreebusypublishend (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b9925-103">PidTagFreeBusyPublishEnd Canonical Property</span></span>

  
  
<span data-ttu-id="b9925-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9925-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9925-105">Enthält die Endzeit des Veröffentlichungszeitraums.</span><span class="sxs-lookup"><span data-stu-id="b9925-105">Contains the end time of the publishing range.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b9925-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b9925-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b9925-107">PR_FREEBUSY_PUBLISH_END</span><span class="sxs-lookup"><span data-stu-id="b9925-107">PR_FREEBUSY_PUBLISH_END</span></span>  <br/> |
|<span data-ttu-id="b9925-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="b9925-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b9925-109">0x6848</span><span class="sxs-lookup"><span data-stu-id="b9925-109">0x6848</span></span>  <br/> |
|<span data-ttu-id="b9925-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b9925-110">Data type:</span></span>  <br/> |<span data-ttu-id="b9925-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b9925-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b9925-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b9925-112">Area:</span></span>  <br/> |<span data-ttu-id="b9925-113">Frei/Gebucht</span><span class="sxs-lookup"><span data-stu-id="b9925-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9925-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9925-114">Remarks</span></span>

<span data-ttu-id="b9925-115">Der Wert für diese Eigenschaft wird berechnet, indem der Wert von **PR_FREEBUSY_COUNT_MONTHS** ([pidtagfreebusycountmonths (](pidtagfreebusycountmonths-canonical-property.md)) zum Startdatum des Veröffentlichungszeitraums hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="b9925-115">The value for this property is computed by adding the value of **PR_FREEBUSY_COUNT_MONTHS** ([PidTagFreeBusyCountMonths](pidtagfreebusycountmonths-canonical-property.md)) to the start date of the publishing range.</span></span> <span data-ttu-id="b9925-116">Dieser Wert wird als die Anzahl der Minuten seit Mitternacht, 1. Januar 1601 in koordinierter weltZeit (UTC) ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="b9925-116">This value is expressed as the number of minutes since midnight, January 1, 1601 in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b9925-117">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b9925-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b9925-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b9925-118">Protocol specifications</span></span>

<span data-ttu-id="b9925-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b9925-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b9925-120">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="b9925-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b9925-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b9925-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b9925-122">Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="b9925-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b9925-123">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="b9925-123">Header files</span></span>

<span data-ttu-id="b9925-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b9925-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="b9925-125">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="b9925-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="b9925-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="b9925-126">Mapitags.h</span></span>
  
> <span data-ttu-id="b9925-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b9925-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b9925-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9925-128">See also</span></span>



[<span data-ttu-id="b9925-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b9925-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b9925-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b9925-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b9925-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b9925-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b9925-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b9925-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

