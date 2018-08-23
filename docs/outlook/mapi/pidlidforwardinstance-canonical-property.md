---
title: PidLidForwardInstance (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidForwardInstance
api_type:
- COM
ms.assetid: 055bdcaf-5002-44a6-b2b6-87244b2bea93
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 47dd6f10d1dbd25ea275ea96a2eddb6e9c6dfacb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571773"
---
# <a name="pidlidforwardinstance-canonical-property"></a><span data-ttu-id="1d051-103">PidLidForwardInstance (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1d051-103">PidLidForwardInstance Canonical Property</span></span>

  
  
<span data-ttu-id="1d051-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d051-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d051-105">Gibt an, dass die Besprechungsanfrage eine Ausnahme in einer Terminserie stellt, und er (selbst wenn Sie vom Organisator weitergeleitet) weitergeleitet wurde, statt eine Einladung vom Organisator gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="1d051-105">Indicates that the meeting request represents an exception to a recurring series, and it was forwarded (even when forwarded by the organizer) rather than being an invitation sent by the organizer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1d051-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1d051-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1d051-107">dispidFwrdInstance</span><span class="sxs-lookup"><span data-stu-id="1d051-107">dispidFwrdInstance</span></span>  <br/> |
|<span data-ttu-id="1d051-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="1d051-108">Property set:</span></span>  <br/> |<span data-ttu-id="1d051-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="1d051-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="1d051-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="1d051-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1d051-111">0x0000820A</span><span class="sxs-lookup"><span data-stu-id="1d051-111">0x0000820A</span></span>  <br/> |
|<span data-ttu-id="1d051-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1d051-112">Data type:</span></span>  <br/> |<span data-ttu-id="1d051-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="1d051-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="1d051-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1d051-114">Area:</span></span>  <br/> |<span data-ttu-id="1d051-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="1d051-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1d051-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="1d051-116">Remarks</span></span>

<span data-ttu-id="1d051-117">Der Wert für diese Eigenschaft FALSE gibt an, dass die Besprechungsanfrage keine weitergeleitete Instanz ist.</span><span class="sxs-lookup"><span data-stu-id="1d051-117">A value of FALSE for this property indicates that the meeting request is not a forwarded instance.</span></span> <span data-ttu-id="1d051-118">Diese Eigenschaft ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1d051-118">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1d051-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1d051-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1d051-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="1d051-120">Protocol specifications</span></span>

<span data-ttu-id="1d051-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1d051-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1d051-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="1d051-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1d051-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1d051-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1d051-124">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="1d051-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1d051-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="1d051-125">Header files</span></span>

<span data-ttu-id="1d051-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1d051-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="1d051-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1d051-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1d051-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d051-128">See also</span></span>



[<span data-ttu-id="1d051-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1d051-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1d051-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1d051-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1d051-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1d051-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1d051-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1d051-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

