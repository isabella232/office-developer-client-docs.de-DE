---
title: PidLidNonSendCcTrackStatus (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendCcTrackStatus
api_type:
- COM
ms.assetid: e2654fad-444b-45bc-976d-3c5cbbc81b84
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 10b6009bc86df4232c995e7c6bca463f45999528
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319670"
---
# <a name="pidlidnonsendcctrackstatus-canonical-property"></a><span data-ttu-id="06bfc-103">PidLidNonSendCcTrackStatus (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="06bfc-103">PidLidNonSendCcTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="06bfc-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06bfc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06bfc-105">Enthält den Wert für jeden Teilnehmer, der in der **eigenschaft dispidNonSendableCC** ([PidLidNonSendableCc](pidlidnonsendablecc-canonical-property.md)) aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="06bfc-105">Contains the value for each attendee listed in the **dispidNonSendableCC** ([PidLidNonSendableCc](pidlidnonsendablecc-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="06bfc-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="06bfc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="06bfc-107">dispidNonSendCcTrackStatus</span><span class="sxs-lookup"><span data-stu-id="06bfc-107">dispidNonSendCcTrackStatus</span></span>  <br/> |
|<span data-ttu-id="06bfc-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="06bfc-108">Property set:</span></span>  <br/> |<span data-ttu-id="06bfc-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="06bfc-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="06bfc-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="06bfc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="06bfc-111">0x00008544</span><span class="sxs-lookup"><span data-stu-id="06bfc-111">0x00008544</span></span>  <br/> |
|<span data-ttu-id="06bfc-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="06bfc-112">Data type:</span></span>  <br/> |<span data-ttu-id="06bfc-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="06bfc-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="06bfc-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="06bfc-114">Area:</span></span>  <br/> |<span data-ttu-id="06bfc-115">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="06bfc-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06bfc-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="06bfc-116">Remarks</span></span>

<span data-ttu-id="06bfc-117">Diese Eigenschaft ist nur erforderlich, wenn **die dispidNonSendableCC-Eigenschaft** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="06bfc-117">This property is required only when the **dispidNonSendableCC** property is set.</span></span> <span data-ttu-id="06bfc-118">Die Anzahl der Werte in dieser Eigenschaft muss der Anzahl der Werte in **dispidNonSendableCC entspricht.**</span><span class="sxs-lookup"><span data-stu-id="06bfc-118">The number of values in this property must equal the number of values in **dispidNonSendableCC**.</span></span> <span data-ttu-id="06bfc-119">Jeder PT_LONG in dieser Eigenschaft entspricht dem Teilnehmer in der **dispidNonSendableCC-Eigenschaft** am gleichen Index.</span><span class="sxs-lookup"><span data-stu-id="06bfc-119">Each PT_LONG value in this property corresponds to the attendee in the **dispidNonSendableCC** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="06bfc-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="06bfc-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="06bfc-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="06bfc-121">Protocol specifications</span></span>

<span data-ttu-id="06bfc-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06bfc-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06bfc-123">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="06bfc-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="06bfc-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06bfc-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06bfc-125">Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.</span><span class="sxs-lookup"><span data-stu-id="06bfc-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="06bfc-126">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="06bfc-126">Header files</span></span>

<span data-ttu-id="06bfc-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="06bfc-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="06bfc-128">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="06bfc-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="06bfc-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06bfc-129">See also</span></span>



[<span data-ttu-id="06bfc-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="06bfc-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="06bfc-131">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="06bfc-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="06bfc-132">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="06bfc-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="06bfc-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="06bfc-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

