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
ms.openlocfilehash: 716d8b5b09ee0e29d1946042cae2631561d74df5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584653"
---
# <a name="pidlidtaskffixoffline-canonical-property"></a><span data-ttu-id="11077-103">PidLidTaskFFixOffline (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="11077-103">PidLidTaskFFixOffline Canonical Property</span></span>

  
  
<span data-ttu-id="11077-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11077-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11077-105">Gibt die Genauigkeit der **DispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md))-Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="11077-105">Indicates the accuracy of the **dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="11077-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="11077-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="11077-107">dispidTaskFFixOffline</span><span class="sxs-lookup"><span data-stu-id="11077-107">dispidTaskFFixOffline</span></span>  <br/> |
|<span data-ttu-id="11077-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="11077-108">Property set:</span></span>  <br/> |<span data-ttu-id="11077-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="11077-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="11077-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="11077-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="11077-111">0x0000812C</span><span class="sxs-lookup"><span data-stu-id="11077-111">0x0000812C</span></span>  <br/> |
|<span data-ttu-id="11077-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="11077-112">Data type:</span></span>  <br/> |<span data-ttu-id="11077-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="11077-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="11077-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="11077-114">Area:</span></span>  <br/> |<span data-ttu-id="11077-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="11077-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11077-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="11077-116">Remarks</span></span>

<span data-ttu-id="11077-117">Wenn die **DispidTaskFFixOffline** -Eigenschaft auf FALSE festgelegt ist oder nicht festgelegt ist, ist der Wert der Eigenschaft **DispidTaskOwner** korrekt.</span><span class="sxs-lookup"><span data-stu-id="11077-117">If the **dispidTaskFFixOffline** property is set to FALSE or is unset, the value for the **dispidTaskOwner** property is correct.</span></span> <span data-ttu-id="11077-118">Wenn **DispidTaskFFixOffline** auf TRUE festgelegt ist, kann der Client einen genauen Wert für **DispidTaskOwner**nicht ermitteln.</span><span class="sxs-lookup"><span data-stu-id="11077-118">If **dispidTaskFFixOffline** is set to TRUE, the client cannot determine an accurate value for **dispidTaskOwner**.</span></span> <span data-ttu-id="11077-119">In diesem Fall kann der Client **DispidTaskOwner** auf einen generischen Besitzername, beispielsweise "Unknown" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="11077-119">In that case, the client can set **dispidTaskOwner** to a generic owner name, such as "Unknown".</span></span> <span data-ttu-id="11077-120">Wenn ein Client einen **DispidTaskFFixOffline** Wert "true trifft" und den Namen eines Besitzers genau bestimmen kann, sollte der Client jedoch **DispidTaskOwner** aktualisieren und **DispidTaskFFixOffline** auf FALSE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="11077-120">However, if a client encounters a **dispidTaskFFixOffline** value of TRUE and can determine an accurate owner name, the client should update **dispidTaskOwner** and set **dispidTaskFFixOffline** to FALSE.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="11077-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="11077-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="11077-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="11077-122">Protocol specifications</span></span>

<span data-ttu-id="11077-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11077-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11077-124">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="11077-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="11077-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="11077-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="11077-126">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="11077-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="11077-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="11077-127">Header files</span></span>

<span data-ttu-id="11077-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="11077-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="11077-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="11077-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="11077-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11077-130">See also</span></span>



[<span data-ttu-id="11077-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="11077-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="11077-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="11077-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="11077-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="11077-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="11077-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="11077-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

