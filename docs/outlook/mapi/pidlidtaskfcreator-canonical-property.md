---
title: PidLidTaskFCreator (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFCreator
api_type:
- COM
ms.assetid: bb88750b-4773-4241-aa38-462a2634dbcb
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 458a20e238d6023520ede3416ece239f2d553891
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793834"
---
# <a name="pidlidtaskfcreator-canonical-property"></a><span data-ttu-id="f7b45-103">PidLidTaskFCreator (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f7b45-103">PidLidTaskFCreator Canonical Property</span></span>

  
  
<span data-ttu-id="f7b45-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f7b45-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f7b45-105">Gibt an, dass die Aufgabe durch den aktuellen Benutzer oder die Benutzer-Agent anstelle von ursprünglich erstellt wurde, durch die Verarbeitung einer Aufgabenanfrage.</span><span class="sxs-lookup"><span data-stu-id="f7b45-105">Indicates the task was originally created by the current user or user agent instead of by processing a task request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f7b45-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f7b45-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f7b45-107">dispidTaskFCreator</span><span class="sxs-lookup"><span data-stu-id="f7b45-107">dispidTaskFCreator</span></span>  <br/> |
|<span data-ttu-id="f7b45-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="f7b45-108">Property set:</span></span>  <br/> |<span data-ttu-id="f7b45-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="f7b45-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="f7b45-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="f7b45-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f7b45-111">0x0000811E</span><span class="sxs-lookup"><span data-stu-id="f7b45-111">0x0000811E</span></span>  <br/> |
|<span data-ttu-id="f7b45-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f7b45-112">Data type:</span></span>  <br/> |<span data-ttu-id="f7b45-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f7b45-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f7b45-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f7b45-114">Area:</span></span>  <br/> |<span data-ttu-id="f7b45-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="f7b45-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7b45-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7b45-116">Remarks</span></span>

<span data-ttu-id="f7b45-117">Der Client wird diese Eigenschaft auf true fest, wenn der Benutzer die Aufgabe erstellt und auf false festgelegt, wenn die Aufgabe von einem anderen Benutzer zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="f7b45-117">The client sets this property to TRUE when the user creates the task and to FALSE when the task is assigned by another user.</span></span> <span data-ttu-id="f7b45-118">Wenn Sie diese Eigenschaft nicht festgelegt lassen, wird der Wert TRUE angenommen.</span><span class="sxs-lookup"><span data-stu-id="f7b45-118">If this property is left unset, a value of TRUE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f7b45-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f7b45-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f7b45-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="f7b45-120">Protocol specifications</span></span>

<span data-ttu-id="f7b45-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7b45-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7b45-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="f7b45-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f7b45-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7b45-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7b45-124">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="f7b45-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f7b45-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="f7b45-125">Header files</span></span>

<span data-ttu-id="f7b45-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f7b45-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="f7b45-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f7b45-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f7b45-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7b45-128">See also</span></span>



[<span data-ttu-id="f7b45-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f7b45-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f7b45-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f7b45-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f7b45-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f7b45-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f7b45-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f7b45-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

