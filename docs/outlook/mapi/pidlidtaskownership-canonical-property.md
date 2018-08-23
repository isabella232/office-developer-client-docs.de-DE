---
title: PidLidTaskOwnership (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskOwnership
api_type:
- COM
ms.assetid: 805dcb6c-f405-4c4d-8bca-af4bd9cd44fa
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5c335d8fab820c9876adbe8f001696a02068460c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591408"
---
# <a name="pidlidtaskownership-canonical-property"></a><span data-ttu-id="cccdb-103">PidLidTaskOwnership (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="cccdb-103">PidLidTaskOwnership Canonical Property</span></span>

  
  
<span data-ttu-id="cccdb-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cccdb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cccdb-105">Gibt die Rolle des aktuellen Benutzers relativ zu der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="cccdb-105">Indicates the role of the current user relative to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cccdb-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="cccdb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cccdb-107">dispidTaskOwnership</span><span class="sxs-lookup"><span data-stu-id="cccdb-107">dispidTaskOwnership</span></span>  <br/> |
|<span data-ttu-id="cccdb-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="cccdb-108">Property set:</span></span>  <br/> |<span data-ttu-id="cccdb-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="cccdb-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="cccdb-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="cccdb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="cccdb-111">0x00008129</span><span class="sxs-lookup"><span data-stu-id="cccdb-111">0x00008129</span></span>  <br/> |
|<span data-ttu-id="cccdb-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="cccdb-112">Data type:</span></span>  <br/> |<span data-ttu-id="cccdb-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cccdb-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cccdb-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="cccdb-114">Area:</span></span>  <br/> |<span data-ttu-id="cccdb-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="cccdb-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cccdb-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="cccdb-116">Remarks</span></span>

<span data-ttu-id="cccdb-117">Diese Eigenschaft muss eine der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="cccdb-117">This property must be one of the following values.</span></span>
  
|<span data-ttu-id="cccdb-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="cccdb-118">**Value**</span></span>|<span data-ttu-id="cccdb-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cccdb-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cccdb-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cccdb-120">0x00000000</span></span>  <br/> |<span data-ttu-id="cccdb-121">Die Aufgabe wird nicht zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="cccdb-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="cccdb-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="cccdb-122">0x00000001</span></span>  <br/> |<span data-ttu-id="cccdb-123">Die Aufgabe ist die Aufgabe delegierende Person Kopie des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="cccdb-123">The task is the task assigner's copy of the task.</span></span>  <br/> |
|<span data-ttu-id="cccdb-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="cccdb-124">0x00000002</span></span>  <br/> |<span data-ttu-id="cccdb-125">Der Vorgang ist der Aufgabe zugewiesenen Kopie des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="cccdb-125">The task is the task assignee's copy of the task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="cccdb-126">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cccdb-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cccdb-127">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="cccdb-127">Protocol specifications</span></span>

<span data-ttu-id="cccdb-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cccdb-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cccdb-129">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="cccdb-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cccdb-130">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cccdb-130">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cccdb-131">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="cccdb-131">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cccdb-132">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="cccdb-132">Header files</span></span>

<span data-ttu-id="cccdb-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cccdb-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="cccdb-134">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="cccdb-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cccdb-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cccdb-135">See also</span></span>



[<span data-ttu-id="cccdb-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cccdb-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cccdb-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cccdb-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cccdb-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="cccdb-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cccdb-139">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="cccdb-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

