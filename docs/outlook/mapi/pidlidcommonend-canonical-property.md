---
title: PidLidCommonEnd (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCommonEnd
api_type:
- COM
ms.assetid: c89f388a-1585-4bed-91b4-1b0c268292f3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fc3849ac972ce7e3efbfa981ff950ee3615cb533
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571465"
---
# <a name="pidlidcommonend-canonical-property"></a><span data-ttu-id="f7c5f-103">PidLidCommonEnd (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f7c5f-103">PidLidCommonEnd Canonical Property</span></span>

  
  
<span data-ttu-id="f7c5f-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7c5f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7c5f-105">Stellt das Enddatum und die Uhrzeit einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="f7c5f-105">Represents the end date and time of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f7c5f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f7c5f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f7c5f-107">dispidCommonEnd</span><span class="sxs-lookup"><span data-stu-id="f7c5f-107">dispidCommonEnd</span></span>  <br/> |
|<span data-ttu-id="f7c5f-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="f7c5f-108">Property set:</span></span>  <br/> |<span data-ttu-id="f7c5f-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="f7c5f-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="f7c5f-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="f7c5f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f7c5f-111">0x00008517</span><span class="sxs-lookup"><span data-stu-id="f7c5f-111">0x00008517</span></span>  <br/> |
|<span data-ttu-id="f7c5f-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f7c5f-112">Data type:</span></span>  <br/> |<span data-ttu-id="f7c5f-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="f7c5f-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="f7c5f-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f7c5f-114">Area:</span></span>  <br/> |<span data-ttu-id="f7c5f-115">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="f7c5f-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7c5f-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="f7c5f-116">Remarks</span></span>

<span data-ttu-id="f7c5f-117">Diese Eigenschaft gibt die Endzeit für ein Element an.</span><span class="sxs-lookup"><span data-stu-id="f7c5f-117">This property indicates the end time for an item.</span></span> <span data-ttu-id="f7c5f-118">Es muss größer als oder gleich dem Wert der Eigenschaft **DispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) sein.</span><span class="sxs-lookup"><span data-stu-id="f7c5f-118">It must be greater than or equal to the value of the **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="f7c5f-119">Dieser Wert muss die Entsprechung (Coordinated Universal Time, UTC) der **DispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f7c5f-119">This value must be the Coordinated Universal Time (UTC) equivalent of the **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f7c5f-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f7c5f-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f7c5f-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f7c5f-121">Protocol specifications</span></span>

<span data-ttu-id="f7c5f-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7c5f-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7c5f-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="f7c5f-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f7c5f-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7c5f-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7c5f-125">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="f7c5f-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="f7c5f-126">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7c5f-126">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7c5f-127">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="f7c5f-127">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f7c5f-128">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="f7c5f-128">Header files</span></span>

<span data-ttu-id="f7c5f-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f7c5f-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="f7c5f-130">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f7c5f-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f7c5f-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7c5f-131">See also</span></span>



[<span data-ttu-id="f7c5f-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f7c5f-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f7c5f-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f7c5f-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f7c5f-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f7c5f-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f7c5f-135">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f7c5f-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

