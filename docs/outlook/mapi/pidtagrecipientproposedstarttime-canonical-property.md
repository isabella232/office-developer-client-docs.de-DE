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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283142"
---
# <a name="pidtagrecipientproposedstarttime-canonical-property"></a><span data-ttu-id="48c14-103">PidTagRecipientProposedStartTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="48c14-103">PidTagRecipientProposedStartTime Canonical Property</span></span>

  
  
<span data-ttu-id="48c14-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48c14-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48c14-105">Gibt eine vorgeschlagene Startzeit einer Besprechung an.</span><span class="sxs-lookup"><span data-stu-id="48c14-105">Indicates a proposed starting time of a meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="48c14-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="48c14-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="48c14-107">PR_RECIPIENT_PROPOSEDSTARTTIME</span><span class="sxs-lookup"><span data-stu-id="48c14-107">PR_RECIPIENT_PROPOSEDSTARTTIME</span></span>  <br/> |
|<span data-ttu-id="48c14-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="48c14-108">Identifier:</span></span>  <br/> |<span data-ttu-id="48c14-109">0x5FE3</span><span class="sxs-lookup"><span data-stu-id="48c14-109">0x5FE3</span></span>  <br/> |
|<span data-ttu-id="48c14-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="48c14-110">Data type:</span></span>  <br/> |<span data-ttu-id="48c14-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="48c14-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="48c14-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="48c14-112">Area:</span></span>  <br/> |<span data-ttu-id="48c14-113">Transportempfänger</span><span class="sxs-lookup"><span data-stu-id="48c14-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48c14-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="48c14-114">Remarks</span></span>

<span data-ttu-id="48c14-115">Wenn der Wert der **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md))-Eigenschaft auf TRUE festgelegt ist, gibt der Wert dieser Eigenschaft den Vom Teilnehmer angeforderten Wert an, der als Wert der **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md))-Eigenschaft für das Besprechungsobjekt oder Ausnahmeobjekt der einzelnen Instanz festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="48c14-115">When the value of the **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) property is set to TRUE, the value of this property indicates the value requested by the attendee to set as the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property for the single instance meeting object or exception object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="48c14-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="48c14-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="48c14-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="48c14-117">Protocol specifications</span></span>

<span data-ttu-id="48c14-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48c14-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48c14-119">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="48c14-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="48c14-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48c14-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48c14-121">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="48c14-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="48c14-122">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="48c14-122">Header files</span></span>

<span data-ttu-id="48c14-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="48c14-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="48c14-124">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="48c14-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="48c14-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="48c14-125">Mapitags.h</span></span>
  
> <span data-ttu-id="48c14-126">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="48c14-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="48c14-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48c14-127">See also</span></span>



[<span data-ttu-id="48c14-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="48c14-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="48c14-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="48c14-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="48c14-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="48c14-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="48c14-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="48c14-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

