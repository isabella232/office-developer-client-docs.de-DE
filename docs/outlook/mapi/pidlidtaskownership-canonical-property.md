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
ms.openlocfilehash: 45fcba3f18aeb9092b71e28a6b68e42ad1abe77d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332109"
---
# <a name="pidlidtaskownership-canonical-property"></a><span data-ttu-id="81601-103">PidLidTaskOwnership (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="81601-103">PidLidTaskOwnership Canonical Property</span></span>

  
  
<span data-ttu-id="81601-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81601-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81601-105">Gibt die Rolle des aktuellen Benutzers relativ zur Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="81601-105">Indicates the role of the current user relative to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="81601-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="81601-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="81601-107">dispidTaskOwnership</span><span class="sxs-lookup"><span data-stu-id="81601-107">dispidTaskOwnership</span></span>  <br/> |
|<span data-ttu-id="81601-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="81601-108">Property set:</span></span>  <br/> |<span data-ttu-id="81601-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="81601-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="81601-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="81601-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="81601-111">0x00008129</span><span class="sxs-lookup"><span data-stu-id="81601-111">0x00008129</span></span>  <br/> |
|<span data-ttu-id="81601-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="81601-112">Data type:</span></span>  <br/> |<span data-ttu-id="81601-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="81601-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="81601-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="81601-114">Area:</span></span>  <br/> |<span data-ttu-id="81601-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="81601-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81601-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="81601-116">Remarks</span></span>

<span data-ttu-id="81601-117">Diese Eigenschaft muss einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="81601-117">This property must be one of the following values.</span></span>
  
|<span data-ttu-id="81601-118">**Wert**</span><span class="sxs-lookup"><span data-stu-id="81601-118">**Value**</span></span>|<span data-ttu-id="81601-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="81601-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="81601-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="81601-120">0x00000000</span></span>  <br/> |<span data-ttu-id="81601-121">Die Aufgabe wird nicht zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="81601-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="81601-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="81601-122">0x00000001</span></span>  <br/> |<span data-ttu-id="81601-123">Bei der Aufgabe handelt es sich um die Kopie der Aufgabe durch den Aufgaben zuweisende Benutzer.</span><span class="sxs-lookup"><span data-stu-id="81601-123">The task is the task assigner's copy of the task.</span></span>  <br/> |
|<span data-ttu-id="81601-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="81601-124">0x00000002</span></span>  <br/> |<span data-ttu-id="81601-125">Die Aufgabe ist die Kopie des Aufgabenbef?hners des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="81601-125">The task is the task assignee's copy of the task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="81601-126">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="81601-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="81601-127">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="81601-127">Protocol specifications</span></span>

<span data-ttu-id="81601-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81601-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81601-129">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="81601-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="81601-130">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81601-130">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81601-131">Definiert mehrere Objekte, die das elektronische Äquivalent von Vorgängen, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.</span><span class="sxs-lookup"><span data-stu-id="81601-131">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="81601-132">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="81601-132">Header files</span></span>

<span data-ttu-id="81601-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="81601-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="81601-134">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="81601-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="81601-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81601-135">See also</span></span>



[<span data-ttu-id="81601-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="81601-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="81601-137">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="81601-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="81601-138">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="81601-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="81601-139">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="81601-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

