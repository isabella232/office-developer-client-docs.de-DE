---
title: PidTagRecipientProposedStartTime (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8815728adce809641586c4da5beb4c9fad735507
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397114"
---
# <a name="pidtagrecipientproposedstarttime-canonical-property"></a><span data-ttu-id="2fc4e-103">PidTagRecipientProposedStartTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2fc4e-103">PidTagRecipientProposedStartTime Canonical Property</span></span>

  
  
<span data-ttu-id="2fc4e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2fc4e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2fc4e-105">Gibt eine vorgeschlagene Startzeit einer Besprechung an.</span><span class="sxs-lookup"><span data-stu-id="2fc4e-105">Indicates a proposed starting time of a meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2fc4e-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2fc4e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2fc4e-107">PR_RECIPIENT_PROPOSEDSTARTTIME</span><span class="sxs-lookup"><span data-stu-id="2fc4e-107">PR_RECIPIENT_PROPOSEDSTARTTIME</span></span>  <br/> |
|<span data-ttu-id="2fc4e-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="2fc4e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2fc4e-109">0x5FE3</span><span class="sxs-lookup"><span data-stu-id="2fc4e-109">0x5FE3</span></span>  <br/> |
|<span data-ttu-id="2fc4e-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="2fc4e-110">Data type:</span></span>  <br/> |<span data-ttu-id="2fc4e-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="2fc4e-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="2fc4e-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2fc4e-112">Area:</span></span>  <br/> |<span data-ttu-id="2fc4e-113">Transport-Empfänger</span><span class="sxs-lookup"><span data-stu-id="2fc4e-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2fc4e-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2fc4e-114">Remarks</span></span>

<span data-ttu-id="2fc4e-115">Wenn der Wert der **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md))-Eigenschaft auf TRUE festgelegt ist, gibt den Wert dieser Eigenschaft den Wert angefordert, indem die Teilnehmer als Wert des **DispidApptStartWhole** ([ festlegen PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md))-Eigenschaft für das Einzelinstanz Besprechung oder Exception-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2fc4e-115">When the value of the **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) property is set to TRUE, the value of this property indicates the value requested by the attendee to set as the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property for the single instance meeting object or exception object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2fc4e-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2fc4e-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2fc4e-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="2fc4e-117">Protocol specifications</span></span>

<span data-ttu-id="2fc4e-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2fc4e-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2fc4e-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="2fc4e-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2fc4e-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2fc4e-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2fc4e-121">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="2fc4e-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2fc4e-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="2fc4e-122">Header files</span></span>

<span data-ttu-id="2fc4e-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2fc4e-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="2fc4e-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="2fc4e-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="2fc4e-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2fc4e-125">Mapitags.h</span></span>
  
> <span data-ttu-id="2fc4e-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2fc4e-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2fc4e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2fc4e-127">See also</span></span>



[<span data-ttu-id="2fc4e-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2fc4e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2fc4e-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2fc4e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2fc4e-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2fc4e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2fc4e-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2fc4e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

