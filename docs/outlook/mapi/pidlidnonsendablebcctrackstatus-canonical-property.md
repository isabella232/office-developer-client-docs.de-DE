---
title: PidLidNonSendableBccTrackStatus (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableBccTrackStatus
api_type:
- COM
ms.assetid: daad8735-a3da-4a0b-9329-6eb253c281fd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: de3c56e3ed532d8f4c3cff272049384e9c6a3867
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586088"
---
# <a name="pidlidnonsendablebcctrackstatus-canonical-property"></a><span data-ttu-id="648aa-103">PidLidNonSendableBccTrackStatus (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="648aa-103">PidLidNonSendableBccTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="648aa-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="648aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="648aa-105">Enthält den Wert für jeden Teilnehmer, die in der Eigenschaft **DispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)) aufgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="648aa-105">Contains the value for each attendee that is listed in the **dispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="648aa-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="648aa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="648aa-107">dispidNonSendBccTrackStatus</span><span class="sxs-lookup"><span data-stu-id="648aa-107">dispidNonSendBccTrackStatus</span></span>  <br/> |
|<span data-ttu-id="648aa-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="648aa-108">Property set:</span></span>  <br/> |<span data-ttu-id="648aa-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="648aa-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="648aa-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="648aa-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="648aa-111">0x00008545</span><span class="sxs-lookup"><span data-stu-id="648aa-111">0x00008545</span></span>  <br/> |
|<span data-ttu-id="648aa-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="648aa-112">Data type:</span></span>  <br/> |<span data-ttu-id="648aa-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="648aa-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="648aa-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="648aa-114">Area:</span></span>  <br/> |<span data-ttu-id="648aa-115">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="648aa-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="648aa-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="648aa-116">Remarks</span></span>

<span data-ttu-id="648aa-117">Diese Eigenschaft ist erforderlich, nur, wenn die **DispidNonSendableBCC** -Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="648aa-117">This property is required only when the **dispidNonSendableBCC** property is set.</span></span> <span data-ttu-id="648aa-118">Die Anzahl von Werten in dieser Eigenschaft muss die Anzahl von Werten in der **DispidNonSendableBCC**entsprechen.</span><span class="sxs-lookup"><span data-stu-id="648aa-118">The number of values in this property must equal the number of values in the **dispidNonSendableBCC**.</span></span> <span data-ttu-id="648aa-119">Jeder Wert in dieser Eigenschaft entspricht der Teilnehmer in der **DispidNonSendableBCC** -Eigenschaft im selben Index.</span><span class="sxs-lookup"><span data-stu-id="648aa-119">Each value in this property corresponds to the attendee in the **dispidNonSendableBCC** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="648aa-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="648aa-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="648aa-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="648aa-121">Protocol specifications</span></span>

<span data-ttu-id="648aa-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="648aa-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="648aa-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="648aa-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="648aa-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="648aa-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="648aa-125">Gibt die Eigenschaften und Vorgänge für den Termin, einer Besprechungsanfrage und Antwortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="648aa-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="648aa-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="648aa-126">Header files</span></span>

<span data-ttu-id="648aa-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="648aa-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="648aa-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="648aa-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="648aa-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="648aa-129">See also</span></span>



[<span data-ttu-id="648aa-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="648aa-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="648aa-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="648aa-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="648aa-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="648aa-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="648aa-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="648aa-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

