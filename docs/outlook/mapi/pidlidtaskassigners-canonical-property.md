---
title: PidLidTaskAssigners (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAssigners
api_type:
- COM
ms.assetid: 07500bd0-bcff-4b03-8ed3-80508875e253
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 97a4915d5422f6c5463ed399835172725b83407f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303066"
---
# <a name="pidlidtaskassigners-canonical-property"></a><span data-ttu-id="2d184-103">PidLidTaskAssigners (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2d184-103">PidLidTaskAssigners Canonical Property</span></span>

  
  
<span data-ttu-id="2d184-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d184-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d184-105">Enthält einen Stapel von Einträgen, die Aufgaben zuweisende Benutzer darstellen.</span><span class="sxs-lookup"><span data-stu-id="2d184-105">Contains a stack of entries that represent task assigners.</span></span> <span data-ttu-id="2d184-106">Der letzte Aufgaben zuweisende Benutzer wird am oberen Rand des Stapels angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2d184-106">The most recent task assigner appears at the top of the stack.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2d184-107">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2d184-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="2d184-108">dispidTaskMyDelegators</span><span class="sxs-lookup"><span data-stu-id="2d184-108">dispidTaskMyDelegators</span></span>  <br/> |
|<span data-ttu-id="2d184-109">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="2d184-109">Property set:</span></span>  <br/> |<span data-ttu-id="2d184-110">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="2d184-110">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="2d184-111">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="2d184-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2d184-112">0x00008117</span><span class="sxs-lookup"><span data-stu-id="2d184-112">0x00008117</span></span>  <br/> |
|<span data-ttu-id="2d184-113">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="2d184-113">Data type:</span></span>  <br/> |<span data-ttu-id="2d184-114">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2d184-114">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2d184-115">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2d184-115">Area:</span></span>  <br/> |<span data-ttu-id="2d184-116">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="2d184-116">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2d184-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2d184-117">Remarks</span></span>

<span data-ttu-id="2d184-118">Wenn der Client eine Aufgabenanforderung empfängt, fügt er diese Eigenschaft an, welche Struktur in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)definiert ist, einem Eintrag, der den Absender der Aufgabe darstellt.</span><span class="sxs-lookup"><span data-stu-id="2d184-118">When the client receives a task request, it appends to this property, which structure is defined in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), an entry that represents the task's sender.</span></span> <span data-ttu-id="2d184-119">Wenn der Client eine Vorgangsabweisung erhält, entfernt der Client den letzten Aufgabenbefeindungseintrag aus dieser Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="2d184-119">When the client receives a task rejection, the client removes the last task assigner entry from this property.</span></span> <span data-ttu-id="2d184-120">Wenn der Client eine Aufgabenantwort sendet, sendet der Client sie an den letzten Task assigner, der im Wert dieser Eigenschaft aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="2d184-120">When the client sends a task response, the client sends it to the last task assigner listed in the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2d184-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2d184-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2d184-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="2d184-122">Protocol specifications</span></span>

<span data-ttu-id="2d184-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2d184-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2d184-124">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="2d184-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2d184-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2d184-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2d184-126">Definiert mehrere Objekte, die das elektronische Äquivalent von Vorgängen, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren</span><span class="sxs-lookup"><span data-stu-id="2d184-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="2d184-127">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="2d184-127">Header files</span></span>

<span data-ttu-id="2d184-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2d184-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="2d184-129">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="2d184-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2d184-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d184-130">See also</span></span>



[<span data-ttu-id="2d184-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2d184-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2d184-132">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="2d184-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2d184-133">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2d184-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2d184-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2d184-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

