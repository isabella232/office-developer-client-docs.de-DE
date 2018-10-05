---
title: PidLidTaskLastDelegate (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ddf4b81ed35f500dad0029ea6375e9a75a996186
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392326"
---
# <a name="pidlidtasklastdelegate-canonical-property"></a><span data-ttu-id="4b8ff-103">PidLidTaskLastDelegate (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4b8ff-103">PidLidTaskLastDelegate Canonical Property</span></span>

  
  
<span data-ttu-id="4b8ff-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b8ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="4b8ff-105">Gibt den Namen des Benutzers, die zuletzt zugewiesen oder die Aufgabe zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="4b8ff-105">Names the user who most recently assigned or was assigned the task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4b8ff-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4b8ff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4b8ff-107">dispidTaskLastDelegate</span><span class="sxs-lookup"><span data-stu-id="4b8ff-107">dispidTaskLastDelegate</span></span>  <br/> |
|<span data-ttu-id="4b8ff-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="4b8ff-108">Property set:</span></span>  <br/> |<span data-ttu-id="4b8ff-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="4b8ff-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="4b8ff-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="4b8ff-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4b8ff-111">0x00008125</span><span class="sxs-lookup"><span data-stu-id="4b8ff-111">0x00008125</span></span>  <br/> |
|<span data-ttu-id="4b8ff-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4b8ff-112">Data type:</span></span>  <br/> |<span data-ttu-id="4b8ff-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4b8ff-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4b8ff-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4b8ff-114">Area:</span></span>  <br/> |<span data-ttu-id="4b8ff-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="4b8ff-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4b8ff-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4b8ff-116">Remarks</span></span>

<span data-ttu-id="4b8ff-117">Vor dem Senden einer Aufgabenanfrage, wird der Client diese Eigenschaft auf den Namen der Aufgabe delegierende Person.</span><span class="sxs-lookup"><span data-stu-id="4b8ff-117">Before sending a task request, the client sets this property to the name of the task assigner.</span></span> <span data-ttu-id="4b8ff-118">Vor dem Senden einer Aufgabenantwort, wird der Client diese Eigenschaft auf den Namen des Beauftragte für die Aufgabe ein.</span><span class="sxs-lookup"><span data-stu-id="4b8ff-118">Before sending a task response, the client sets this property to the name of the task assignee.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4b8ff-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4b8ff-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4b8ff-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4b8ff-120">Protocol specifications</span></span>

<span data-ttu-id="4b8ff-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b8ff-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b8ff-122">Enthält Set Eigenschaftendefinition und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="4b8ff-122">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4b8ff-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b8ff-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b8ff-124">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="4b8ff-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4b8ff-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="4b8ff-125">Header files</span></span>

<span data-ttu-id="4b8ff-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4b8ff-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="4b8ff-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4b8ff-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4b8ff-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b8ff-128">See also</span></span>



[<span data-ttu-id="4b8ff-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4b8ff-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4b8ff-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4b8ff-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4b8ff-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4b8ff-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4b8ff-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4b8ff-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

