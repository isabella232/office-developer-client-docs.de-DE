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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355671"
---
# <a name="pidlidtasklastdelegate-canonical-property"></a><span data-ttu-id="7e4de-103">PidLidTaskLastDelegate (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7e4de-103">PidLidTaskLastDelegate Canonical Property</span></span>

  
  
<span data-ttu-id="7e4de-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e4de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="7e4de-105">Benennt den Benutzer, dem die Aufgabe zuletzt zugewiesen oder zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="7e4de-105">Names the user who most recently assigned or was assigned the task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7e4de-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7e4de-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7e4de-107">dispidTaskLastDelegate</span><span class="sxs-lookup"><span data-stu-id="7e4de-107">dispidTaskLastDelegate</span></span>  <br/> |
|<span data-ttu-id="7e4de-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="7e4de-108">Property set:</span></span>  <br/> |<span data-ttu-id="7e4de-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="7e4de-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="7e4de-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="7e4de-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7e4de-111">0x00008125</span><span class="sxs-lookup"><span data-stu-id="7e4de-111">0x00008125</span></span>  <br/> |
|<span data-ttu-id="7e4de-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7e4de-112">Data type:</span></span>  <br/> |<span data-ttu-id="7e4de-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7e4de-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7e4de-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7e4de-114">Area:</span></span>  <br/> |<span data-ttu-id="7e4de-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="7e4de-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e4de-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7e4de-116">Remarks</span></span>

<span data-ttu-id="7e4de-117">Vor dem Senden einer Aufgabenanforderung legt der Client diese Eigenschaft auf den Namen des Aufgabenbef?hners fest.</span><span class="sxs-lookup"><span data-stu-id="7e4de-117">Before sending a task request, the client sets this property to the name of the task assigner.</span></span> <span data-ttu-id="7e4de-118">Vor dem Senden einer Aufgabenantwort legt der Client diese Eigenschaft auf den Namen des Aufgabenbeantworter fest.</span><span class="sxs-lookup"><span data-stu-id="7e4de-118">Before sending a task response, the client sets this property to the name of the task assignee.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7e4de-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7e4de-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7e4de-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="7e4de-120">Protocol specifications</span></span>

<span data-ttu-id="7e4de-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e4de-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e4de-122">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="7e4de-122">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7e4de-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e4de-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e4de-124">Definiert mehrere Objekte, die das elektronische Äquivalent von Vorgängen, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.</span><span class="sxs-lookup"><span data-stu-id="7e4de-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7e4de-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="7e4de-125">Header files</span></span>

<span data-ttu-id="7e4de-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7e4de-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="7e4de-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7e4de-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7e4de-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e4de-128">See also</span></span>



[<span data-ttu-id="7e4de-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7e4de-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7e4de-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="7e4de-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7e4de-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7e4de-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7e4de-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7e4de-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

