---
title: Kanonische PidLidTaskActualEffort-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0782191010341019ebea71ebf545dec490521520
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793802"
---
# <a name="pidlidtaskactualeffort-canonical-property"></a><span data-ttu-id="0bd3e-103">Kanonische PidLidTaskActualEffort-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0bd3e-103">PidLidTaskActualEffort Canonical Property</span></span>

  
  
<span data-ttu-id="0bd3e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0bd3e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0bd3e-105">Gibt die Anzahl von Minuten an, dass der Benutzer eine Aufgabe ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0bd3e-105">Indicates the number of minutes that the user performed a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0bd3e-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0bd3e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0bd3e-107">dispidTaskActualEffort</span><span class="sxs-lookup"><span data-stu-id="0bd3e-107">dispidTaskActualEffort</span></span>  <br/> |
|<span data-ttu-id="0bd3e-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="0bd3e-108">Property set:</span></span>  <br/> |<span data-ttu-id="0bd3e-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="0bd3e-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="0bd3e-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="0bd3e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0bd3e-111">0x00008110</span><span class="sxs-lookup"><span data-stu-id="0bd3e-111">0x00008110</span></span>  <br/> |
|<span data-ttu-id="0bd3e-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0bd3e-112">Data type:</span></span>  <br/> |<span data-ttu-id="0bd3e-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0bd3e-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0bd3e-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0bd3e-114">Area:</span></span>  <br/> |<span data-ttu-id="0bd3e-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="0bd3e-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0bd3e-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0bd3e-116">Remarks</span></span>

<span data-ttu-id="0bd3e-117">Der Wert muss größer als oder gleich 0 und kleiner als 0x5AE980DF (1,525,252,319), wobei gleich 480 Minuten eine Tag und 2400 Minuten gleich eine Woche (acht Stunden in einen Arbeitstag und fünf Tage in einer Arbeitswoche).</span><span class="sxs-lookup"><span data-stu-id="0bd3e-117">The value must be greater than or equal to 0 and less than 0x5AE980DF (1,525,252,319), where 480 minutes equal one day and 2400 minutes equal one week (eight hours in a work day and five days in a work week).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0bd3e-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0bd3e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0bd3e-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0bd3e-119">Protocol specifications</span></span>

<span data-ttu-id="0bd3e-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0bd3e-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0bd3e-121">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="0bd3e-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0bd3e-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0bd3e-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0bd3e-123">Gibt die Eigenschaften und Operationen, die für Kontakt- und Objekte in der persönlichen Verteilerliste Liste zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="0bd3e-123">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0bd3e-124">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="0bd3e-124">Header files</span></span>

<span data-ttu-id="0bd3e-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0bd3e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="0bd3e-126">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0bd3e-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0bd3e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0bd3e-127">See also</span></span>



[<span data-ttu-id="0bd3e-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0bd3e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0bd3e-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0bd3e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0bd3e-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0bd3e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0bd3e-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0bd3e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

