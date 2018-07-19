---
title: PidTagScheduleInfoDisallowRecurringAppts (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDisallowRecurringAppts
api_type:
- COM
ms.assetid: 61e082dd-f5bc-479b-990a-c9c0360f883e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f5f3feb5b3186f8d0239558aa410c7f71bdf54f8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795084"
---
# <a name="pidtagscheduleinfodisallowrecurringappts-canonical-property"></a><span data-ttu-id="9acbf-103">PidTagScheduleInfoDisallowRecurringAppts (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9acbf-103">PidTagScheduleInfoDisallowRecurringAppts Canonical Property</span></span>

  
  
<span data-ttu-id="9acbf-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9acbf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9acbf-105">Enthält True, wenn die automatische Antwort auf wiederkehrender Termine ablehnen ist.</span><span class="sxs-lookup"><span data-stu-id="9acbf-105">Contains TRUE when the automatic response to recurring appointments is decline.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9acbf-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9acbf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9acbf-107">PR_SCHDINFO_DISALLOW_RECURRING_APPTS</span><span class="sxs-lookup"><span data-stu-id="9acbf-107">PR_SCHDINFO_DISALLOW_RECURRING_APPTS</span></span>  <br/> |
|<span data-ttu-id="9acbf-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="9acbf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9acbf-109">0x686E</span><span class="sxs-lookup"><span data-stu-id="9acbf-109">0x686E</span></span>  <br/> |
|<span data-ttu-id="9acbf-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9acbf-110">Data type:</span></span>  <br/> |<span data-ttu-id="9acbf-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="9acbf-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="9acbf-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9acbf-112">Area:</span></span>  <br/> |<span data-ttu-id="9acbf-113">Frei/Gebucht-Informationen</span><span class="sxs-lookup"><span data-stu-id="9acbf-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9acbf-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9acbf-114">Remarks</span></span>

<span data-ttu-id="9acbf-115">Diese Eigenschaft ist nur sinnvoll, wenn der Wert der **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md))-Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9acbf-115">This property is only meaningful when the value of the **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="9acbf-116">Das fehlen diese Eigenschaft gibt an, dass Besprechungsserien akzeptiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="9acbf-116">The absence of this property indicates that recurring meetings must be accepted.</span></span> <span data-ttu-id="9acbf-117">Dies ist keine erforderliche Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="9acbf-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9acbf-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9acbf-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9acbf-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="9acbf-119">Protocol specifications</span></span>

<span data-ttu-id="9acbf-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9acbf-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9acbf-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="9acbf-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9acbf-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9acbf-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9acbf-123">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="9acbf-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="9acbf-124">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9acbf-124">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9acbf-125">Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="9acbf-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9acbf-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="9acbf-126">Header files</span></span>

<span data-ttu-id="9acbf-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9acbf-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="9acbf-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9acbf-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="9acbf-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9acbf-129">Mapitags.h</span></span>
  
> <span data-ttu-id="9acbf-130">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9acbf-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9acbf-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9acbf-131">See also</span></span>



[<span data-ttu-id="9acbf-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9acbf-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9acbf-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9acbf-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9acbf-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9acbf-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9acbf-135">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9acbf-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

