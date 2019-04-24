---
title: Kanonische Pidlidtasklastdelegate (-Eigenschaft
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
ms.openlocfilehash: ddf4b81ed35f500dad0029ea6375e9a75a996186
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355671"
---
# <a name="pidlidtasklastdelegate-canonical-property"></a><span data-ttu-id="b42e5-103">Kanonische Pidlidtasklastdelegate (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b42e5-103">PidLidTaskLastDelegate Canonical Property</span></span>

  
  
<span data-ttu-id="b42e5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b42e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="b42e5-105">Benennt den Benutzer, dem die Aufgabe zuletzt zugewiesen oder zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="b42e5-105">Names the user who most recently assigned or was assigned the task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b42e5-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b42e5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b42e5-107">dispidTaskLastDelegate</span><span class="sxs-lookup"><span data-stu-id="b42e5-107">dispidTaskLastDelegate</span></span>  <br/> |
|<span data-ttu-id="b42e5-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="b42e5-108">Property set:</span></span>  <br/> |<span data-ttu-id="b42e5-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="b42e5-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="b42e5-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="b42e5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b42e5-111">0x00008125</span><span class="sxs-lookup"><span data-stu-id="b42e5-111">0x00008125</span></span>  <br/> |
|<span data-ttu-id="b42e5-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b42e5-112">Data type:</span></span>  <br/> |<span data-ttu-id="b42e5-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b42e5-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b42e5-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b42e5-114">Area:</span></span>  <br/> |<span data-ttu-id="b42e5-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="b42e5-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b42e5-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b42e5-116">Remarks</span></span>

<span data-ttu-id="b42e5-117">Vor dem Senden einer Aufgabenanfrage legt der Client diese Eigenschaft auf den Namen des Aufgaben beauftragten fest.</span><span class="sxs-lookup"><span data-stu-id="b42e5-117">Before sending a task request, the client sets this property to the name of the task assigner.</span></span> <span data-ttu-id="b42e5-118">Vor dem Senden einer Aufgaben Antwort legt der Client diese Eigenschaft auf den Namen des Aufgabenempfängers fest.</span><span class="sxs-lookup"><span data-stu-id="b42e5-118">Before sending a task response, the client sets this property to the name of the task assignee.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b42e5-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b42e5-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b42e5-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b42e5-120">Protocol specifications</span></span>

<span data-ttu-id="b42e5-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b42e5-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b42e5-122">Stellt die Eigenschaftensatz Definition und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="b42e5-122">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b42e5-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b42e5-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b42e5-124">Definiert mehrere Objekte, die das elektronische Äquivalent von Aufgaben, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.</span><span class="sxs-lookup"><span data-stu-id="b42e5-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b42e5-125">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="b42e5-125">Header files</span></span>

<span data-ttu-id="b42e5-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b42e5-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="b42e5-127">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="b42e5-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b42e5-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b42e5-128">See also</span></span>



[<span data-ttu-id="b42e5-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b42e5-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b42e5-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b42e5-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b42e5-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b42e5-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b42e5-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b42e5-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

