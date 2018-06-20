---
title: Kanonische PidLidTaskLastDelegate-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskLastDelegate
api_type:
- COM
ms.assetid: 5eb8c1ce-063f-4273-acba-e6f9c994e7d3
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8e1a343486e78daae45ca7315ba4d29d44b688bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793837"
---
# <a name="pidlidtasklastdelegate-canonical-property"></a><span data-ttu-id="c7c51-103">Kanonische PidLidTaskLastDelegate-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c7c51-103">PidLidTaskLastDelegate Canonical Property</span></span>

  
  
<span data-ttu-id="c7c51-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c7c51-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="c7c51-105">Gibt den Namen des Benutzers, die zuletzt zugewiesen oder die Aufgabe zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="c7c51-105">Names the user who most recently assigned or was assigned the task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c7c51-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c7c51-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c7c51-107">dispidTaskLastDelegate</span><span class="sxs-lookup"><span data-stu-id="c7c51-107">dispidTaskLastDelegate</span></span>  <br/> |
|<span data-ttu-id="c7c51-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="c7c51-108">Property set:</span></span>  <br/> |<span data-ttu-id="c7c51-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="c7c51-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="c7c51-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="c7c51-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c7c51-111">0x00008125</span><span class="sxs-lookup"><span data-stu-id="c7c51-111">0x00008125</span></span>  <br/> |
|<span data-ttu-id="c7c51-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c7c51-112">Data type:</span></span>  <br/> |<span data-ttu-id="c7c51-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c7c51-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c7c51-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c7c51-114">Area:</span></span>  <br/> |<span data-ttu-id="c7c51-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="c7c51-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7c51-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c7c51-116">Remarks</span></span>

<span data-ttu-id="c7c51-117">Vor dem Senden einer Aufgabenanfrage, wird der Client diese Eigenschaft auf den Namen der Aufgabe delegierende Person.</span><span class="sxs-lookup"><span data-stu-id="c7c51-117">Before sending a task request, the client sets this property to the name of the task assigner.</span></span> <span data-ttu-id="c7c51-118">Vor dem Senden einer Aufgabenantwort, wird der Client diese Eigenschaft auf den Namen des Beauftragte für die Aufgabe ein.</span><span class="sxs-lookup"><span data-stu-id="c7c51-118">Before sending a task response, the client sets this property to the name of the task assignee.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c7c51-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c7c51-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c7c51-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c7c51-120">Protocol specifications</span></span>

<span data-ttu-id="c7c51-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c7c51-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c7c51-122">Enthält Set Eigenschaftendefinition und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="c7c51-122">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c7c51-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c7c51-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c7c51-124">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="c7c51-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c7c51-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="c7c51-125">Header files</span></span>

<span data-ttu-id="c7c51-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c7c51-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c7c51-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c7c51-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c7c51-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7c51-128">See also</span></span>



[<span data-ttu-id="c7c51-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c7c51-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c7c51-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c7c51-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c7c51-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c7c51-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c7c51-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c7c51-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

