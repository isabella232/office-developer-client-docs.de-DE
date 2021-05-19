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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344919"
---
# <a name="pidlidtodosubordinal-canonical-property"></a><span data-ttu-id="93c7b-103">PidLidToDoSubOrdinal (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="93c7b-103">PidLidToDoSubOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="93c7b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93c7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93c7b-105">Dient als Tie breaker, wenn die **dispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) -Eigenschaft Objekte sortiert und das Ergebnis in einer Bindung.</span><span class="sxs-lookup"><span data-stu-id="93c7b-105">Acts as a tie breaker when the **dispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) property sorts objects and the result in a tie.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="93c7b-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="93c7b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="93c7b-107">dispidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="93c7b-107">dispidToDoSubOrdinal</span></span>  <br/> |
|<span data-ttu-id="93c7b-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="93c7b-108">Property set:</span></span>  <br/> |<span data-ttu-id="93c7b-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="93c7b-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="93c7b-110">Lange ID (LID):</span><span class="sxs-lookup"><span data-stu-id="93c7b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="93c7b-111">0x000085A1</span><span class="sxs-lookup"><span data-stu-id="93c7b-111">0x000085A1</span></span>  <br/> |
|<span data-ttu-id="93c7b-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="93c7b-112">Data type:</span></span>  <br/> |<span data-ttu-id="93c7b-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="93c7b-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="93c7b-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="93c7b-114">Area:</span></span>  <br/> |<span data-ttu-id="93c7b-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="93c7b-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93c7b-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="93c7b-116">Remarks</span></span>

<span data-ttu-id="93c7b-117">Wenn diese Eigenschaft verwendet wird, muss sie lexikografiegrafisch sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="93c7b-117">If used, this property must be sorted lexicographically.</span></span> <span data-ttu-id="93c7b-118">Die Komponentenzeichen der Zeichenfolge dürfen nur aus den Ziffern Null bis neun bestehen.</span><span class="sxs-lookup"><span data-stu-id="93c7b-118">The component characters of the string must consist of only the numerals zero through nine.</span></span> <span data-ttu-id="93c7b-119">Diese Eigenschaft sollte zunächst auf "5555555" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="93c7b-119">This property should be initially set to "5555555".</span></span> <span data-ttu-id="93c7b-120">Die Länge dieser Eigenschaft darf 254 Zeichen nicht überschreiten (mit Ausnahme des endenden NULL-Zeichens).</span><span class="sxs-lookup"><span data-stu-id="93c7b-120">The length of this property must not exceed 254 characters (excluding the terminating NULL character).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="93c7b-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="93c7b-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="93c7b-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="93c7b-122">Protocol specifications</span></span>

<span data-ttu-id="93c7b-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93c7b-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93c7b-124">Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="93c7b-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="93c7b-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93c7b-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93c7b-126">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Kennzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="93c7b-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="93c7b-127">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="93c7b-127">Header files</span></span>

<span data-ttu-id="93c7b-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="93c7b-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="93c7b-129">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="93c7b-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="93c7b-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93c7b-130">See also</span></span>



[<span data-ttu-id="93c7b-131">PidLidToDoOrdinalDate (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="93c7b-131">PidLidToDoOrdinalDate Canonical Property</span></span>](pidlidtodoordinaldate-canonical-property.md)


[<span data-ttu-id="93c7b-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="93c7b-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="93c7b-133">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="93c7b-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="93c7b-134">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="93c7b-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="93c7b-135">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="93c7b-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

