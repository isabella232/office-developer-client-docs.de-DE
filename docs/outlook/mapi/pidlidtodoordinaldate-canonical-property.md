---
title: PidLidToDoOrdinalDate (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b0c5e3019efeeb0b9788d81e8730e976bfcc9d75
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401587"
---
# <a name="pidlidtodoordinaldate-canonical-property"></a><span data-ttu-id="4b217-103">PidLidToDoOrdinalDate (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4b217-103">PidLidToDoOrdinalDate Canonical Property</span></span>

  
  
<span data-ttu-id="4b217-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b217-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b217-105">Bestimmt die Sortierreihenfolge der Objekte in einer konsolidierten Aufgabenliste.</span><span class="sxs-lookup"><span data-stu-id="4b217-105">Determines the sort order of objects in a consolidated to-do list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4b217-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4b217-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4b217-107">dispidToDoOrdinalDate</span><span class="sxs-lookup"><span data-stu-id="4b217-107">dispidToDoOrdinalDate</span></span>  <br/> |
|<span data-ttu-id="4b217-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="4b217-108">Property set:</span></span>  <br/> |<span data-ttu-id="4b217-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="4b217-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="4b217-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="4b217-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4b217-111">0x000085A0</span><span class="sxs-lookup"><span data-stu-id="4b217-111">0x000085A0</span></span>  <br/> |
|<span data-ttu-id="4b217-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4b217-112">Data type:</span></span>  <br/> |<span data-ttu-id="4b217-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="4b217-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="4b217-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4b217-114">Area:</span></span>  <br/> |<span data-ttu-id="4b217-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="4b217-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4b217-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4b217-116">Remarks</span></span>

<span data-ttu-id="4b217-117">Wenn ein Objekt gekennzeichnet ist, muss diese Eigenschaft auf die aktuelle Zeit in koordinierter Weltzeit (UTC) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4b217-117">When an object is flagged, this property should be set to the current time in Coordinated Universal Time (UTC).</span></span> 
  
<span data-ttu-id="4b217-118">Wenn der Client Benutzern das Neuanordnen von Aufgaben in der konsolidierten Aufgabenliste ermöglicht durch Ziehen oder andere Mechanismen, können sie alle geeigneten Algorithmus Sie den neuen Wert dieser Eigenschaft ermitteln, damit die Aufgabe an der richtigen Stelle angezeigt wird, wenn diese Eigenschaft als ein Sor verwendet wird Ting dar.</span><span class="sxs-lookup"><span data-stu-id="4b217-118">If the client allows a user to reorder tasks within the consolidated task list via dragging or other mechanisms, they can use any suitable algorithm to determine the new value of this property so that the task appears in the correct place when this property is used as a sorting field.</span></span>
  
<span data-ttu-id="4b217-119">Wenn diese Eigenschaft sortiert Objekte und die Ergebnisse in einer Gleichwertigkeit Sortieren verwendet wird, wird die Eigenschaft **DispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) als eine Tie wörtertrennung verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b217-119">When this property is used to sort objects and the sort results in a tie, the **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) property is used as a tie breaker.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4b217-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4b217-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4b217-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="4b217-121">Protocol specifications</span></span>

<span data-ttu-id="4b217-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b217-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b217-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="4b217-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4b217-124">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b217-124">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b217-125">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="4b217-125">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4b217-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="4b217-126">Header files</span></span>

<span data-ttu-id="4b217-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4b217-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="4b217-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="4b217-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4b217-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b217-129">See also</span></span>



[<span data-ttu-id="4b217-130">PidLidToDoSubOrdinal (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4b217-130">PidLidToDoSubOrdinal Canonical Property</span></span>](pidlidtodosubordinal-canonical-property.md)


[<span data-ttu-id="4b217-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4b217-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4b217-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4b217-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4b217-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4b217-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4b217-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4b217-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

