---
title: Kanonische Pidlidcommonend (-Eigenschaft
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
ms.openlocfilehash: 97d6ef6343cedb6fbed93cccda9f65476bb73f4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345500"
---
# <a name="pidlidcommonend-canonical-property"></a><span data-ttu-id="9bad1-103">Kanonische Pidlidcommonend (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9bad1-103">PidLidCommonEnd Canonical Property</span></span>

  
  
<span data-ttu-id="9bad1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9bad1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9bad1-105">Stellt das Enddatum und die Uhrzeit einer Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="9bad1-105">Represents the end date and time of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9bad1-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="9bad1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9bad1-107">dispidCommonEnd</span><span class="sxs-lookup"><span data-stu-id="9bad1-107">dispidCommonEnd</span></span>  <br/> |
|<span data-ttu-id="9bad1-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="9bad1-108">Property set:</span></span>  <br/> |<span data-ttu-id="9bad1-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="9bad1-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="9bad1-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="9bad1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9bad1-111">0x00008517</span><span class="sxs-lookup"><span data-stu-id="9bad1-111">0x00008517</span></span>  <br/> |
|<span data-ttu-id="9bad1-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="9bad1-112">Data type:</span></span>  <br/> |<span data-ttu-id="9bad1-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="9bad1-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="9bad1-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="9bad1-114">Area:</span></span>  <br/> |<span data-ttu-id="9bad1-115">Allgemeine Nachrichtenübermittlung</span><span class="sxs-lookup"><span data-stu-id="9bad1-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9bad1-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9bad1-116">Remarks</span></span>

<span data-ttu-id="9bad1-117">Diese Eigenschaft gibt die Endzeit für ein Element an.</span><span class="sxs-lookup"><span data-stu-id="9bad1-117">This property indicates the end time for an item.</span></span> <span data-ttu-id="9bad1-118">Sie muss größer oder gleich dem Wert der **dispidCommonStart** ([pidlidcommonstart (](pidlidcommonstart-canonical-property.md))-Eigenschaft sein.</span><span class="sxs-lookup"><span data-stu-id="9bad1-118">It must be greater than or equal to the value of the **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="9bad1-119">Dieser Wert muss die UTC-Entsprechung (Coordinated Universal Time) der **dispidTaskDueDate** ([pidlidtaskduedate (](pidlidtaskduedate-canonical-property.md))-Eigenschaft sein.</span><span class="sxs-lookup"><span data-stu-id="9bad1-119">This value must be the Coordinated Universal Time (UTC) equivalent of the **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9bad1-120">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9bad1-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9bad1-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="9bad1-121">Protocol specifications</span></span>

<span data-ttu-id="9bad1-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9bad1-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9bad1-123">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="9bad1-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9bad1-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9bad1-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9bad1-125">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="9bad1-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="9bad1-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9bad1-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9bad1-127">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="9bad1-127">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9bad1-128">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="9bad1-128">Header files</span></span>

<span data-ttu-id="9bad1-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9bad1-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="9bad1-130">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="9bad1-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9bad1-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9bad1-131">See also</span></span>



[<span data-ttu-id="9bad1-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9bad1-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9bad1-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9bad1-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9bad1-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="9bad1-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9bad1-135">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="9bad1-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

