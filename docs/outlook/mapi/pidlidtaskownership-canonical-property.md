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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 17f3ac0c5cd6005329212d0dcb458b37bb75f41d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793865"
---
# <a name="pidlidtaskownership-canonical-property"></a><span data-ttu-id="0d781-103">PidLidTaskOwnership (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0d781-103">PidLidTaskOwnership Canonical Property</span></span>

  
  
<span data-ttu-id="0d781-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0d781-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0d781-105">Gibt die Rolle des aktuellen Benutzers relativ zu der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="0d781-105">Indicates the role of the current user relative to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0d781-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0d781-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0d781-107">dispidTaskOwnership</span><span class="sxs-lookup"><span data-stu-id="0d781-107">dispidTaskOwnership</span></span>  <br/> |
|<span data-ttu-id="0d781-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="0d781-108">Property set:</span></span>  <br/> |<span data-ttu-id="0d781-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="0d781-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="0d781-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="0d781-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0d781-111">0x00008129</span><span class="sxs-lookup"><span data-stu-id="0d781-111">0x00008129</span></span>  <br/> |
|<span data-ttu-id="0d781-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0d781-112">Data type:</span></span>  <br/> |<span data-ttu-id="0d781-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0d781-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0d781-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0d781-114">Area:</span></span>  <br/> |<span data-ttu-id="0d781-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="0d781-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d781-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d781-116">Remarks</span></span>

<span data-ttu-id="0d781-117">Diese Eigenschaft muss eine der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="0d781-117">This property must be one of the following values.</span></span>
  
|<span data-ttu-id="0d781-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="0d781-118">**Value**</span></span>|<span data-ttu-id="0d781-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0d781-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0d781-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d781-120">0x00000000</span></span>  <br/> |<span data-ttu-id="0d781-121">Die Aufgabe wird nicht zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="0d781-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="0d781-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0d781-122">0x00000001</span></span>  <br/> |<span data-ttu-id="0d781-123">Die Aufgabe ist die Aufgabe delegierende Person Kopie des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="0d781-123">The task is the task assigner's copy of the task.</span></span>  <br/> |
|<span data-ttu-id="0d781-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="0d781-124">0x00000002</span></span>  <br/> |<span data-ttu-id="0d781-125">Der Vorgang ist der Aufgabe zugewiesenen Kopie des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="0d781-125">The task is the task assignee's copy of the task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="0d781-126">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0d781-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0d781-127">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0d781-127">Protocol specifications</span></span>

<span data-ttu-id="0d781-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0d781-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0d781-129">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="0d781-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0d781-130">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0d781-130">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0d781-131">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="0d781-131">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0d781-132">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="0d781-132">Header files</span></span>

<span data-ttu-id="0d781-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0d781-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="0d781-134">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0d781-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0d781-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d781-135">See also</span></span>



[<span data-ttu-id="0d781-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0d781-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0d781-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0d781-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0d781-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0d781-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0d781-139">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0d781-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

