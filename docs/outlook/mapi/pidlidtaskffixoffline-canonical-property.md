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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b8da927fe0080a83748bbb2941979dcb246222fa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793839"
---
# <a name="pidlidtaskffixoffline-canonical-property"></a><span data-ttu-id="e0f82-103">PidLidTaskFFixOffline (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e0f82-103">PidLidTaskFFixOffline Canonical Property</span></span>

  
  
<span data-ttu-id="e0f82-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e0f82-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e0f82-105">Gibt die Genauigkeit der **DispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md))-Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="e0f82-105">Indicates the accuracy of the **dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e0f82-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="e0f82-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e0f82-107">dispidTaskFFixOffline</span><span class="sxs-lookup"><span data-stu-id="e0f82-107">dispidTaskFFixOffline</span></span>  <br/> |
|<span data-ttu-id="e0f82-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="e0f82-108">Property set:</span></span>  <br/> |<span data-ttu-id="e0f82-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="e0f82-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="e0f82-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="e0f82-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e0f82-111">0x0000812C</span><span class="sxs-lookup"><span data-stu-id="e0f82-111">0x0000812C</span></span>  <br/> |
|<span data-ttu-id="e0f82-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="e0f82-112">Data type:</span></span>  <br/> |<span data-ttu-id="e0f82-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e0f82-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e0f82-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="e0f82-114">Area:</span></span>  <br/> |<span data-ttu-id="e0f82-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="e0f82-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0f82-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0f82-116">Remarks</span></span>

<span data-ttu-id="e0f82-117">Wenn die **DispidTaskFFixOffline** -Eigenschaft auf FALSE festgelegt ist oder nicht festgelegt ist, ist der Wert der Eigenschaft **DispidTaskOwner** korrekt.</span><span class="sxs-lookup"><span data-stu-id="e0f82-117">If the **dispidTaskFFixOffline** property is set to FALSE or is unset, the value for the **dispidTaskOwner** property is correct.</span></span> <span data-ttu-id="e0f82-118">Wenn **DispidTaskFFixOffline** auf TRUE festgelegt ist, kann der Client einen genauen Wert für **DispidTaskOwner**nicht ermitteln.</span><span class="sxs-lookup"><span data-stu-id="e0f82-118">If **dispidTaskFFixOffline** is set to TRUE, the client cannot determine an accurate value for **dispidTaskOwner**.</span></span> <span data-ttu-id="e0f82-119">In diesem Fall kann der Client **DispidTaskOwner** auf einen generischen Besitzername, beispielsweise "Unknown" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e0f82-119">In that case, the client can set **dispidTaskOwner** to a generic owner name, such as "Unknown".</span></span> <span data-ttu-id="e0f82-120">Wenn ein Client einen **DispidTaskFFixOffline** Wert "true trifft" und den Namen eines Besitzers genau bestimmen kann, sollte der Client jedoch **DispidTaskOwner** aktualisieren und **DispidTaskFFixOffline** auf FALSE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e0f82-120">However, if a client encounters a **dispidTaskFFixOffline** value of TRUE and can determine an accurate owner name, the client should update **dispidTaskOwner** and set **dispidTaskFFixOffline** to FALSE.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e0f82-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e0f82-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e0f82-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="e0f82-122">Protocol specifications</span></span>

<span data-ttu-id="e0f82-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0f82-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0f82-124">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e0f82-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e0f82-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0f82-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0f82-126">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="e0f82-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="e0f82-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="e0f82-127">Header files</span></span>

<span data-ttu-id="e0f82-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e0f82-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="e0f82-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e0f82-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e0f82-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0f82-130">See also</span></span>



[<span data-ttu-id="e0f82-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e0f82-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e0f82-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e0f82-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e0f82-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="e0f82-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e0f82-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="e0f82-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

