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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b364fb91bda7e895b546f9a281ef14ce33b073f9
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396827"
---
# <a name="pidlidexceptionreplacetime-canonical-property"></a><span data-ttu-id="fea02-103">PidLidExceptionReplaceTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fea02-103">PidLidExceptionReplaceTime Canonical Property</span></span>

  
  
<span data-ttu-id="fea02-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fea02-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fea02-105">Gibt das Datum und Uhrzeit in das Serienmuster, das die Ausnahme ersetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fea02-105">Specifies the date and time within the recurrence pattern that the exception will replace.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fea02-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="fea02-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fea02-107">dispidExceptionReplaceTime</span><span class="sxs-lookup"><span data-stu-id="fea02-107">dispidExceptionReplaceTime</span></span>  <br/> |
|<span data-ttu-id="fea02-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="fea02-108">Property set:</span></span>  <br/> |<span data-ttu-id="fea02-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="fea02-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="fea02-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="fea02-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fea02-111">0x00008228</span><span class="sxs-lookup"><span data-stu-id="fea02-111">0x00008228</span></span>  <br/> |
|<span data-ttu-id="fea02-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="fea02-112">Data type:</span></span>  <br/> |<span data-ttu-id="fea02-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="fea02-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="fea02-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="fea02-114">Area:</span></span>  <br/> |<span data-ttu-id="fea02-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="fea02-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fea02-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fea02-116">Remarks</span></span>

<span data-ttu-id="fea02-117">Der Wert muss in koordinierter Weltzeit (UTC) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fea02-117">The value must be specified in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="fea02-118">Mit dieser Eigenschaft können das Ausnahme Attachment-Objekt für eine bestimmte Instanz gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="fea02-118">This property allows the exception attachment object to be found for a particular instance.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fea02-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fea02-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fea02-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="fea02-120">Protocol specifications</span></span>

<span data-ttu-id="fea02-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fea02-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fea02-122">Enthält Eigenschaftendefinitionen an.</span><span class="sxs-lookup"><span data-stu-id="fea02-122">Provides property set definitions.</span></span>
    
<span data-ttu-id="fea02-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fea02-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fea02-124">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="fea02-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fea02-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="fea02-125">Header files</span></span>

<span data-ttu-id="fea02-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fea02-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="fea02-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="fea02-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fea02-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fea02-128">See also</span></span>



[<span data-ttu-id="fea02-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fea02-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fea02-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fea02-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fea02-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="fea02-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fea02-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="fea02-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

