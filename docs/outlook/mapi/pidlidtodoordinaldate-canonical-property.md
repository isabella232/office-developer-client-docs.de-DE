---
title: Kanonische Pidlidtodoordinaldate (-Eigenschaft
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
ms.openlocfilehash: b0c5e3019efeeb0b9788d81e8730e976bfcc9d75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345276"
---
# <a name="pidlidtodoordinaldate-canonical-property"></a><span data-ttu-id="12c00-103">Kanonische Pidlidtodoordinaldate (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="12c00-103">PidLidToDoOrdinalDate Canonical Property</span></span>

  
  
<span data-ttu-id="12c00-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12c00-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12c00-105">Bestimmt die Sortierreihenfolge von Objekten in einer konsolidierten Aufgabenliste.</span><span class="sxs-lookup"><span data-stu-id="12c00-105">Determines the sort order of objects in a consolidated to-do list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="12c00-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="12c00-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="12c00-107">dispidToDoOrdinalDate</span><span class="sxs-lookup"><span data-stu-id="12c00-107">dispidToDoOrdinalDate</span></span>  <br/> |
|<span data-ttu-id="12c00-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="12c00-108">Property set:</span></span>  <br/> |<span data-ttu-id="12c00-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="12c00-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="12c00-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="12c00-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="12c00-111">0x000085A0</span><span class="sxs-lookup"><span data-stu-id="12c00-111">0x000085A0</span></span>  <br/> |
|<span data-ttu-id="12c00-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="12c00-112">Data type:</span></span>  <br/> |<span data-ttu-id="12c00-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="12c00-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="12c00-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="12c00-114">Area:</span></span>  <br/> |<span data-ttu-id="12c00-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="12c00-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12c00-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12c00-116">Remarks</span></span>

<span data-ttu-id="12c00-117">Wenn ein Objekt gekennzeichnet wird, sollte diese Eigenschaft auf die aktuelle Uhrzeit in koordinierter weltZeit (UTC) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="12c00-117">When an object is flagged, this property should be set to the current time in Coordinated Universal Time (UTC).</span></span> 
  
<span data-ttu-id="12c00-118">Wenn der Client es einem Benutzer ermöglicht, Vorgänge innerhalb der konsolidierten Aufgabenliste per Drag & Drop neu anordnen zu können, kann er einen beliebigen geeigneten Algorithmus verwenden, um den neuen Wert dieser Eigenschaft zu bestimmen, sodass die Aufgabe an der richtigen Stelle angezeigt wird, wenn diese Eigenschaft als Sor verwendet wird. Ting-Feld.</span><span class="sxs-lookup"><span data-stu-id="12c00-118">If the client allows a user to reorder tasks within the consolidated task list via dragging or other mechanisms, they can use any suitable algorithm to determine the new value of this property so that the task appears in the correct place when this property is used as a sorting field.</span></span>
  
<span data-ttu-id="12c00-119">Wenn diese Eigenschaft verwendet wird, um Objekte und die Sortierergebnisse in einem tie zu sortieren, wird die **dispidToDoSubOrdinal** ([pidlidtodosubordinal (](pidlidtodosubordinal-canonical-property.md))-Eigenschaft als Tie-Breaker verwendet.</span><span class="sxs-lookup"><span data-stu-id="12c00-119">When this property is used to sort objects and the sort results in a tie, the **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) property is used as a tie breaker.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="12c00-120">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="12c00-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="12c00-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="12c00-121">Protocol specifications</span></span>

<span data-ttu-id="12c00-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="12c00-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="12c00-123">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="12c00-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="12c00-124">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="12c00-124">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="12c00-125">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Markierung an.</span><span class="sxs-lookup"><span data-stu-id="12c00-125">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="12c00-126">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="12c00-126">Header files</span></span>

<span data-ttu-id="12c00-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="12c00-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="12c00-128">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="12c00-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="12c00-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12c00-129">See also</span></span>



[<span data-ttu-id="12c00-130">Kanonische Pidlidtodosubordinal (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="12c00-130">PidLidToDoSubOrdinal Canonical Property</span></span>](pidlidtodosubordinal-canonical-property.md)


[<span data-ttu-id="12c00-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="12c00-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="12c00-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="12c00-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="12c00-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="12c00-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="12c00-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="12c00-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

