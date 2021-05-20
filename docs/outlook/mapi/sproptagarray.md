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
ms.openlocfilehash: 9a5be98298ab1f9333ac1c223a6ef594e60dd86a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430700"
---
# <a name="sproptagarray"></a><span data-ttu-id="bfc7e-103">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="bfc7e-103">SPropTagArray</span></span>

  
  
<span data-ttu-id="bfc7e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bfc7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bfc7e-105">Enthält ein Array von Eigenschaftstags.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-105">Contains an array of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bfc7e-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="bfc7e-106">Header file:</span></span>  <br/> |<span data-ttu-id="bfc7e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bfc7e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="bfc7e-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="bfc7e-108">Related macros:</span></span>  <br/> |<span data-ttu-id="bfc7e-109">[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md), [SizedSPropTagArray](sizedsproptagarray.md)</span><span class="sxs-lookup"><span data-stu-id="bfc7e-109">[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md), [SizedSPropTagArray](sizedsproptagarray.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropTagArray
{
  ULONG cValues;
  ULONG aulPropTag[MAPI_DIM];
} SPropTagArray, FAR *LPSPropTagArray;

```

## <a name="members"></a><span data-ttu-id="bfc7e-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="bfc7e-110">Members</span></span>

 <span data-ttu-id="bfc7e-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="bfc7e-111">**cValues**</span></span>
  
> <span data-ttu-id="bfc7e-112">Anzahl der Eigenschaftstags im Array, das vom **aulPropTag-Element angegeben** wird.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-112">Count of property tags in the array indicated by the **aulPropTag** member.</span></span> 
    
 <span data-ttu-id="bfc7e-113">**aulPropTag**</span><span class="sxs-lookup"><span data-stu-id="bfc7e-113">**aulPropTag**</span></span>
  
> <span data-ttu-id="bfc7e-114">Array von Eigenschaftstags.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-114">Array of property tags.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bfc7e-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bfc7e-115">Remarks</span></span>

<span data-ttu-id="bfc7e-116">Ein Eigenschaftstag ist eine 32-Bit-Ganzzahl ohne Vorzeichen, die aus zwei Teilen besteht:</span><span class="sxs-lookup"><span data-stu-id="bfc7e-116">A property tag is a 32-bit unsigned integer that consists of two parts:</span></span> 
  
- <span data-ttu-id="bfc7e-117">Ein Bezeichner in der hohen Reihenfolge von 16 Bit.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-117">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="bfc7e-118">Ein Typ in niedriger Reihenfolge von 16 Bit.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-118">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="bfc7e-119">Der Bezeichner ist ein numerischer Wert in einem bestimmten Bereich.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-119">The identifier is a numeric value in a particular range.</span></span> <span data-ttu-id="bfc7e-120">MAPI definiert Bereiche für Bezeichner, um zu beschreiben, wofür die Eigenschaft verwendet wird und wer für die Verwaltung verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-120">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="bfc7e-121">MAPI definiert Einschränkungen für jedes der Eigenschaftentags, die es in der Mapitags.h-Headerdatei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-121">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="bfc7e-122">Der Typ gibt das Format für den Wert der Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-122">The type indicates the format for the property's value.</span></span> <span data-ttu-id="bfc7e-123">MAPI definiert Konstanten für jeden der Eigenschaftentypen, die in der Mapidefs.h-Headerdatei unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="bfc7e-123">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="bfc7e-124">Weitere Informationen zu Eigenschaftstags und deren Komponenten finden Sie in einem der folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="bfc7e-124">For more information about property tags and their components, see one of the following topics:</span></span> 
  
[<span data-ttu-id="bfc7e-125">MAPI-Eigenschaftstags</span><span class="sxs-lookup"><span data-stu-id="bfc7e-125">MAPI Property Tags</span></span>](mapi-property-tags.md)
  
[<span data-ttu-id="bfc7e-126">Übersicht über die MAPI-Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="bfc7e-126">MAPI Property Identifier Overview</span></span>](mapi-property-identifier-overview.md)
  
[<span data-ttu-id="bfc7e-127">Übersicht über den MAPI-Eigenschaftstyp</span><span class="sxs-lookup"><span data-stu-id="bfc7e-127">MAPI Property Type Overview</span></span>](mapi-property-type-overview.md)
  
<span data-ttu-id="bfc7e-128">Eine vollständige Liste der einwertigen und mehrwertigen Eigenschaftentypen finden Sie im Anhang, [Property Identifiers und Types](property-identifiers-and-types.md).</span><span class="sxs-lookup"><span data-stu-id="bfc7e-128">For a complete list of the single-valued and multi-valued property types, see the appendix, [Property Identifiers and Types](property-identifiers-and-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bfc7e-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfc7e-129">See also</span></span>



[<span data-ttu-id="bfc7e-130">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="bfc7e-130">MAPI Structures</span></span>](mapi-structures.md)

