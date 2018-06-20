---
title: Kanonische PidTagRecipientProposedStartTime-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposedStartTime
api_type:
- COM
ms.assetid: 6687ff62-7ac6-409c-8c87-4e09d38e45f1
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 65d5c2f94da219fc1cb87384ebdd3c1cf34bd9a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794910"
---
# <a name="pidtagrecipientproposedstarttime-canonical-property"></a><span data-ttu-id="93595-103">Kanonische PidTagRecipientProposedStartTime-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="93595-103">PidTagRecipientProposedStartTime Canonical Property</span></span>

  
  
<span data-ttu-id="93595-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="93595-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="93595-105">Gibt eine vorgeschlagene Startzeit einer Besprechung an.</span><span class="sxs-lookup"><span data-stu-id="93595-105">Indicates a proposed starting time of a meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="93595-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="93595-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="93595-107">PR_RECIPIENT_PROPOSEDSTARTTIME</span><span class="sxs-lookup"><span data-stu-id="93595-107">PR_RECIPIENT_PROPOSEDSTARTTIME</span></span>  <br/> |
|<span data-ttu-id="93595-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="93595-108">Identifier:</span></span>  <br/> |<span data-ttu-id="93595-109">0x5FE3</span><span class="sxs-lookup"><span data-stu-id="93595-109">0x5FE3</span></span>  <br/> |
|<span data-ttu-id="93595-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="93595-110">Data type:</span></span>  <br/> |<span data-ttu-id="93595-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="93595-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="93595-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="93595-112">Area:</span></span>  <br/> |<span data-ttu-id="93595-113">Transport-Empfänger</span><span class="sxs-lookup"><span data-stu-id="93595-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93595-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="93595-114">Remarks</span></span>

<span data-ttu-id="93595-115">Wenn der Wert der **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md))-Eigenschaft auf TRUE festgelegt ist, gibt den Wert dieser Eigenschaft den Wert angefordert, indem die Teilnehmer als Wert des **DispidApptStartWhole** ([ festlegen PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md))-Eigenschaft für das Einzelinstanz Besprechung oder Exception-Objekt.</span><span class="sxs-lookup"><span data-stu-id="93595-115">When the value of the **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) property is set to TRUE, the value of this property indicates the value requested by the attendee to set as the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property for the single instance meeting object or exception object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="93595-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="93595-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="93595-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="93595-117">Protocol specifications</span></span>

<span data-ttu-id="93595-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93595-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93595-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="93595-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="93595-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93595-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93595-121">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="93595-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="93595-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="93595-122">Header files</span></span>

<span data-ttu-id="93595-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="93595-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="93595-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="93595-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="93595-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="93595-125">Mapitags.h</span></span>
  
> <span data-ttu-id="93595-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="93595-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="93595-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93595-127">See also</span></span>



[<span data-ttu-id="93595-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="93595-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="93595-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="93595-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="93595-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="93595-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="93595-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="93595-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

