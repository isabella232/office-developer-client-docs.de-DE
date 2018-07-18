---
title: PidLidTaskVersion (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskVersion
api_type:
- COM
ms.assetid: 3ab77f25-ad11-4501-8d35-ef560c07e2f2
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a31e2862aa3a6265f1dd9f8036abe329cf556276
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793868"
---
# <a name="pidlidtaskversion-canonical-property"></a><span data-ttu-id="24971-103">PidLidTaskVersion (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="24971-103">PidLidTaskVersion Canonical Property</span></span>

  
  
<span data-ttu-id="24971-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="24971-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="24971-105">Gibt an, welche Kopie eines Vorgangs das neueste Update ist.</span><span class="sxs-lookup"><span data-stu-id="24971-105">Indicates which copy is the latest update of a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="24971-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="24971-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="24971-107">dispidTaskVersion</span><span class="sxs-lookup"><span data-stu-id="24971-107">dispidTaskVersion</span></span>  <br/> |
|<span data-ttu-id="24971-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="24971-108">Property set:</span></span>  <br/> |<span data-ttu-id="24971-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="24971-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="24971-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="24971-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="24971-111">0x00008112</span><span class="sxs-lookup"><span data-stu-id="24971-111">0x00008112</span></span>  <br/> |
|<span data-ttu-id="24971-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="24971-112">Data type:</span></span>  <br/> |<span data-ttu-id="24971-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="24971-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="24971-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="24971-114">Area:</span></span>  <br/> |<span data-ttu-id="24971-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="24971-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24971-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24971-116">Remarks</span></span>

<span data-ttu-id="24971-117">Updates mit niedrigeren Versionen als die Aufgabe werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="24971-117">Updates with lower versions than the task are ignored.</span></span> 
  
<span data-ttu-id="24971-118">Wenn eine Aufgabe in einer Aufgabe Mitteilung einbetten, wird der Client die aktuelle Version der eingebetteten Aufgabe bei der Aufgabe-Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="24971-118">When embedding a task in a task communication, the client sets the current version of the embedded task on the task communication as well.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="24971-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="24971-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="24971-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="24971-120">Protocol specifications</span></span>

<span data-ttu-id="24971-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24971-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24971-122">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="24971-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="24971-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24971-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24971-124">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="24971-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="24971-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="24971-125">Header files</span></span>

<span data-ttu-id="24971-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="24971-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="24971-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="24971-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="24971-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24971-128">See also</span></span>



[<span data-ttu-id="24971-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="24971-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="24971-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="24971-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="24971-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="24971-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="24971-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="24971-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

