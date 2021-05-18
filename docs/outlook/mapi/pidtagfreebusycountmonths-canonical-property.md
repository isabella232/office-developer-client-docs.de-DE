---
title: PidTagFreeBusyCountMonths (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyCountMonths
api_type:
- HeaderDef
ms.assetid: 278a77f2-65ec-4281-b406-942cc416a476
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 610e9d396442f981b7bcbf126e3086e6885399d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316191"
---
# <a name="pidtagfreebusycountmonths-canonical-property"></a><span data-ttu-id="08136-103">PidTagFreeBusyCountMonths (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="08136-103">PidTagFreeBusyCountMonths Canonical Property</span></span>

  
  
<span data-ttu-id="08136-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08136-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08136-105">Enthält den Wert für die Berechnung der Start- und Endtermine des Bereichs von Frei/Gebucht-Daten, die in öffentlichen Ordnern veröffentlicht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="08136-105">Contains the value for calculating the start and end dates of the range of free/busy data to be published to public folders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="08136-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="08136-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="08136-107">PR_FREEBUSY_COUNT_MONTHS</span><span class="sxs-lookup"><span data-stu-id="08136-107">PR_FREEBUSY_COUNT_MONTHS</span></span>  <br/> |
|<span data-ttu-id="08136-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="08136-108">Identifier:</span></span>  <br/> |<span data-ttu-id="08136-109">0x6869</span><span class="sxs-lookup"><span data-stu-id="08136-109">0x6869</span></span>  <br/> |
|<span data-ttu-id="08136-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="08136-110">Data type:</span></span>  <br/> |<span data-ttu-id="08136-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="08136-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="08136-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="08136-112">Area:</span></span>  <br/> |<span data-ttu-id="08136-113">Durch nachrichtenklassendefinierte übertragungsfähige Nachrichten</span><span class="sxs-lookup"><span data-stu-id="08136-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08136-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="08136-114">Remarks</span></span>

<span data-ttu-id="08136-115">Der Wert dieser Eigenschaft muss größer oder gleich 0 und kleiner als oder gleich 36 sein.</span><span class="sxs-lookup"><span data-stu-id="08136-115">This property's value must be greater than or equal to 0 and less than or equal to 36.</span></span> <span data-ttu-id="08136-116">Dies ist keine erforderliche Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="08136-116">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="08136-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="08136-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="08136-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="08136-118">Protocol specifications</span></span>

<span data-ttu-id="08136-119">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08136-119">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08136-120">Veröffentlicht die Verfügbarkeit eines Benutzers oder einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="08136-120">Publishes the availability of a user or resource.</span></span>
    
<span data-ttu-id="08136-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08136-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08136-122">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="08136-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="08136-123">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="08136-123">Header files</span></span>

<span data-ttu-id="08136-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="08136-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="08136-125">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="08136-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="08136-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="08136-126">Mapitags.h</span></span>
  
> <span data-ttu-id="08136-127">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="08136-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08136-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08136-128">See also</span></span>



[<span data-ttu-id="08136-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08136-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="08136-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="08136-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="08136-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="08136-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="08136-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="08136-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

