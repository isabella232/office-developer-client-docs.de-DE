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
ms.openlocfilehash: 678fd982505cc2bc910af9ef131f852a7f0c919a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391080"
---
# <a name="pidtagscheduleinfodisallowrecurringappts-canonical-property"></a><span data-ttu-id="9c064-103">PidTagScheduleInfoDisallowRecurringAppts (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9c064-103">PidTagScheduleInfoDisallowRecurringAppts Canonical Property</span></span>

  
  
<span data-ttu-id="9c064-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c064-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c064-105">Enthält True, wenn die automatische Antwort auf wiederkehrender Termine ablehnen ist.</span><span class="sxs-lookup"><span data-stu-id="9c064-105">Contains TRUE when the automatic response to recurring appointments is decline.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9c064-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9c064-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9c064-107">PR_SCHDINFO_DISALLOW_RECURRING_APPTS</span><span class="sxs-lookup"><span data-stu-id="9c064-107">PR_SCHDINFO_DISALLOW_RECURRING_APPTS</span></span>  <br/> |
|<span data-ttu-id="9c064-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="9c064-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9c064-109">0x686E</span><span class="sxs-lookup"><span data-stu-id="9c064-109">0x686E</span></span>  <br/> |
|<span data-ttu-id="9c064-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9c064-110">Data type:</span></span>  <br/> |<span data-ttu-id="9c064-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="9c064-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="9c064-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9c064-112">Area:</span></span>  <br/> |<span data-ttu-id="9c064-113">Frei/Gebucht-Informationen</span><span class="sxs-lookup"><span data-stu-id="9c064-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9c064-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9c064-114">Remarks</span></span>

<span data-ttu-id="9c064-115">Diese Eigenschaft ist nur sinnvoll, wenn der Wert der **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md))-Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9c064-115">This property is only meaningful when the value of the **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="9c064-116">Das fehlen diese Eigenschaft gibt an, dass Besprechungsserien akzeptiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="9c064-116">The absence of this property indicates that recurring meetings must be accepted.</span></span> <span data-ttu-id="9c064-117">Dies ist keine erforderliche Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="9c064-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9c064-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9c064-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9c064-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="9c064-119">Protocol specifications</span></span>

<span data-ttu-id="9c064-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9c064-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9c064-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="9c064-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9c064-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9c064-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9c064-123">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="9c064-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="9c064-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9c064-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9c064-125">Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="9c064-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9c064-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="9c064-126">Header files</span></span>

<span data-ttu-id="9c064-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9c064-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="9c064-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="9c064-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="9c064-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9c064-129">Mapitags.h</span></span>
  
> <span data-ttu-id="9c064-130">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9c064-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9c064-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c064-131">See also</span></span>



[<span data-ttu-id="9c064-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9c064-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9c064-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9c064-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9c064-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9c064-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9c064-135">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9c064-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

