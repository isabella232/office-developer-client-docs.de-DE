---
title: SPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropTagArray
api_type:
- COM
ms.assetid: 4a9e1579-bebe-4a51-8ced-6dba9c3bcb63
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5cfad1c75aaab9afae47de5798f9e6b7ea530940
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795609"
---
# <a name="sproptagarray"></a><span data-ttu-id="729fb-103">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="729fb-103">SPropTagArray</span></span>

  
  
<span data-ttu-id="729fb-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="729fb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="729fb-105">Enthält ein Array von Eigenschaftentags.</span><span class="sxs-lookup"><span data-stu-id="729fb-105">Contains an array of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="729fb-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="729fb-106">Header file:</span></span>  <br/> |<span data-ttu-id="729fb-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="729fb-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="729fb-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="729fb-108">Related macros:</span></span>  <br/> |<span data-ttu-id="729fb-109">[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md), [SizedSPropTagArray](sizedsproptagarray.md)</span><span class="sxs-lookup"><span data-stu-id="729fb-109">[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md), [SizedSPropTagArray](sizedsproptagarray.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropTagArray
{
  ULONG cValues;
  ULONG aulPropTag[MAPI_DIM];
} SPropTagArray, FAR *LPSPropTagArray;

```

## <a name="members"></a><span data-ttu-id="729fb-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="729fb-110">Members</span></span>

 <span data-ttu-id="729fb-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="729fb-111">**cValues**</span></span>
  
> <span data-ttu-id="729fb-112">Anzahl der Eigenschaftentags im Array vom **AulPropTag** Member angegeben.</span><span class="sxs-lookup"><span data-stu-id="729fb-112">Count of property tags in the array indicated by the **aulPropTag** member.</span></span> 
    
 <span data-ttu-id="729fb-113">**aulPropTag**</span><span class="sxs-lookup"><span data-stu-id="729fb-113">**aulPropTag**</span></span>
  
> <span data-ttu-id="729fb-114">Array von Eigenschaftentags.</span><span class="sxs-lookup"><span data-stu-id="729fb-114">Array of property tags.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="729fb-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="729fb-115">Remarks</span></span>

<span data-ttu-id="729fb-116">Ein Eigenschaftentag ist eine 32-Bit-Ganzzahl ohne Vorzeichen, die besteht aus zwei Teilen:</span><span class="sxs-lookup"><span data-stu-id="729fb-116">A property tag is a 32-bit unsigned integer that consists of two parts:</span></span> 
  
- <span data-ttu-id="729fb-117">Ein Bezeichner in der hohen 16 Bits.</span><span class="sxs-lookup"><span data-stu-id="729fb-117">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="729fb-118">Ein Typ in den niederwertige 16 Bit.</span><span class="sxs-lookup"><span data-stu-id="729fb-118">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="729fb-119">Der Bezeichner ist einen numerischen Wert in einem bestimmten Bereich.</span><span class="sxs-lookup"><span data-stu-id="729fb-119">The identifier is a numeric value in a particular range.</span></span> <span data-ttu-id="729fb-120">MAPI definiert Bereiche für Bezeichner zum Beschreiben der für die-Eigenschaft verwendet wird und die, die für die Verwaltung zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="729fb-120">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="729fb-121">MAPI definiert Einschränkungen für jede Eigenschaft Tags, die sie in der Headerdatei Mapitags.h unterstützt.</span><span class="sxs-lookup"><span data-stu-id="729fb-121">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="729fb-122">Der Typ gibt das Format für den Wert der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="729fb-122">The type indicates the format for the property's value.</span></span> <span data-ttu-id="729fb-123">MAPI definiert Konstanten für jede Eigenschaftentypen, die in der Headerdatei Mapidefs.h unterstützt.</span><span class="sxs-lookup"><span data-stu-id="729fb-123">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="729fb-124">Weitere Informationen zu Eigenschaftentags und deren Komponenten finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="729fb-124">For more information about property tags and their components, see one of the following topics:</span></span> 
  
[<span data-ttu-id="729fb-125">MAPI-Eigenschaftentags</span><span class="sxs-lookup"><span data-stu-id="729fb-125">MAPI Property Tags</span></span>](mapi-property-tags.md)
  
[<span data-ttu-id="729fb-126">Übersicht über die Bezeichner des MAPI-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="729fb-126">MAPI Property Identifier Overview</span></span>](mapi-property-identifier-overview.md)
  
[<span data-ttu-id="729fb-127">Übersicht über Typ von MAPI-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="729fb-127">MAPI Property Type Overview</span></span>](mapi-property-type-overview.md)
  
<span data-ttu-id="729fb-128">Eine vollständige Liste der Eigenschaftentypen einwertige und mehrwertige finden Sie im Anhang, [Eigenschaftenbezeichner und Typen](property-identifiers-and-types.md).</span><span class="sxs-lookup"><span data-stu-id="729fb-128">For a complete list of the single-valued and multi-valued property types, see the appendix, [Property Identifiers and Types](property-identifiers-and-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="729fb-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="729fb-129">See also</span></span>



[<span data-ttu-id="729fb-130">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="729fb-130">MAPI Structures</span></span>](mapi-structures.md)

