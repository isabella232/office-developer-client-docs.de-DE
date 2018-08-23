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
ms.openlocfilehash: 1ee68f0f60f96798130115cbd313f6d7cd403486
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590498"
---
# <a name="pidlidnonsendcctrackstatus-canonical-property"></a><span data-ttu-id="0a5d2-103">PidLidNonSendCcTrackStatus (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0a5d2-103">PidLidNonSendCcTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="0a5d2-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a5d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a5d2-105">Enthält den Wert für jeden Teilnehmer in der Eigenschaft **DispidNonSendableCC** ([PidLidNonSendableCc](pidlidnonsendablecc-canonical-property.md)) aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="0a5d2-105">Contains the value for each attendee listed in the **dispidNonSendableCC** ([PidLidNonSendableCc](pidlidnonsendablecc-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0a5d2-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0a5d2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0a5d2-107">dispidNonSendCcTrackStatus</span><span class="sxs-lookup"><span data-stu-id="0a5d2-107">dispidNonSendCcTrackStatus</span></span>  <br/> |
|<span data-ttu-id="0a5d2-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="0a5d2-108">Property set:</span></span>  <br/> |<span data-ttu-id="0a5d2-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="0a5d2-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="0a5d2-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="0a5d2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0a5d2-111">0x00008544</span><span class="sxs-lookup"><span data-stu-id="0a5d2-111">0x00008544</span></span>  <br/> |
|<span data-ttu-id="0a5d2-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0a5d2-112">Data type:</span></span>  <br/> |<span data-ttu-id="0a5d2-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="0a5d2-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="0a5d2-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0a5d2-114">Area:</span></span>  <br/> |<span data-ttu-id="0a5d2-115">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="0a5d2-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a5d2-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="0a5d2-116">Remarks</span></span>

<span data-ttu-id="0a5d2-117">Diese Eigenschaft ist erforderlich, nur, wenn die **DispidNonSendableCC** -Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="0a5d2-117">This property is required only when the **dispidNonSendableCC** property is set.</span></span> <span data-ttu-id="0a5d2-118">Die Anzahl von Werten in dieser Eigenschaft muss die Anzahl von Werten in **DispidNonSendableCC**entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0a5d2-118">The number of values in this property must equal the number of values in **dispidNonSendableCC**.</span></span> <span data-ttu-id="0a5d2-119">Jeder PT_LONG Wert in dieser Eigenschaft entspricht der Teilnehmer in der **DispidNonSendableCC** -Eigenschaft im selben Index.</span><span class="sxs-lookup"><span data-stu-id="0a5d2-119">Each PT_LONG value in this property corresponds to the attendee in the **dispidNonSendableCC** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0a5d2-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0a5d2-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0a5d2-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0a5d2-121">Protocol specifications</span></span>

<span data-ttu-id="0a5d2-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0a5d2-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0a5d2-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="0a5d2-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0a5d2-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0a5d2-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0a5d2-125">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="0a5d2-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0a5d2-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="0a5d2-126">Header files</span></span>

<span data-ttu-id="0a5d2-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0a5d2-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="0a5d2-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0a5d2-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0a5d2-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a5d2-129">See also</span></span>



[<span data-ttu-id="0a5d2-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0a5d2-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0a5d2-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0a5d2-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0a5d2-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0a5d2-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0a5d2-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0a5d2-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

