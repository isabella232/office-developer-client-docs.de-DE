---
title: Kanonische pidlidcommonend (-Eigenschaft
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
ms.openlocfilehash: 97d6ef6343cedb6fbed93cccda9f65476bb73f4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345500"
---
# <a name="pidlidcommonend-canonical-property"></a><span data-ttu-id="edbc0-103">Kanonische pidlidcommonend (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="edbc0-103">PidLidCommonEnd Canonical Property</span></span>

  
  
<span data-ttu-id="edbc0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="edbc0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="edbc0-105">Stellt das Enddatum und die Endzeit einer Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="edbc0-105">Represents the end date and time of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="edbc0-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="edbc0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="edbc0-107">dispidCommonEnd</span><span class="sxs-lookup"><span data-stu-id="edbc0-107">dispidCommonEnd</span></span>  <br/> |
|<span data-ttu-id="edbc0-108">Eigenschaftengruppe:</span><span class="sxs-lookup"><span data-stu-id="edbc0-108">Property set:</span></span>  <br/> |<span data-ttu-id="edbc0-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="edbc0-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="edbc0-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="edbc0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="edbc0-111">0x00008517</span><span class="sxs-lookup"><span data-stu-id="edbc0-111">0x00008517</span></span>  <br/> |
|<span data-ttu-id="edbc0-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="edbc0-112">Data type:</span></span>  <br/> |<span data-ttu-id="edbc0-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="edbc0-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="edbc0-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="edbc0-114">Area:</span></span>  <br/> |<span data-ttu-id="edbc0-115">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="edbc0-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="edbc0-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="edbc0-116">Remarks</span></span>

<span data-ttu-id="edbc0-117">Diese Eigenschaft gibt die Endzeit für ein Element an.</span><span class="sxs-lookup"><span data-stu-id="edbc0-117">This property indicates the end time for an item.</span></span> <span data-ttu-id="edbc0-118">Sie muss größer als oder gleich dem Wert der **dispidCommonStart** ([pidlidcommonstart (](pidlidcommonstart-canonical-property.md))-Eigenschaft sein.</span><span class="sxs-lookup"><span data-stu-id="edbc0-118">It must be greater than or equal to the value of the **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="edbc0-119">Dieser Wert muss die UTC-Entsprechung (Coordinated Universal Time) der **dispidTaskDueDate** ([pidlidtaskduedate (](pidlidtaskduedate-canonical-property.md))-Eigenschaft sein.</span><span class="sxs-lookup"><span data-stu-id="edbc0-119">This value must be the Coordinated Universal Time (UTC) equivalent of the **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="edbc0-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="edbc0-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="edbc0-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="edbc0-121">Protocol specifications</span></span>

<span data-ttu-id="edbc0-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edbc0-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edbc0-123">Stellt Eigenschaftenmengen Definitionen und Verweise auf zugehörige Exchange Server Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="edbc0-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="edbc0-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edbc0-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edbc0-125">Verarbeitet Nachrichten-und Attachment-Objekte.</span><span class="sxs-lookup"><span data-stu-id="edbc0-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="edbc0-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="edbc0-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="edbc0-127">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="edbc0-127">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="edbc0-128">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="edbc0-128">Header files</span></span>

<span data-ttu-id="edbc0-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="edbc0-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="edbc0-130">Stellt Definitionen von Datentypen bereit.</span><span class="sxs-lookup"><span data-stu-id="edbc0-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="edbc0-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="edbc0-131">See also</span></span>



[<span data-ttu-id="edbc0-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="edbc0-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="edbc0-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="edbc0-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="edbc0-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="edbc0-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="edbc0-135">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="edbc0-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

