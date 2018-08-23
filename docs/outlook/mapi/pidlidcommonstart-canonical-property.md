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
ms.openlocfilehash: d0d72f3ca63930f1a8df7818e4ce4a34e8d11e71
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567776"
---
# <a name="pidlidcommonstart-canonical-property"></a><span data-ttu-id="6e3ce-103">PidLidCommonStart (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6e3ce-103">PidLidCommonStart Canonical Property</span></span>

  
  
<span data-ttu-id="6e3ce-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e3ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e3ce-105">Stellt das Startdatum und die Uhrzeit einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="6e3ce-105">Represents the start date and time of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6e3ce-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6e3ce-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6e3ce-107">dispidCommonStart</span><span class="sxs-lookup"><span data-stu-id="6e3ce-107">dispidCommonStart</span></span>  <br/> |
|<span data-ttu-id="6e3ce-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="6e3ce-108">Property set:</span></span>  <br/> |<span data-ttu-id="6e3ce-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="6e3ce-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="6e3ce-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="6e3ce-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6e3ce-111">0x00008516</span><span class="sxs-lookup"><span data-stu-id="6e3ce-111">0x00008516</span></span>  <br/> |
|<span data-ttu-id="6e3ce-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6e3ce-112">Data type:</span></span>  <br/> |<span data-ttu-id="6e3ce-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="6e3ce-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="6e3ce-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6e3ce-114">Area:</span></span>  <br/> |<span data-ttu-id="6e3ce-115">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="6e3ce-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e3ce-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="6e3ce-116">Remarks</span></span>

<span data-ttu-id="6e3ce-117">Diese Eigenschaft gibt die Startzeit für ein Element an.</span><span class="sxs-lookup"><span data-stu-id="6e3ce-117">This property indicates the start time for an item.</span></span> <span data-ttu-id="6e3ce-118">Es muss kleiner oder gleich dem Wert der Eigenschaft **DispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6e3ce-118">It must be less than or equal to the value of the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="6e3ce-119">Der Wert dieser Eigenschaft muss die Entsprechung (Coordinated Universal Time, UTC) der **DispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6e3ce-119">The value of this property must be the Coordinated Universal Time (UTC) equivalent of the **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6e3ce-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6e3ce-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6e3ce-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="6e3ce-121">Protocol specifications</span></span>

<span data-ttu-id="6e3ce-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e3ce-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e3ce-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="6e3ce-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6e3ce-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e3ce-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e3ce-125">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="6e3ce-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="6e3ce-126">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e3ce-126">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e3ce-127">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="6e3ce-127">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6e3ce-128">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="6e3ce-128">Header files</span></span>

<span data-ttu-id="6e3ce-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6e3ce-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="6e3ce-130">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6e3ce-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6e3ce-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e3ce-131">See also</span></span>



[<span data-ttu-id="6e3ce-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6e3ce-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6e3ce-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6e3ce-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6e3ce-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6e3ce-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6e3ce-135">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6e3ce-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

