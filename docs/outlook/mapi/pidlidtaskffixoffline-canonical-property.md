---
title: Kanonische Pidlidtaskffixoffline (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFFixOffline
api_type:
- COM
ms.assetid: bbaf7df4-2de0-4da3-9125-eb24dfa94cd8
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 226e59ef6aa88bc290cf5aeb4d620979f926e1eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303038"
---
# <a name="pidlidtaskffixoffline-canonical-property"></a><span data-ttu-id="e07f9-103">Kanonische Pidlidtaskffixoffline (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e07f9-103">PidLidTaskFFixOffline Canonical Property</span></span>

  
  
<span data-ttu-id="e07f9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e07f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e07f9-105">Gibt die Genauigkeit der **dispidTaskOwner** ([pidlidtaskowner (](pidlidtaskowner-canonical-property.md))-Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="e07f9-105">Indicates the accuracy of the **dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e07f9-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e07f9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e07f9-107">dispidTaskFFixOffline</span><span class="sxs-lookup"><span data-stu-id="e07f9-107">dispidTaskFFixOffline</span></span>  <br/> |
|<span data-ttu-id="e07f9-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="e07f9-108">Property set:</span></span>  <br/> |<span data-ttu-id="e07f9-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="e07f9-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="e07f9-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="e07f9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e07f9-111">0x0000812C</span><span class="sxs-lookup"><span data-stu-id="e07f9-111">0x0000812C</span></span>  <br/> |
|<span data-ttu-id="e07f9-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e07f9-112">Data type:</span></span>  <br/> |<span data-ttu-id="e07f9-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e07f9-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e07f9-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e07f9-114">Area:</span></span>  <br/> |<span data-ttu-id="e07f9-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="e07f9-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e07f9-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e07f9-116">Remarks</span></span>

<span data-ttu-id="e07f9-117">Wenn die **dispidTaskFFixOffline** -Eigenschaft auf false oder festgelegt ist, ist der Wert für die **dispidTaskOwner** -Eigenschaft richtig.</span><span class="sxs-lookup"><span data-stu-id="e07f9-117">If the **dispidTaskFFixOffline** property is set to FALSE or is unset, the value for the **dispidTaskOwner** property is correct.</span></span> <span data-ttu-id="e07f9-118">Wenn **dispidTaskFFixOffline** auf true festgelegt ist, kann der Client keinen genauen Wert für **dispidTaskOwner**ermitteln.</span><span class="sxs-lookup"><span data-stu-id="e07f9-118">If **dispidTaskFFixOffline** is set to TRUE, the client cannot determine an accurate value for **dispidTaskOwner**.</span></span> <span data-ttu-id="e07f9-119">In diesem Fall kann der Client **dispidTaskOwner** auf einen generischen Besitzernamen wie "unknown" festlegen.</span><span class="sxs-lookup"><span data-stu-id="e07f9-119">In that case, the client can set **dispidTaskOwner** to a generic owner name, such as "Unknown".</span></span> <span data-ttu-id="e07f9-120">Wenn ein Client jedoch einen **dispidTaskFFixOffline** -Wert von true erkennt und einen genauen Besitzernamen ermitteln kann, sollte der Client **DispidTaskOwner** aktualisieren und **dispidTaskFFixOffline** auf false festlegen.</span><span class="sxs-lookup"><span data-stu-id="e07f9-120">However, if a client encounters a **dispidTaskFFixOffline** value of TRUE and can determine an accurate owner name, the client should update **dispidTaskOwner** and set **dispidTaskFFixOffline** to FALSE.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e07f9-121">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e07f9-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e07f9-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e07f9-122">Protocol specifications</span></span>

<span data-ttu-id="e07f9-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e07f9-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e07f9-124">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="e07f9-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e07f9-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e07f9-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e07f9-126">Definiert mehrere Objekte, die das elektronische Äquivalent von Aufgaben, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.</span><span class="sxs-lookup"><span data-stu-id="e07f9-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="e07f9-127">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="e07f9-127">Header files</span></span>

<span data-ttu-id="e07f9-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e07f9-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="e07f9-129">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="e07f9-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e07f9-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e07f9-130">See also</span></span>



[<span data-ttu-id="e07f9-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e07f9-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e07f9-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e07f9-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e07f9-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e07f9-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e07f9-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e07f9-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

