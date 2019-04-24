---
title: Kanonische Pidlidtaskestimatedeffort (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskEstimatedEffort
api_type:
- COM
ms.assetid: c84167d8-f726-45c6-9b21-bcde64473148
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5700ab6baaab2a5e73448582a855e6f243d5361d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303045"
---
# <a name="pidlidtaskestimatedeffort-canonical-property"></a><span data-ttu-id="b7d81-103">Kanonische Pidlidtaskestimatedeffort (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b7d81-103">PidLidTaskEstimatedEffort Canonical Property</span></span>

  
  
<span data-ttu-id="b7d81-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7d81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7d81-105">Gibt die Zeitdauer (in Minuten) an, die der Benutzer zum Ausführen einer Aufgabe erwartet.</span><span class="sxs-lookup"><span data-stu-id="b7d81-105">Indicates the amount of time, in minutes, that the user expects to perform a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b7d81-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b7d81-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b7d81-107">dispidTaskEstimatedEffort</span><span class="sxs-lookup"><span data-stu-id="b7d81-107">dispidTaskEstimatedEffort</span></span>  <br/> |
|<span data-ttu-id="b7d81-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="b7d81-108">Property set:</span></span>  <br/> |<span data-ttu-id="b7d81-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="b7d81-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="b7d81-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="b7d81-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b7d81-111">0x00008111</span><span class="sxs-lookup"><span data-stu-id="b7d81-111">0x00008111</span></span>  <br/> |
|<span data-ttu-id="b7d81-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b7d81-112">Data type:</span></span>  <br/> |<span data-ttu-id="b7d81-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b7d81-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b7d81-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b7d81-114">Area:</span></span>  <br/> |<span data-ttu-id="b7d81-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="b7d81-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7d81-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7d81-116">Remarks</span></span>

<span data-ttu-id="b7d81-117">Der Wert muss größer oder gleich 0 und kleiner als 0x5AE980DF (1.525.252.319) sein, wobei 480 Minuten ein Tag und 2400 Minuten eine Woche (acht Stunden an einem Arbeitstag und fünf Tage in einer Arbeitswoche) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b7d81-117">The value must be greater than or equal to 0 and less than 0x5AE980DF (1,525,252,319), where 480 minutes equal one day and 2400 minutes equal one week (eight hours in a work day and five days in a work week).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b7d81-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b7d81-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b7d81-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b7d81-119">Protocol specifications</span></span>

<span data-ttu-id="b7d81-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7d81-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7d81-121">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="b7d81-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b7d81-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7d81-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7d81-123">Definiert mehrere Objekte, die das elektronische Äquivalent von Aufgaben, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren.</span><span class="sxs-lookup"><span data-stu-id="b7d81-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="b7d81-124">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="b7d81-124">Header files</span></span>

<span data-ttu-id="b7d81-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b7d81-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="b7d81-126">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="b7d81-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b7d81-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7d81-127">See also</span></span>



[<span data-ttu-id="b7d81-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b7d81-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b7d81-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b7d81-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b7d81-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b7d81-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b7d81-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b7d81-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

