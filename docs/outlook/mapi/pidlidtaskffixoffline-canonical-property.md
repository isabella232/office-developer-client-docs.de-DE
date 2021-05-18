---
title: PidLidTaskFFixOffline (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 226e59ef6aa88bc290cf5aeb4d620979f926e1eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303038"
---
# <a name="pidlidtaskffixoffline-canonical-property"></a><span data-ttu-id="c6f51-103">PidLidTaskFFixOffline (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c6f51-103">PidLidTaskFFixOffline Canonical Property</span></span>

  
  
<span data-ttu-id="c6f51-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6f51-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6f51-105">Gibt die Genauigkeit der **eigenschaft dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)) an.</span><span class="sxs-lookup"><span data-stu-id="c6f51-105">Indicates the accuracy of the **dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c6f51-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c6f51-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c6f51-107">dispidTaskFFixOffline</span><span class="sxs-lookup"><span data-stu-id="c6f51-107">dispidTaskFFixOffline</span></span>  <br/> |
|<span data-ttu-id="c6f51-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="c6f51-108">Property set:</span></span>  <br/> |<span data-ttu-id="c6f51-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="c6f51-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="c6f51-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="c6f51-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c6f51-111">0x0000812C</span><span class="sxs-lookup"><span data-stu-id="c6f51-111">0x0000812C</span></span>  <br/> |
|<span data-ttu-id="c6f51-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c6f51-112">Data type:</span></span>  <br/> |<span data-ttu-id="c6f51-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c6f51-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c6f51-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c6f51-114">Area:</span></span>  <br/> |<span data-ttu-id="c6f51-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="c6f51-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6f51-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c6f51-116">Remarks</span></span>

<span data-ttu-id="c6f51-117">Wenn die **dispidTaskFFixOffline-Eigenschaft** auf FALSE festgelegt oder nicht festgelegt ist, ist der Wert für die **dispidTaskOwner-Eigenschaft** richtig.</span><span class="sxs-lookup"><span data-stu-id="c6f51-117">If the **dispidTaskFFixOffline** property is set to FALSE or is unset, the value for the **dispidTaskOwner** property is correct.</span></span> <span data-ttu-id="c6f51-118">Wenn **dispidTaskFFixOffline** auf TRUE festgelegt ist, kann der Client keinen genauen Wert für **dispidTaskOwner ermitteln.**</span><span class="sxs-lookup"><span data-stu-id="c6f51-118">If **dispidTaskFFixOffline** is set to TRUE, the client cannot determine an accurate value for **dispidTaskOwner**.</span></span> <span data-ttu-id="c6f51-119">In diesem Fall kann der Client **dispidTaskOwner** auf einen generischen Besitzernamen festlegen, z. B. "Unbekannt".</span><span class="sxs-lookup"><span data-stu-id="c6f51-119">In that case, the client can set **dispidTaskOwner** to a generic owner name, such as "Unknown".</span></span> <span data-ttu-id="c6f51-120">Wenn ein Client jedoch auf den **dispidTaskFFixOffline-Wert** TRUE trifft und einen genauen Besitzernamen bestimmen kann, sollte der Client **dispidTaskOwner** aktualisieren und **dispidTaskFFixOffline** auf FALSE festlegen.</span><span class="sxs-lookup"><span data-stu-id="c6f51-120">However, if a client encounters a **dispidTaskFFixOffline** value of TRUE and can determine an accurate owner name, the client should update **dispidTaskOwner** and set **dispidTaskFFixOffline** to FALSE.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c6f51-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c6f51-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c6f51-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c6f51-122">Protocol specifications</span></span>

<span data-ttu-id="c6f51-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6f51-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c6f51-124">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="c6f51-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c6f51-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6f51-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c6f51-126">Definiert mehrere Objekte, die das elektronische Äquivalent von Vorgängen, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.</span><span class="sxs-lookup"><span data-stu-id="c6f51-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="c6f51-127">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="c6f51-127">Header files</span></span>

<span data-ttu-id="c6f51-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c6f51-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="c6f51-129">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c6f51-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c6f51-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6f51-130">See also</span></span>



[<span data-ttu-id="c6f51-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c6f51-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c6f51-132">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="c6f51-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c6f51-133">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c6f51-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c6f51-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c6f51-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

