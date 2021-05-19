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
ms.openlocfilehash: 97d6ef6343cedb6fbed93cccda9f65476bb73f4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345500"
---
# <a name="pidlidcommonend-canonical-property"></a><span data-ttu-id="6cc85-103">PidLidCommonEnd (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6cc85-103">PidLidCommonEnd Canonical Property</span></span>

  
  
<span data-ttu-id="6cc85-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6cc85-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6cc85-105">Stellt das Enddatum und die Uhrzeit einer Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="6cc85-105">Represents the end date and time of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6cc85-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6cc85-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6cc85-107">dispidCommonEnd</span><span class="sxs-lookup"><span data-stu-id="6cc85-107">dispidCommonEnd</span></span>  <br/> |
|<span data-ttu-id="6cc85-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="6cc85-108">Property set:</span></span>  <br/> |<span data-ttu-id="6cc85-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="6cc85-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="6cc85-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="6cc85-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6cc85-111">0x00008517</span><span class="sxs-lookup"><span data-stu-id="6cc85-111">0x00008517</span></span>  <br/> |
|<span data-ttu-id="6cc85-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6cc85-112">Data type:</span></span>  <br/> |<span data-ttu-id="6cc85-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="6cc85-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="6cc85-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6cc85-114">Area:</span></span>  <br/> |<span data-ttu-id="6cc85-115">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="6cc85-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6cc85-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6cc85-116">Remarks</span></span>

<span data-ttu-id="6cc85-117">Diese Eigenschaft gibt die Endzeit für ein Element an.</span><span class="sxs-lookup"><span data-stu-id="6cc85-117">This property indicates the end time for an item.</span></span> <span data-ttu-id="6cc85-118">Sie muss größer oder gleich dem Wert der **dispidCommonStart** ([PidLidCommonStart )-Eigenschaft](pidlidcommonstart-canonical-property.md)sein.</span><span class="sxs-lookup"><span data-stu-id="6cc85-118">It must be greater than or equal to the value of the **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="6cc85-119">Dieser Wert muss das Äquivalent der **Eigenschaft dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) sein.</span><span class="sxs-lookup"><span data-stu-id="6cc85-119">This value must be the Coordinated Universal Time (UTC) equivalent of the **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6cc85-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6cc85-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6cc85-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="6cc85-121">Protocol specifications</span></span>

<span data-ttu-id="6cc85-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6cc85-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6cc85-123">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="6cc85-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6cc85-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6cc85-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6cc85-125">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="6cc85-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="6cc85-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6cc85-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6cc85-127">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="6cc85-127">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6cc85-128">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="6cc85-128">Header files</span></span>

<span data-ttu-id="6cc85-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6cc85-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="6cc85-130">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6cc85-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6cc85-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6cc85-131">See also</span></span>



[<span data-ttu-id="6cc85-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6cc85-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6cc85-133">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="6cc85-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6cc85-134">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6cc85-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6cc85-135">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6cc85-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

