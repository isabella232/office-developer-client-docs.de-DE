---
title: Kanonische PidLidToDoOrdinalDate-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoOrdinalDate
api_type:
- COM
ms.assetid: b6a500fc-07f4-4788-ae46-d179a96a48e2
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d708424ccb15be15746fe8a33eea73a8e0f99323
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793876"
---
# <a name="pidlidtodoordinaldate-canonical-property"></a><span data-ttu-id="982eb-103">Kanonische PidLidToDoOrdinalDate-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="982eb-103">PidLidToDoOrdinalDate Canonical Property</span></span>

  
  
<span data-ttu-id="982eb-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="982eb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="982eb-105">Bestimmt die Sortierreihenfolge der Objekte in einer konsolidierten Aufgabenliste.</span><span class="sxs-lookup"><span data-stu-id="982eb-105">Determines the sort order of objects in a consolidated to-do list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="982eb-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="982eb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="982eb-107">dispidToDoOrdinalDate</span><span class="sxs-lookup"><span data-stu-id="982eb-107">dispidToDoOrdinalDate</span></span>  <br/> |
|<span data-ttu-id="982eb-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="982eb-108">Property set:</span></span>  <br/> |<span data-ttu-id="982eb-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="982eb-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="982eb-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="982eb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="982eb-111">0x000085A0</span><span class="sxs-lookup"><span data-stu-id="982eb-111">0x000085A0</span></span>  <br/> |
|<span data-ttu-id="982eb-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="982eb-112">Data type:</span></span>  <br/> |<span data-ttu-id="982eb-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="982eb-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="982eb-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="982eb-114">Area:</span></span>  <br/> |<span data-ttu-id="982eb-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="982eb-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="982eb-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="982eb-116">Remarks</span></span>

<span data-ttu-id="982eb-117">Wenn ein Objekt gekennzeichnet ist, muss diese Eigenschaft auf die aktuelle Zeit in koordinierter Weltzeit (UTC) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="982eb-117">When an object is flagged, this property should be set to the current time in Coordinated Universal Time (UTC).</span></span> 
  
<span data-ttu-id="982eb-118">Wenn der Client Benutzern das Neuanordnen von Aufgaben in der konsolidierten Aufgabenliste ermöglicht durch Ziehen oder andere Mechanismen, können sie alle geeigneten Algorithmus Sie den neuen Wert dieser Eigenschaft ermitteln, damit die Aufgabe an der richtigen Stelle angezeigt wird, wenn diese Eigenschaft als ein Sor verwendet wird Ting dar.</span><span class="sxs-lookup"><span data-stu-id="982eb-118">If the client allows a user to reorder tasks within the consolidated task list via dragging or other mechanisms, they can use any suitable algorithm to determine the new value of this property so that the task appears in the correct place when this property is used as a sorting field.</span></span>
  
<span data-ttu-id="982eb-119">Wenn diese Eigenschaft sortiert Objekte und die Ergebnisse in einer Gleichwertigkeit Sortieren verwendet wird, wird die Eigenschaft **DispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) als eine Tie wörtertrennung verwendet.</span><span class="sxs-lookup"><span data-stu-id="982eb-119">When this property is used to sort objects and the sort results in a tie, the **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) property is used as a tie breaker.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="982eb-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="982eb-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="982eb-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="982eb-121">Protocol specifications</span></span>

<span data-ttu-id="982eb-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="982eb-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="982eb-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="982eb-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="982eb-124">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="982eb-124">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="982eb-125">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="982eb-125">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="982eb-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="982eb-126">Header files</span></span>

<span data-ttu-id="982eb-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="982eb-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="982eb-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="982eb-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="982eb-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="982eb-129">See also</span></span>



[<span data-ttu-id="982eb-130">Kanonische PidLidToDoSubOrdinal-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="982eb-130">PidLidToDoSubOrdinal Canonical Property</span></span>](pidlidtodosubordinal-canonical-property.md)


[<span data-ttu-id="982eb-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="982eb-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="982eb-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="982eb-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="982eb-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="982eb-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="982eb-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="982eb-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

