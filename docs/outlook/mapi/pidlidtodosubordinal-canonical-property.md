---
title: PidLidToDoSubOrdinal (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoSubOrdinal
api_type:
- COM
ms.assetid: e3bc15ef-155e-49fd-88e5-64713df9b939
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c4ea125a5bde89e0885be4c04e3f106f202b1e18
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384563"
---
# <a name="pidlidtodosubordinal-canonical-property"></a><span data-ttu-id="7b749-103">PidLidToDoSubOrdinal (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7b749-103">PidLidToDoSubOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="7b749-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b749-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b749-105">Fungiert als eine Tie wörtertrennung, wenn die Eigenschaft **DispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) Objekte und das Ergebnis in einer Gleichwertigkeit sortiert.</span><span class="sxs-lookup"><span data-stu-id="7b749-105">Acts as a tie breaker when the **dispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) property sorts objects and the result in a tie.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7b749-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7b749-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7b749-107">dispidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="7b749-107">dispidToDoSubOrdinal</span></span>  <br/> |
|<span data-ttu-id="7b749-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="7b749-108">Property set:</span></span>  <br/> |<span data-ttu-id="7b749-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="7b749-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="7b749-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="7b749-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7b749-111">0x000085A1</span><span class="sxs-lookup"><span data-stu-id="7b749-111">0x000085A1</span></span>  <br/> |
|<span data-ttu-id="7b749-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7b749-112">Data type:</span></span>  <br/> |<span data-ttu-id="7b749-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7b749-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7b749-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7b749-114">Area:</span></span>  <br/> |<span data-ttu-id="7b749-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="7b749-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b749-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7b749-116">Remarks</span></span>

<span data-ttu-id="7b749-117">Wenn verwendet, muss diese Eigenschaft lexikografisch sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="7b749-117">If used, this property must be sorted lexicographically.</span></span> <span data-ttu-id="7b749-118">Die Komponente Zeichen der Zeichenfolge darf nur die Ziffern 0 bis 9 bestehen.</span><span class="sxs-lookup"><span data-stu-id="7b749-118">The component characters of the string must consist of only the numerals zero through nine.</span></span> <span data-ttu-id="7b749-119">Diese Eigenschaft sollte anfänglich auf "5555555" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7b749-119">This property should be initially set to "5555555".</span></span> <span data-ttu-id="7b749-120">Die Länge dieser Eigenschaft muss (mit Ausnahme der abschließenden NULL-Zeichens) 254 Zeichen nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="7b749-120">The length of this property must not exceed 254 characters (excluding the terminating NULL character).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7b749-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7b749-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7b749-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="7b749-122">Protocol specifications</span></span>

<span data-ttu-id="7b749-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b749-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b749-124">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="7b749-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7b749-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b749-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b749-126">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="7b749-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7b749-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="7b749-127">Header files</span></span>

<span data-ttu-id="7b749-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7b749-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="7b749-129">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7b749-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7b749-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b749-130">See also</span></span>



[<span data-ttu-id="7b749-131">PidLidToDoOrdinalDate (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7b749-131">PidLidToDoOrdinalDate Canonical Property</span></span>](pidlidtodoordinaldate-canonical-property.md)


[<span data-ttu-id="7b749-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7b749-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7b749-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7b749-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7b749-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7b749-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7b749-135">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7b749-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

