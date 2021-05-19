---
title: PidLidCommonStart (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCommonStart
api_type:
- COM
ms.assetid: d999852d-ce98-4c3c-a772-87f5db4aa04e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ec7c213d7eec9ab0ef5766442e3de59a24811d37
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345486"
---
# <a name="pidlidcommonstart-canonical-property"></a><span data-ttu-id="c4a43-103">PidLidCommonStart (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c4a43-103">PidLidCommonStart Canonical Property</span></span>

  
  
<span data-ttu-id="c4a43-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4a43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4a43-105">Stellt das Startdatum und die Uhrzeit einer Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="c4a43-105">Represents the start date and time of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c4a43-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c4a43-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c4a43-107">dispidCommonStart</span><span class="sxs-lookup"><span data-stu-id="c4a43-107">dispidCommonStart</span></span>  <br/> |
|<span data-ttu-id="c4a43-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="c4a43-108">Property set:</span></span>  <br/> |<span data-ttu-id="c4a43-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="c4a43-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="c4a43-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="c4a43-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c4a43-111">0x00008516</span><span class="sxs-lookup"><span data-stu-id="c4a43-111">0x00008516</span></span>  <br/> |
|<span data-ttu-id="c4a43-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c4a43-112">Data type:</span></span>  <br/> |<span data-ttu-id="c4a43-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c4a43-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="c4a43-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c4a43-114">Area:</span></span>  <br/> |<span data-ttu-id="c4a43-115">Allgemeines Messaging</span><span class="sxs-lookup"><span data-stu-id="c4a43-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4a43-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c4a43-116">Remarks</span></span>

<span data-ttu-id="c4a43-117">Diese Eigenschaft gibt die Startzeit für ein Element an.</span><span class="sxs-lookup"><span data-stu-id="c4a43-117">This property indicates the start time for an item.</span></span> <span data-ttu-id="c4a43-118">Sie muss kleiner oder gleich dem Wert der **dispidCommonEnd** ([PidLidCommonEnd )-Eigenschaft](pidlidcommonend-canonical-property.md)sein.</span><span class="sxs-lookup"><span data-stu-id="c4a43-118">It must be less than or equal to the value of the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="c4a43-119">Der Wert dieser Eigenschaft muss das UTC-Äquivalent (Coordinated Universal Time) der **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md))-Eigenschaft sein.</span><span class="sxs-lookup"><span data-stu-id="c4a43-119">The value of this property must be the Coordinated Universal Time (UTC) equivalent of the **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c4a43-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c4a43-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c4a43-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c4a43-121">Protocol specifications</span></span>

<span data-ttu-id="c4a43-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4a43-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4a43-123">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="c4a43-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c4a43-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4a43-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4a43-125">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="c4a43-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="c4a43-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4a43-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4a43-127">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="c4a43-127">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c4a43-128">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="c4a43-128">Header files</span></span>

<span data-ttu-id="c4a43-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c4a43-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="c4a43-130">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c4a43-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c4a43-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4a43-131">See also</span></span>



[<span data-ttu-id="c4a43-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c4a43-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c4a43-133">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="c4a43-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c4a43-134">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c4a43-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c4a43-135">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c4a43-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

