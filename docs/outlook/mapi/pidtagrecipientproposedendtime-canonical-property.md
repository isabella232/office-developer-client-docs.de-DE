---
title: PidTagRecipientProposedEndTime (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposedEndTime
api_type:
- COM
ms.assetid: 08dc1f81-964b-4059-9167-e517391b26e9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f0310d8dcde9acc1e14f0be124543897e9867951
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794913"
---
# <a name="pidtagrecipientproposedendtime-canonical-property"></a><span data-ttu-id="aaf13-103">PidTagRecipientProposedEndTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="aaf13-103">PidTagRecipientProposedEndTime Canonical Property</span></span>

  
  
<span data-ttu-id="aaf13-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aaf13-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aaf13-105">Gibt eine vorgeschlagene Endzeit einer Besprechung an.</span><span class="sxs-lookup"><span data-stu-id="aaf13-105">Indicates a proposed end time of a meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aaf13-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="aaf13-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aaf13-107">PR_RECIPIENT_PROPOSEDENDTIME</span><span class="sxs-lookup"><span data-stu-id="aaf13-107">PR_RECIPIENT_PROPOSEDENDTIME</span></span>  <br/> |
|<span data-ttu-id="aaf13-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="aaf13-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aaf13-109">0x5FE4</span><span class="sxs-lookup"><span data-stu-id="aaf13-109">0x5FE4</span></span>  <br/> |
|<span data-ttu-id="aaf13-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="aaf13-110">Data type:</span></span>  <br/> |<span data-ttu-id="aaf13-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="aaf13-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="aaf13-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="aaf13-112">Area:</span></span>  <br/> |<span data-ttu-id="aaf13-113">Transport-Empfänger</span><span class="sxs-lookup"><span data-stu-id="aaf13-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aaf13-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aaf13-114">Remarks</span></span>

<span data-ttu-id="aaf13-115">Wenn der Wert der **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md))-Eigenschaft auf TRUE festgelegt ist, gibt den Wert dieser Eigenschaft den Wert angefordert, indem die Teilnehmer als Wert des **DispidApptEndWhole** ([ festlegen PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md))-Eigenschaft für das Einzelinstanz Besprechung oder Exception-Objekt.</span><span class="sxs-lookup"><span data-stu-id="aaf13-115">When the value of the **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) property is set to TRUE, the value of this property indicates the value requested by the attendee to set as the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property for the single instance meeting object or exception object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="aaf13-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="aaf13-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aaf13-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="aaf13-117">Protocol specifications</span></span>

<span data-ttu-id="aaf13-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aaf13-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aaf13-119">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="aaf13-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="aaf13-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aaf13-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aaf13-121">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="aaf13-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aaf13-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="aaf13-122">Header files</span></span>

<span data-ttu-id="aaf13-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aaf13-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="aaf13-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="aaf13-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="aaf13-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="aaf13-125">Mapitags.h</span></span>
  
> <span data-ttu-id="aaf13-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="aaf13-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aaf13-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aaf13-127">See also</span></span>



[<span data-ttu-id="aaf13-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aaf13-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aaf13-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aaf13-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aaf13-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="aaf13-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aaf13-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="aaf13-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

