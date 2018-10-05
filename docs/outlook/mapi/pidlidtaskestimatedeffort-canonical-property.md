---
title: PidLidTaskEstimatedEffort (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5700ab6baaab2a5e73448582a855e6f243d5361d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382799"
---
# <a name="pidlidtaskestimatedeffort-canonical-property"></a><span data-ttu-id="25849-103">PidLidTaskEstimatedEffort (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="25849-103">PidLidTaskEstimatedEffort Canonical Property</span></span>

  
  
<span data-ttu-id="25849-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25849-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25849-105">Gibt die Zeitspanne in Minuten, die der Benutzer zum Ausführen einer Aufgabe erwartet an.</span><span class="sxs-lookup"><span data-stu-id="25849-105">Indicates the amount of time, in minutes, that the user expects to perform a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="25849-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="25849-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="25849-107">dispidTaskEstimatedEffort</span><span class="sxs-lookup"><span data-stu-id="25849-107">dispidTaskEstimatedEffort</span></span>  <br/> |
|<span data-ttu-id="25849-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="25849-108">Property set:</span></span>  <br/> |<span data-ttu-id="25849-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="25849-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="25849-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="25849-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="25849-111">0x00008111</span><span class="sxs-lookup"><span data-stu-id="25849-111">0x00008111</span></span>  <br/> |
|<span data-ttu-id="25849-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="25849-112">Data type:</span></span>  <br/> |<span data-ttu-id="25849-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="25849-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="25849-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="25849-114">Area:</span></span>  <br/> |<span data-ttu-id="25849-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="25849-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25849-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="25849-116">Remarks</span></span>

<span data-ttu-id="25849-117">Der Wert muss größer als oder gleich 0 und kleiner als 0x5AE980DF (1,525,252,319), wobei gleich 480 Minuten eine Tag und 2400 Minuten gleich eine Woche (acht Stunden in einen Arbeitstag und fünf Tage in einer Arbeitswoche).</span><span class="sxs-lookup"><span data-stu-id="25849-117">The value must be greater than or equal to 0 and less than 0x5AE980DF (1,525,252,319), where 480 minutes equal one day and 2400 minutes equal one week (eight hours in a work day and five days in a work week).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="25849-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="25849-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="25849-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="25849-119">Protocol specifications</span></span>

<span data-ttu-id="25849-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25849-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25849-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="25849-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="25849-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25849-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25849-123">Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.</span><span class="sxs-lookup"><span data-stu-id="25849-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="25849-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="25849-124">Header files</span></span>

<span data-ttu-id="25849-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="25849-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="25849-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="25849-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="25849-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25849-127">See also</span></span>



[<span data-ttu-id="25849-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="25849-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="25849-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="25849-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="25849-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="25849-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="25849-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="25849-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

