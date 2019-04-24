---
title: Kanonische Pidlidnonsendtotrackstatus (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendToTrackStatus
api_type:
- COM
ms.assetid: 50fec332-e7df-4bc6-8c50-59b9ca545f89
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: bdfbd553e130a4e463017168a76dc94fc0df827b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331367"
---
# <a name="pidlidnonsendtotrackstatus-canonical-property"></a><span data-ttu-id="dca1c-103">Kanonische Pidlidnonsendtotrackstatus (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="dca1c-103">PidLidNonSendToTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="dca1c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dca1c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dca1c-105">Enthält den Wert für jeden Teilnehmer, der in der **dispidNonSendableTo** ([pidlidnonsendableto (](pidlidnonsendableto-canonical-property.md))-Eigenschaft aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="dca1c-105">Contains the value for each attendee listed in the **dispidNonSendableTo** ([PidLidNonSendableTo](pidlidnonsendableto-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dca1c-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="dca1c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dca1c-107">dispidNonSendToTrackStatus</span><span class="sxs-lookup"><span data-stu-id="dca1c-107">dispidNonSendToTrackStatus</span></span>  <br/> |
|<span data-ttu-id="dca1c-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="dca1c-108">Property set:</span></span>  <br/> |<span data-ttu-id="dca1c-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="dca1c-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="dca1c-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="dca1c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="dca1c-111">0x00008543</span><span class="sxs-lookup"><span data-stu-id="dca1c-111">0x00008543</span></span>  <br/> |
|<span data-ttu-id="dca1c-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="dca1c-112">Data type:</span></span>  <br/> |<span data-ttu-id="dca1c-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="dca1c-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="dca1c-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="dca1c-114">Area:</span></span>  <br/> |<span data-ttu-id="dca1c-115">Allgemeine Nachrichtenübermittlung</span><span class="sxs-lookup"><span data-stu-id="dca1c-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dca1c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dca1c-116">Remarks</span></span>

<span data-ttu-id="dca1c-117">Diese Eigenschaft ist nur erforderlich, wenn die **dispidNonSendableTo** -Eigenschaft festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dca1c-117">This property is required only when the **dispidNonSendableTo** property is set.</span></span> <span data-ttu-id="dca1c-118">Die Anzahl der Werte in dieser Eigenschaft muss der Anzahl der Werte in **dispidNonSendableTo**entsprechen.</span><span class="sxs-lookup"><span data-stu-id="dca1c-118">The number of values in this property must equal the number of values in **dispidNonSendableTo**.</span></span> <span data-ttu-id="dca1c-119">Jeder PT_LONG-Wert in dieser Eigenschaft entspricht dem Teilnehmer in der **dispidNonSendableTo** -Eigenschaft am gleichen Index.</span><span class="sxs-lookup"><span data-stu-id="dca1c-119">Each PT_LONG value in this property corresponds to the attendee in the **dispidNonSendableTo** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="dca1c-120">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="dca1c-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dca1c-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="dca1c-121">Protocol specifications</span></span>

<span data-ttu-id="dca1c-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dca1c-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dca1c-123">Stellt die Eigenschaftensatz Definition und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="dca1c-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dca1c-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dca1c-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dca1c-125">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="dca1c-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dca1c-126">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="dca1c-126">Header files</span></span>

<span data-ttu-id="dca1c-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="dca1c-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="dca1c-128">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="dca1c-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dca1c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dca1c-129">See also</span></span>



[<span data-ttu-id="dca1c-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dca1c-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dca1c-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dca1c-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dca1c-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="dca1c-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dca1c-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="dca1c-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

