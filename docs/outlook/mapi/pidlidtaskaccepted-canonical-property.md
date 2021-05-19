---
title: PidLidTaskAccepted (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAccepted
api_type:
- COM
ms.assetid: 8e31f893-b639-43da-a535-662153c82d82
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0172bf0d69c3f345b592364be754f58c9e7a4420
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331283"
---
# <a name="pidlidtaskaccepted-canonical-property"></a><span data-ttu-id="a1022-103">PidLidTaskAccepted (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a1022-103">PidLidTaskAccepted Canonical Property</span></span>

  
  
<span data-ttu-id="a1022-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1022-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1022-105">Gibt an, ob ein Aufgabenbef?hnter auf eine Vorgangsanforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="a1022-105">Indicates whether a task assignee has replied to a task request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a1022-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a1022-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a1022-107">dispidTaskAccepted</span><span class="sxs-lookup"><span data-stu-id="a1022-107">dispidTaskAccepted</span></span>  <br/> |
|<span data-ttu-id="a1022-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="a1022-108">Property set:</span></span>  <br/> |<span data-ttu-id="a1022-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="a1022-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="a1022-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="a1022-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a1022-111">0x00008108</span><span class="sxs-lookup"><span data-stu-id="a1022-111">0x00008108</span></span>  <br/> |
|<span data-ttu-id="a1022-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a1022-112">Data type:</span></span>  <br/> |<span data-ttu-id="a1022-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="a1022-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="a1022-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a1022-114">Area:</span></span>  <br/> |<span data-ttu-id="a1022-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="a1022-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1022-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a1022-116">Remarks</span></span>

<span data-ttu-id="a1022-117">Der Client legt diese Eigenschaft für einen neuen Vorgang auf FALSE fest, oder der Client legt diese Eigenschaft auf TRUE fest, wenn ein Vorgang angenommen oder abgelehnt wird.</span><span class="sxs-lookup"><span data-stu-id="a1022-117">The client sets this property to FALSE for a new task, or the client sets this property to TRUE when a task is either accepted or rejected.</span></span> <span data-ttu-id="a1022-118">Wenn die Eigenschaft nicht gesetzt ist, wird der Wert FALSE angenommen.</span><span class="sxs-lookup"><span data-stu-id="a1022-118">If the property is left unset, a value of FALSE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a1022-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a1022-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a1022-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a1022-120">Protocol specifications</span></span>

<span data-ttu-id="a1022-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1022-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1022-122">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="a1022-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a1022-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1022-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1022-124">Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="a1022-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a1022-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="a1022-125">Header files</span></span>

<span data-ttu-id="a1022-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a1022-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="a1022-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a1022-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a1022-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1022-128">See also</span></span>



[<span data-ttu-id="a1022-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a1022-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a1022-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="a1022-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a1022-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a1022-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a1022-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a1022-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

