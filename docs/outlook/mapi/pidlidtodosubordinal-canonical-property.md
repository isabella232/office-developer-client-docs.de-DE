---
title: Kanonische Pidlidtodosubordinal (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c4ea125a5bde89e0885be4c04e3f106f202b1e18
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344919"
---
# <a name="pidlidtodosubordinal-canonical-property"></a><span data-ttu-id="a9820-103">Kanonische Pidlidtodosubordinal (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a9820-103">PidLidToDoSubOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="a9820-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9820-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9820-105">Fungiert als Tie-Breaker, wenn die **dispidToDoOrdinalDate** ([pidlidtodoordinaldate (](pidlidtodoordinaldate-canonical-property.md))-Eigenschaft Objekte und das Ergebnis in einem Unentschieden sortiert.</span><span class="sxs-lookup"><span data-stu-id="a9820-105">Acts as a tie breaker when the **dispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) property sorts objects and the result in a tie.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a9820-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a9820-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a9820-107">dispidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="a9820-107">dispidToDoSubOrdinal</span></span>  <br/> |
|<span data-ttu-id="a9820-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="a9820-108">Property set:</span></span>  <br/> |<span data-ttu-id="a9820-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="a9820-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="a9820-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="a9820-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a9820-111">0x000085A1</span><span class="sxs-lookup"><span data-stu-id="a9820-111">0x000085A1</span></span>  <br/> |
|<span data-ttu-id="a9820-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a9820-112">Data type:</span></span>  <br/> |<span data-ttu-id="a9820-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a9820-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a9820-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a9820-114">Area:</span></span>  <br/> |<span data-ttu-id="a9820-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="a9820-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9820-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9820-116">Remarks</span></span>

<span data-ttu-id="a9820-117">Wenn diese Eigenschaft verwendet wird, muss Sie lexikografisch sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="a9820-117">If used, this property must be sorted lexicographically.</span></span> <span data-ttu-id="a9820-118">Die Komponentenzeichen der Zeichenfolge müssen nur aus den Ziffern 0 bis 9 bestehen.</span><span class="sxs-lookup"><span data-stu-id="a9820-118">The component characters of the string must consist of only the numerals zero through nine.</span></span> <span data-ttu-id="a9820-119">Diese Eigenschaft sollte anfänglich auf "5555555" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a9820-119">This property should be initially set to "5555555".</span></span> <span data-ttu-id="a9820-120">Die Länge dieser Eigenschaft darf 254 Zeichen nicht überschreiten (ohne das abschließende NULL-Zeichen).</span><span class="sxs-lookup"><span data-stu-id="a9820-120">The length of this property must not exceed 254 characters (excluding the terminating NULL character).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a9820-121">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a9820-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a9820-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a9820-122">Protocol specifications</span></span>

<span data-ttu-id="a9820-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a9820-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a9820-124">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="a9820-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a9820-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a9820-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a9820-126">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Markierung an.</span><span class="sxs-lookup"><span data-stu-id="a9820-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a9820-127">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="a9820-127">Header files</span></span>

<span data-ttu-id="a9820-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a9820-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="a9820-129">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="a9820-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a9820-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9820-130">See also</span></span>



[<span data-ttu-id="a9820-131">Kanonische Pidlidtodoordinaldate (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a9820-131">PidLidToDoOrdinalDate Canonical Property</span></span>](pidlidtodoordinaldate-canonical-property.md)


[<span data-ttu-id="a9820-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a9820-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a9820-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a9820-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a9820-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a9820-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a9820-135">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a9820-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

