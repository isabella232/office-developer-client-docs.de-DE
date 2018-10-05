---
title: PidLidTaskLastUser (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskLastUser
api_type:
- COM
ms.assetid: 914c55e9-cb36-46a4-b5ee-382413fa25f9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 76311a76001b122bdfd984b9dedc37c2ff878fc7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390933"
---
# <a name="pidlidtasklastuser-canonical-property"></a><span data-ttu-id="387a9-103">PidLidTaskLastUser (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="387a9-103">PidLidTaskLastUser Canonical Property</span></span>

  
  
<span data-ttu-id="387a9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="387a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="387a9-105">Gibt den Namen des aktuelle Benutzers, der Besitzer der Aufgabe wurde.</span><span class="sxs-lookup"><span data-stu-id="387a9-105">Names the most recent user who was the task owner.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="387a9-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="387a9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="387a9-107">dispidTaskLastUser</span><span class="sxs-lookup"><span data-stu-id="387a9-107">dispidTaskLastUser</span></span>  <br/> |
|<span data-ttu-id="387a9-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="387a9-108">Property set:</span></span>  <br/> |<span data-ttu-id="387a9-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="387a9-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="387a9-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="387a9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="387a9-111">0x00008122</span><span class="sxs-lookup"><span data-stu-id="387a9-111">0x00008122</span></span>  <br/> |
|<span data-ttu-id="387a9-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="387a9-112">Data type:</span></span>  <br/> |<span data-ttu-id="387a9-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="387a9-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="387a9-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="387a9-114">Area:</span></span>  <br/> |<span data-ttu-id="387a9-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="387a9-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="387a9-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="387a9-116">Remarks</span></span>

<span data-ttu-id="387a9-117">Bevor ein Client eine Aufgabenanfrage sendet, wird diese Eigenschaft auf den Namen der Aufgabe delegierende Person.</span><span class="sxs-lookup"><span data-stu-id="387a9-117">Before a client sends a task request, it sets this property to the name of the task assigner.</span></span> <span data-ttu-id="387a9-118">Bevor ein Client eine Aufgabe Annahme sendet, wird diese Eigenschaft auf den Namen der Beauftragte für die Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="387a9-118">Before a client sends a task acceptance, it sets this property to the name of the task assignee.</span></span> <span data-ttu-id="387a9-119">Bevor ein Client eine Aufgabe Ablehnung sendet, wird diese Eigenschaft auf den Namen der Aufgabe delegierende Person.</span><span class="sxs-lookup"><span data-stu-id="387a9-119">Before a client sends a task rejection, it sets this property to the name of the task assigner.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="387a9-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="387a9-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="387a9-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="387a9-121">Protocol specifications</span></span>

<span data-ttu-id="387a9-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="387a9-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="387a9-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="387a9-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="387a9-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="387a9-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="387a9-125">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="387a9-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="387a9-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="387a9-126">Header files</span></span>

<span data-ttu-id="387a9-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="387a9-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="387a9-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="387a9-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="387a9-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="387a9-129">See also</span></span>



[<span data-ttu-id="387a9-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="387a9-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="387a9-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="387a9-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="387a9-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="387a9-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="387a9-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="387a9-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

