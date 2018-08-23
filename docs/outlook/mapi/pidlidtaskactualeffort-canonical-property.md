---
title: PidLidTaskActualEffort (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskActualEffort
api_type:
- COM
ms.assetid: 8e9a9432-bf50-4333-82ec-fba19dff8006
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a145a103620d23dae4f6a48c225251e8aecc278e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593669"
---
# <a name="pidlidtaskactualeffort-canonical-property"></a><span data-ttu-id="2b0be-103">PidLidTaskActualEffort (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2b0be-103">PidLidTaskActualEffort Canonical Property</span></span>

  
  
<span data-ttu-id="2b0be-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b0be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b0be-105">Gibt die Anzahl von Minuten an, dass der Benutzer eine Aufgabe ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2b0be-105">Indicates the number of minutes that the user performed a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2b0be-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2b0be-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2b0be-107">dispidTaskActualEffort</span><span class="sxs-lookup"><span data-stu-id="2b0be-107">dispidTaskActualEffort</span></span>  <br/> |
|<span data-ttu-id="2b0be-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="2b0be-108">Property set:</span></span>  <br/> |<span data-ttu-id="2b0be-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="2b0be-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="2b0be-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="2b0be-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2b0be-111">0x00008110</span><span class="sxs-lookup"><span data-stu-id="2b0be-111">0x00008110</span></span>  <br/> |
|<span data-ttu-id="2b0be-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="2b0be-112">Data type:</span></span>  <br/> |<span data-ttu-id="2b0be-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2b0be-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2b0be-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2b0be-114">Area:</span></span>  <br/> |<span data-ttu-id="2b0be-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="2b0be-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b0be-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="2b0be-116">Remarks</span></span>

<span data-ttu-id="2b0be-117">Der Wert muss größer als oder gleich 0 und kleiner als 0x5AE980DF (1,525,252,319), wobei gleich 480 Minuten eine Tag und 2400 Minuten gleich eine Woche (acht Stunden in einen Arbeitstag und fünf Tage in einer Arbeitswoche).</span><span class="sxs-lookup"><span data-stu-id="2b0be-117">The value must be greater than or equal to 0 and less than 0x5AE980DF (1,525,252,319), where 480 minutes equal one day and 2400 minutes equal one week (eight hours in a work day and five days in a work week).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2b0be-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2b0be-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2b0be-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="2b0be-119">Protocol specifications</span></span>

<span data-ttu-id="2b0be-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2b0be-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2b0be-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="2b0be-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2b0be-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2b0be-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2b0be-123">Gibt die Eigenschaften und Operationen, die für Kontakt- und Objekte in der persönlichen Verteilerliste Liste zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="2b0be-123">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2b0be-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="2b0be-124">Header files</span></span>

<span data-ttu-id="2b0be-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2b0be-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="2b0be-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="2b0be-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2b0be-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b0be-127">See also</span></span>



[<span data-ttu-id="2b0be-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2b0be-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2b0be-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2b0be-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2b0be-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2b0be-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2b0be-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2b0be-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

