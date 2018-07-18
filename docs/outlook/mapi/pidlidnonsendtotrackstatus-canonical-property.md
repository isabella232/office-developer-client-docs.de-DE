---
title: PidLidNonSendToTrackStatus (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendToTrackStatus
api_type:
- COM
ms.assetid: 50fec332-e7df-4bc6-8c50-59b9ca545f89
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 45d8512d48a1908d81e78b87c5975ab2da8c6c80
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793680"
---
# <a name="pidlidnonsendtotrackstatus-canonical-property"></a><span data-ttu-id="99afa-103">PidLidNonSendToTrackStatus (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="99afa-103">PidLidNonSendToTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="99afa-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="99afa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="99afa-105">Enthält den Wert für jeden Teilnehmer in der Eigenschaft **DispidNonSendableTo** ([PidLidNonSendableTo](pidlidnonsendableto-canonical-property.md)) aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="99afa-105">Contains the value for each attendee listed in the **dispidNonSendableTo** ([PidLidNonSendableTo](pidlidnonsendableto-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="99afa-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="99afa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="99afa-107">dispidNonSendToTrackStatus</span><span class="sxs-lookup"><span data-stu-id="99afa-107">dispidNonSendToTrackStatus</span></span>  <br/> |
|<span data-ttu-id="99afa-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="99afa-108">Property set:</span></span>  <br/> |<span data-ttu-id="99afa-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="99afa-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="99afa-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="99afa-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="99afa-111">0x00008543</span><span class="sxs-lookup"><span data-stu-id="99afa-111">0x00008543</span></span>  <br/> |
|<span data-ttu-id="99afa-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="99afa-112">Data type:</span></span>  <br/> |<span data-ttu-id="99afa-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="99afa-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="99afa-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="99afa-114">Area:</span></span>  <br/> |<span data-ttu-id="99afa-115">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="99afa-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99afa-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99afa-116">Remarks</span></span>

<span data-ttu-id="99afa-117">Diese Eigenschaft ist erforderlich, nur, wenn die **DispidNonSendableTo** -Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="99afa-117">This property is required only when the **dispidNonSendableTo** property is set.</span></span> <span data-ttu-id="99afa-118">Die Anzahl von Werten in dieser Eigenschaft muss die Anzahl von Werten in **DispidNonSendableTo**entsprechen.</span><span class="sxs-lookup"><span data-stu-id="99afa-118">The number of values in this property must equal the number of values in **dispidNonSendableTo**.</span></span> <span data-ttu-id="99afa-119">Jeder PT_LONG Wert in dieser Eigenschaft entspricht der Teilnehmer in der **DispidNonSendableTo** -Eigenschaft im selben Index.</span><span class="sxs-lookup"><span data-stu-id="99afa-119">Each PT_LONG value in this property corresponds to the attendee in the **dispidNonSendableTo** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="99afa-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="99afa-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="99afa-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="99afa-121">Protocol specifications</span></span>

<span data-ttu-id="99afa-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="99afa-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="99afa-123">Enthält Set Eigenschaftendefinition und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="99afa-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="99afa-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="99afa-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="99afa-125">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="99afa-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="99afa-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="99afa-126">Header files</span></span>

<span data-ttu-id="99afa-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="99afa-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="99afa-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="99afa-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="99afa-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99afa-129">See also</span></span>



[<span data-ttu-id="99afa-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="99afa-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="99afa-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="99afa-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="99afa-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="99afa-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="99afa-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="99afa-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

