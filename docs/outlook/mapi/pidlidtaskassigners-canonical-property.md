---
title: PidLidTaskAssigners (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAssigners
api_type:
- COM
ms.assetid: 07500bd0-bcff-4b03-8ed3-80508875e253
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 97a4915d5422f6c5463ed399835172725b83407f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385074"
---
# <a name="pidlidtaskassigners-canonical-property"></a><span data-ttu-id="6ca6e-103">PidLidTaskAssigners (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6ca6e-103">PidLidTaskAssigners Canonical Property</span></span>

  
  
<span data-ttu-id="6ca6e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ca6e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ca6e-105">Enthält einen Stack von Einträgen, die Aufgabe Assigners darstellen.</span><span class="sxs-lookup"><span data-stu-id="6ca6e-105">Contains a stack of entries that represent task assigners.</span></span> <span data-ttu-id="6ca6e-106">Die letzte Aufgabe delegierende Person wird am oberen Rand des Stapels angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6ca6e-106">The most recent task assigner appears at the top of the stack.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6ca6e-107">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6ca6e-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="6ca6e-108">dispidTaskMyDelegators</span><span class="sxs-lookup"><span data-stu-id="6ca6e-108">dispidTaskMyDelegators</span></span>  <br/> |
|<span data-ttu-id="6ca6e-109">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="6ca6e-109">Property set:</span></span>  <br/> |<span data-ttu-id="6ca6e-110">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="6ca6e-110">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="6ca6e-111">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="6ca6e-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6ca6e-112">0x00008117</span><span class="sxs-lookup"><span data-stu-id="6ca6e-112">0x00008117</span></span>  <br/> |
|<span data-ttu-id="6ca6e-113">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6ca6e-113">Data type:</span></span>  <br/> |<span data-ttu-id="6ca6e-114">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6ca6e-114">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6ca6e-115">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6ca6e-115">Area:</span></span>  <br/> |<span data-ttu-id="6ca6e-116">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="6ca6e-116">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ca6e-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6ca6e-117">Remarks</span></span>

<span data-ttu-id="6ca6e-118">Wenn der Client eine Aufgabenanfrage erhält, fügt es an diese Eigenschaft, welche Struktur in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), ein Eintrag definiert ist, der Absender die Aufgabe darstellt.</span><span class="sxs-lookup"><span data-stu-id="6ca6e-118">When the client receives a task request, it appends to this property, which structure is defined in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), an entry that represents the task's sender.</span></span> <span data-ttu-id="6ca6e-119">Wenn der Client eine Aufgabe Ablehnung erhält, entfernt der Client den letzten Aufgabe delegierende Person Eintrag aus dieser Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="6ca6e-119">When the client receives a task rejection, the client removes the last task assigner entry from this property.</span></span> <span data-ttu-id="6ca6e-120">Wenn der Client eine Taskantwort sendet, sendet der Client es auf die letzte Aufgabe delegierende Person, die in der Wert dieser Eigenschaft aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6ca6e-120">When the client sends a task response, the client sends it to the last task assigner listed in the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6ca6e-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6ca6e-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6ca6e-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="6ca6e-122">Protocol specifications</span></span>

<span data-ttu-id="6ca6e-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ca6e-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ca6e-124">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="6ca6e-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6ca6e-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ca6e-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ca6e-126">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen modellieren definiert</span><span class="sxs-lookup"><span data-stu-id="6ca6e-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="6ca6e-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="6ca6e-127">Header files</span></span>

<span data-ttu-id="6ca6e-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6ca6e-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="6ca6e-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6ca6e-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6ca6e-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ca6e-130">See also</span></span>



[<span data-ttu-id="6ca6e-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6ca6e-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6ca6e-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6ca6e-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6ca6e-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6ca6e-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6ca6e-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6ca6e-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

