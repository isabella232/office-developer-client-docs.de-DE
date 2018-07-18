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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4aaa8f1c0bb2d9eb43cd1850ea2148151a0f02fa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793470"
---
# <a name="pidlidcommonend-canonical-property"></a><span data-ttu-id="18b8d-103">PidLidCommonEnd (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="18b8d-103">PidLidCommonEnd Canonical Property</span></span>

  
  
<span data-ttu-id="18b8d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="18b8d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="18b8d-105">Stellt das Enddatum und die Uhrzeit einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="18b8d-105">Represents the end date and time of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="18b8d-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="18b8d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="18b8d-107">dispidCommonEnd</span><span class="sxs-lookup"><span data-stu-id="18b8d-107">dispidCommonEnd</span></span>  <br/> |
|<span data-ttu-id="18b8d-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="18b8d-108">Property set:</span></span>  <br/> |<span data-ttu-id="18b8d-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="18b8d-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="18b8d-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="18b8d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="18b8d-111">0x00008517</span><span class="sxs-lookup"><span data-stu-id="18b8d-111">0x00008517</span></span>  <br/> |
|<span data-ttu-id="18b8d-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="18b8d-112">Data type:</span></span>  <br/> |<span data-ttu-id="18b8d-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="18b8d-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="18b8d-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="18b8d-114">Area:</span></span>  <br/> |<span data-ttu-id="18b8d-115">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="18b8d-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18b8d-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18b8d-116">Remarks</span></span>

<span data-ttu-id="18b8d-117">Diese Eigenschaft gibt die Endzeit für ein Element an.</span><span class="sxs-lookup"><span data-stu-id="18b8d-117">This property indicates the end time for an item.</span></span> <span data-ttu-id="18b8d-118">Es muss größer als oder gleich dem Wert der Eigenschaft **DispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) sein.</span><span class="sxs-lookup"><span data-stu-id="18b8d-118">It must be greater than or equal to the value of the **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="18b8d-119">Dieser Wert muss die Entsprechung (Coordinated Universal Time, UTC) der **DispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="18b8d-119">This value must be the Coordinated Universal Time (UTC) equivalent of the **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="18b8d-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="18b8d-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="18b8d-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="18b8d-121">Protocol specifications</span></span>

<span data-ttu-id="18b8d-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18b8d-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18b8d-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="18b8d-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="18b8d-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18b8d-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18b8d-125">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="18b8d-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="18b8d-126">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18b8d-126">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18b8d-127">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="18b8d-127">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="18b8d-128">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="18b8d-128">Header files</span></span>

<span data-ttu-id="18b8d-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="18b8d-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="18b8d-130">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="18b8d-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="18b8d-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18b8d-131">See also</span></span>



[<span data-ttu-id="18b8d-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18b8d-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="18b8d-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="18b8d-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="18b8d-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="18b8d-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="18b8d-135">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="18b8d-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

