---
title: PidLidOwnerCriticalChange (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidOwnerCriticalChange
api_type:
- COM
ms.assetid: b79aa2b7-b6e0-46dc-89f1-f801a6b5737a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: afc3c93e56c8beda9cb04c79164790b2246de983
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395770"
---
# <a name="pidlidownercriticalchange-canonical-property"></a><span data-ttu-id="10701-103">PidLidOwnerCriticalChange (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="10701-103">PidLidOwnerCriticalChange Canonical Property</span></span>

  
  
<span data-ttu-id="10701-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10701-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10701-105">Gibt das Datum und Uhrzeit, wann eine Besprechungsanfrage vom Organisator gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="10701-105">Specifies the date and time when a meeting request was sent by the organizer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="10701-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="10701-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="10701-107">LID_OWNER_CRITICAL_CHANGE</span><span class="sxs-lookup"><span data-stu-id="10701-107">LID_OWNER_CRITICAL_CHANGE</span></span>  <br/> |
|<span data-ttu-id="10701-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="10701-108">Property set:</span></span>  <br/> |<span data-ttu-id="10701-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="10701-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="10701-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="10701-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="10701-111">0x0000001a</span><span class="sxs-lookup"><span data-stu-id="10701-111">0x0000001A</span></span>  <br/> |
|<span data-ttu-id="10701-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="10701-112">Data type:</span></span>  <br/> |<span data-ttu-id="10701-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="10701-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="10701-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="10701-114">Area:</span></span>  <br/> |<span data-ttu-id="10701-115">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="10701-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10701-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="10701-116">Remarks</span></span>

<span data-ttu-id="10701-117">Der Wert muss in koordinierter Weltzeit (UTC) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="10701-117">The value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="10701-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="10701-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="10701-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="10701-119">Protocol specifications</span></span>

<span data-ttu-id="10701-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10701-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10701-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="10701-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="10701-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10701-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10701-123">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="10701-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="10701-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="10701-124">Header files</span></span>

<span data-ttu-id="10701-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="10701-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="10701-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="10701-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="10701-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10701-127">See also</span></span>



[<span data-ttu-id="10701-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="10701-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="10701-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="10701-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="10701-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="10701-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="10701-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="10701-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

