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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9a5be98298ab1f9333ac1c223a6ef594e60dd86a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344436"
---
# <a name="sproptagarray"></a><span data-ttu-id="822a3-103">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="822a3-103">SPropTagArray</span></span>

  
  
<span data-ttu-id="822a3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="822a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="822a3-105">Enthält ein Array von Property-Tags.</span><span class="sxs-lookup"><span data-stu-id="822a3-105">Contains an array of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="822a3-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="822a3-106">Header file:</span></span>  <br/> |<span data-ttu-id="822a3-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="822a3-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="822a3-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="822a3-108">Related macros:</span></span>  <br/> |<span data-ttu-id="822a3-109">[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md), [SizedSPropTagArray](sizedsproptagarray.md)</span><span class="sxs-lookup"><span data-stu-id="822a3-109">[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md), [SizedSPropTagArray](sizedsproptagarray.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropTagArray
{
  ULONG cValues;
  ULONG aulPropTag[MAPI_DIM];
} SPropTagArray, FAR *LPSPropTagArray;

```

## <a name="members"></a><span data-ttu-id="822a3-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="822a3-110">Members</span></span>

 <span data-ttu-id="822a3-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="822a3-111">**cValues**</span></span>
  
> <span data-ttu-id="822a3-112">Die Anzahl der Eigenschaftstags im vom **aulPropTag** -Element angegebenen Array.</span><span class="sxs-lookup"><span data-stu-id="822a3-112">Count of property tags in the array indicated by the **aulPropTag** member.</span></span> 
    
 <span data-ttu-id="822a3-113">**aulPropTag**</span><span class="sxs-lookup"><span data-stu-id="822a3-113">**aulPropTag**</span></span>
  
> <span data-ttu-id="822a3-114">Array von Property-Tags.</span><span class="sxs-lookup"><span data-stu-id="822a3-114">Array of property tags.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="822a3-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="822a3-115">Remarks</span></span>

<span data-ttu-id="822a3-116">Ein Property-Tag ist eine 32-Bit-Ganzzahl ohne Vorzeichen, die aus zwei Teilen besteht:</span><span class="sxs-lookup"><span data-stu-id="822a3-116">A property tag is a 32-bit unsigned integer that consists of two parts:</span></span> 
  
- <span data-ttu-id="822a3-117">Ein Bezeichner in den hochwertigen 16 Bits.</span><span class="sxs-lookup"><span data-stu-id="822a3-117">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="822a3-118">Ein Typ in den niederwertigen 16 Bits.</span><span class="sxs-lookup"><span data-stu-id="822a3-118">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="822a3-119">Der Bezeichner ist ein numerischer Wert in einem bestimmten Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="822a3-119">The identifier is a numeric value in a particular range.</span></span> <span data-ttu-id="822a3-120">MAPI definiert Bereiche für Bezeichner, um zu beschreiben, wofür die Eigenschaft verwendet wird und wer für deren Verwaltung zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="822a3-120">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="822a3-121">MAPI definiert Einschränkungen für die einzelnen Eigenschaftentags, die in der Headerdatei Mapitags. h unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="822a3-121">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="822a3-122">Der Typ gibt das Format für den Wert der Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="822a3-122">The type indicates the format for the property's value.</span></span> <span data-ttu-id="822a3-123">MAPI definiert Konstanten für alle Eigenschaftentypen, die in der Headerdatei Mapidefs. h unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="822a3-123">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="822a3-124">Weitere Informationen zu Eigenschaftstags und ihren Komponenten finden Sie in einem der folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="822a3-124">For more information about property tags and their components, see one of the following topics:</span></span> 
  
[<span data-ttu-id="822a3-125">MAPI-Eigenschafts Tags</span><span class="sxs-lookup"><span data-stu-id="822a3-125">MAPI Property Tags</span></span>](mapi-property-tags.md)
  
[<span data-ttu-id="822a3-126">Übersicht über die MAPI-EigenschaftsKennung</span><span class="sxs-lookup"><span data-stu-id="822a3-126">MAPI Property Identifier Overview</span></span>](mapi-property-identifier-overview.md)
  
[<span data-ttu-id="822a3-127">Übersicht über die MAPI-EigenschaftsTypen</span><span class="sxs-lookup"><span data-stu-id="822a3-127">MAPI Property Type Overview</span></span>](mapi-property-type-overview.md)
  
<span data-ttu-id="822a3-128">Eine vollständige Liste der einwertigen und mehrwertigen Eigenschaftentypen finden Sie im Anhang, [Eigenschaftenbezeichner und-Typen](property-identifiers-and-types.md).</span><span class="sxs-lookup"><span data-stu-id="822a3-128">For a complete list of the single-valued and multi-valued property types, see the appendix, [Property Identifiers and Types](property-identifiers-and-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="822a3-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="822a3-129">See also</span></span>



[<span data-ttu-id="822a3-130">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="822a3-130">MAPI Structures</span></span>](mapi-structures.md)

