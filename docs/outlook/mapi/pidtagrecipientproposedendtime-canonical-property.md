---
title: Kanonische Pidtagrecipientproposedendtime (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6ea6d634b0e69cf6895c076815941754ba5e83a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332774"
---
# <a name="pidtagrecipientproposedendtime-canonical-property"></a><span data-ttu-id="8b573-103">Kanonische Pidtagrecipientproposedendtime (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8b573-103">PidTagRecipientProposedEndTime Canonical Property</span></span>

  
  
<span data-ttu-id="8b573-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b573-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b573-105">Gibt eine vorgeschlagene Endzeit einer Besprechung an.</span><span class="sxs-lookup"><span data-stu-id="8b573-105">Indicates a proposed end time of a meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8b573-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8b573-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8b573-107">PR_RECIPIENT_PROPOSEDENDTIME</span><span class="sxs-lookup"><span data-stu-id="8b573-107">PR_RECIPIENT_PROPOSEDENDTIME</span></span>  <br/> |
|<span data-ttu-id="8b573-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="8b573-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8b573-109">0x5FE4</span><span class="sxs-lookup"><span data-stu-id="8b573-109">0x5FE4</span></span>  <br/> |
|<span data-ttu-id="8b573-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8b573-110">Data type:</span></span>  <br/> |<span data-ttu-id="8b573-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="8b573-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="8b573-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8b573-112">Area:</span></span>  <br/> |<span data-ttu-id="8b573-113">Transport Empfänger</span><span class="sxs-lookup"><span data-stu-id="8b573-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b573-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b573-114">Remarks</span></span>

<span data-ttu-id="8b573-115">Wenn der Wert der **PR_RECIPIENT_PROPOSED** ([pidtagrecipientproposed (](pidtagrecipientproposed-canonical-property.md))-Eigenschaft auf true festgelegt ist, gibt der Wert dieser Eigenschaft den Wert an, der vom Teilnehmer angefordert wird, um den Wert des **dispidApptEndWhole** festzulegen ([ Pidlidappointmentendwhole (](pidlidappointmentendwhole-canonical-property.md))-Eigenschaft für das Besprechungsobjekt oder Exception-Objekt einer einzelnen Instanz.</span><span class="sxs-lookup"><span data-stu-id="8b573-115">When the value of the **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) property is set to TRUE, the value of this property indicates the value requested by the attendee to set as the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property for the single instance meeting object or exception object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8b573-116">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8b573-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8b573-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="8b573-117">Protocol specifications</span></span>

<span data-ttu-id="8b573-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b573-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b573-119">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="8b573-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8b573-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b573-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b573-121">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="8b573-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8b573-122">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="8b573-122">Header files</span></span>

<span data-ttu-id="8b573-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8b573-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="8b573-124">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="8b573-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="8b573-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="8b573-125">Mapitags.h</span></span>
  
> <span data-ttu-id="8b573-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="8b573-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8b573-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b573-127">See also</span></span>



[<span data-ttu-id="8b573-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b573-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8b573-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b573-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8b573-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8b573-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8b573-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8b573-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

