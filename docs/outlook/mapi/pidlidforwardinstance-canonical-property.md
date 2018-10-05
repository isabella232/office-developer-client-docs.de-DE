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
ms.openlocfilehash: 585e1a5400965288aa4a4c321888a570270021c8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394776"
---
# <a name="pidlidforwardinstance-canonical-property"></a><span data-ttu-id="64c32-103">PidLidForwardInstance (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="64c32-103">PidLidForwardInstance Canonical Property</span></span>

  
  
<span data-ttu-id="64c32-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64c32-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64c32-105">Gibt an, dass die Besprechungsanfrage eine Ausnahme in einer Terminserie stellt, und er (selbst wenn Sie vom Organisator weitergeleitet) weitergeleitet wurde, statt eine Einladung vom Organisator gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="64c32-105">Indicates that the meeting request represents an exception to a recurring series, and it was forwarded (even when forwarded by the organizer) rather than being an invitation sent by the organizer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="64c32-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="64c32-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="64c32-107">dispidFwrdInstance</span><span class="sxs-lookup"><span data-stu-id="64c32-107">dispidFwrdInstance</span></span>  <br/> |
|<span data-ttu-id="64c32-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="64c32-108">Property set:</span></span>  <br/> |<span data-ttu-id="64c32-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="64c32-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="64c32-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="64c32-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="64c32-111">0x0000820A</span><span class="sxs-lookup"><span data-stu-id="64c32-111">0x0000820A</span></span>  <br/> |
|<span data-ttu-id="64c32-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="64c32-112">Data type:</span></span>  <br/> |<span data-ttu-id="64c32-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="64c32-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="64c32-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="64c32-114">Area:</span></span>  <br/> |<span data-ttu-id="64c32-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="64c32-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64c32-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="64c32-116">Remarks</span></span>

<span data-ttu-id="64c32-117">Der Wert für diese Eigenschaft FALSE gibt an, dass die Besprechungsanfrage keine weitergeleitete Instanz ist.</span><span class="sxs-lookup"><span data-stu-id="64c32-117">A value of FALSE for this property indicates that the meeting request is not a forwarded instance.</span></span> <span data-ttu-id="64c32-118">Diese Eigenschaft ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="64c32-118">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="64c32-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="64c32-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="64c32-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="64c32-120">Protocol specifications</span></span>

<span data-ttu-id="64c32-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64c32-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64c32-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="64c32-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="64c32-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64c32-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64c32-124">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="64c32-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="64c32-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="64c32-125">Header files</span></span>

<span data-ttu-id="64c32-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="64c32-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="64c32-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="64c32-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="64c32-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64c32-128">See also</span></span>



[<span data-ttu-id="64c32-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="64c32-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="64c32-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="64c32-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="64c32-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="64c32-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="64c32-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="64c32-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

