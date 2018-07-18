---
title: PidLidExceptionReplaceTime (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidExceptionReplaceTime
api_type:
- COM
ms.assetid: c3aae4f5-7f00-45bf-b007-370041ba360e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2292d53997fd4d54e9272789be83ea94a93c6a3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793537"
---
# <a name="pidlidexceptionreplacetime-canonical-property"></a><span data-ttu-id="5b541-103">PidLidExceptionReplaceTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5b541-103">PidLidExceptionReplaceTime Canonical Property</span></span>

  
  
<span data-ttu-id="5b541-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5b541-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5b541-105">Gibt das Datum und Uhrzeit in das Serienmuster, das die Ausnahme ersetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5b541-105">Specifies the date and time within the recurrence pattern that the exception will replace.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5b541-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5b541-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5b541-107">dispidExceptionReplaceTime</span><span class="sxs-lookup"><span data-stu-id="5b541-107">dispidExceptionReplaceTime</span></span>  <br/> |
|<span data-ttu-id="5b541-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="5b541-108">Property set:</span></span>  <br/> |<span data-ttu-id="5b541-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="5b541-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="5b541-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="5b541-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5b541-111">0x00008228</span><span class="sxs-lookup"><span data-stu-id="5b541-111">0x00008228</span></span>  <br/> |
|<span data-ttu-id="5b541-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5b541-112">Data type:</span></span>  <br/> |<span data-ttu-id="5b541-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="5b541-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="5b541-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5b541-114">Area:</span></span>  <br/> |<span data-ttu-id="5b541-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="5b541-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b541-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b541-116">Remarks</span></span>

<span data-ttu-id="5b541-117">Der Wert muss in koordinierter Weltzeit (UTC) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5b541-117">The value must be specified in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="5b541-118">Mit dieser Eigenschaft können das Ausnahme Attachment-Objekt für eine bestimmte Instanz gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="5b541-118">This property allows the exception attachment object to be found for a particular instance.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5b541-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5b541-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5b541-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5b541-120">Protocol specifications</span></span>

<span data-ttu-id="5b541-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b541-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b541-122">Enthält Eigenschaftendefinitionen an.</span><span class="sxs-lookup"><span data-stu-id="5b541-122">Provides property set definitions.</span></span>
    
<span data-ttu-id="5b541-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b541-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b541-124">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="5b541-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5b541-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="5b541-125">Header files</span></span>

<span data-ttu-id="5b541-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5b541-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="5b541-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5b541-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5b541-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b541-128">See also</span></span>



[<span data-ttu-id="5b541-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5b541-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5b541-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5b541-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5b541-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5b541-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5b541-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5b541-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

