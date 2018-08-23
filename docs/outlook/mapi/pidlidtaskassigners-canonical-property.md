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
ms.openlocfilehash: 20a4cf4fc847bdb361fb73161adeb96afb49e57e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570751"
---
# <a name="pidlidtaskassigners-canonical-property"></a><span data-ttu-id="1e9ec-103">PidLidTaskAssigners (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1e9ec-103">PidLidTaskAssigners Canonical Property</span></span>

  
  
<span data-ttu-id="1e9ec-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e9ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e9ec-105">Enthält einen Stack von Einträgen, die Aufgabe Assigners darstellen.</span><span class="sxs-lookup"><span data-stu-id="1e9ec-105">Contains a stack of entries that represent task assigners.</span></span> <span data-ttu-id="1e9ec-106">Die letzte Aufgabe delegierende Person wird am oberen Rand des Stapels angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1e9ec-106">The most recent task assigner appears at the top of the stack.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1e9ec-107">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1e9ec-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="1e9ec-108">dispidTaskMyDelegators</span><span class="sxs-lookup"><span data-stu-id="1e9ec-108">dispidTaskMyDelegators</span></span>  <br/> |
|<span data-ttu-id="1e9ec-109">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="1e9ec-109">Property set:</span></span>  <br/> |<span data-ttu-id="1e9ec-110">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="1e9ec-110">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="1e9ec-111">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="1e9ec-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1e9ec-112">0x00008117</span><span class="sxs-lookup"><span data-stu-id="1e9ec-112">0x00008117</span></span>  <br/> |
|<span data-ttu-id="1e9ec-113">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1e9ec-113">Data type:</span></span>  <br/> |<span data-ttu-id="1e9ec-114">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1e9ec-114">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1e9ec-115">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1e9ec-115">Area:</span></span>  <br/> |<span data-ttu-id="1e9ec-116">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="1e9ec-116">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e9ec-117">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="1e9ec-117">Remarks</span></span>

<span data-ttu-id="1e9ec-118">Wenn der Client eine Aufgabenanfrage erhält, fügt es an diese Eigenschaft, welche Struktur in [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), ein Eintrag definiert ist, der Absender die Aufgabe darstellt.</span><span class="sxs-lookup"><span data-stu-id="1e9ec-118">When the client receives a task request, it appends to this property, which structure is defined in [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), an entry that represents the task's sender.</span></span> <span data-ttu-id="1e9ec-119">Wenn der Client eine Aufgabe Ablehnung erhält, entfernt der Client den letzten Aufgabe delegierende Person Eintrag aus dieser Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="1e9ec-119">When the client receives a task rejection, the client removes the last task assigner entry from this property.</span></span> <span data-ttu-id="1e9ec-120">Wenn der Client eine Taskantwort sendet, sendet der Client es auf die letzte Aufgabe delegierende Person, die in der Wert dieser Eigenschaft aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1e9ec-120">When the client sends a task response, the client sends it to the last task assigner listed in the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1e9ec-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1e9ec-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1e9ec-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="1e9ec-122">Protocol specifications</span></span>

<span data-ttu-id="1e9ec-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e9ec-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e9ec-124">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="1e9ec-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1e9ec-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e9ec-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e9ec-126">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen modellieren definiert</span><span class="sxs-lookup"><span data-stu-id="1e9ec-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="1e9ec-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="1e9ec-127">Header files</span></span>

<span data-ttu-id="1e9ec-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1e9ec-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="1e9ec-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1e9ec-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1e9ec-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e9ec-130">See also</span></span>



[<span data-ttu-id="1e9ec-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1e9ec-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1e9ec-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1e9ec-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1e9ec-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1e9ec-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1e9ec-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1e9ec-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

