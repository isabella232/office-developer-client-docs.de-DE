---
title: PROP_TAG
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_TAG
api_type:
- COM
ms.assetid: d8c9d18c-4043-41f3-8501-8be8e3a2c9ac
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9e53c39b713aa782eb387b85667f5ded6193006f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795305"
---
# <a name="proptag"></a><span data-ttu-id="e0477-103">PROP_TAG</span><span class="sxs-lookup"><span data-stu-id="e0477-103">PROP_TAG</span></span>

<span data-ttu-id="e0477-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e0477-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e0477-105">Gibt eine Eigenschaftentag erstellt durch die Kombination einer angegebenen Eigenschaftentyp und Bezeichner zurück.</span><span class="sxs-lookup"><span data-stu-id="e0477-105">Returns a property tag created by combining a specified property type and identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e0477-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="e0477-106">Header file:</span></span>  <br/> |<span data-ttu-id="e0477-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e0477-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e0477-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="e0477-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="e0477-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="e0477-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TAG (ulPropType, ulPropID)
```

## <a name="parameters"></a><span data-ttu-id="e0477-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0477-110">Parameters</span></span>

<span data-ttu-id="e0477-111">_ulPropType_</span><span class="sxs-lookup"><span data-stu-id="e0477-111">_ulPropType_</span></span>
  
> <span data-ttu-id="e0477-112">Der Eigenschaftentyp für die neue Eigenschaftentag.</span><span class="sxs-lookup"><span data-stu-id="e0477-112">Property type for the new property tag.</span></span>
    
<span data-ttu-id="e0477-113">_ulPropID_</span><span class="sxs-lookup"><span data-stu-id="e0477-113">_ulPropID_</span></span>
  
> <span data-ttu-id="e0477-114">Der Bezeichner für die neue Eigenschaftentag.</span><span class="sxs-lookup"><span data-stu-id="e0477-114">Property identifier for the new property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e0477-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e0477-115">Remarks</span></span>

<span data-ttu-id="e0477-116">Die **Eigenschaft\_TAG** Makro erstellt eine Eigenschaftentag für eine Eigenschaft vom Typ _UlPropType_ und die Kennung, die in _UlPropID_angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e0477-116">The **PROP\_TAG** macro creates a property tag for a property of type  _ulPropType_ and the identifier that is specified in  _ulPropID_.</span></span> <span data-ttu-id="e0477-117">Beispielsweise kann eine Eigenschaftentag für eine Eintrags-ID mit dem Makro **PROP_TAG** wie folgt erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="e0477-117">For example, a property tag for an entry identifier can be created by using the **PROP_TAG** macro as follows:</span></span> 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

<span data-ttu-id="e0477-118">Die niederwertige 16 Bit des Tags zurückgegebene Eigenschaft enthalten den Eigenschaftentyp PT_BINARY, und die obere 16 Bit der Eigenschaftenbezeichner 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="e0477-118">The low-order 16 bits of the returned property tag contain the property type, PT_BINARY, and the high-order 16 bits contain the property identifier, 0xFFFF.</span></span>
  
<span data-ttu-id="e0477-119">Weitere Informationen zu Eigenschaftentags finden Sie unter [MAPI-Eigenschaftentags](mapi-property-tags.md).</span><span class="sxs-lookup"><span data-stu-id="e0477-119">For more information about property tags, see [MAPI Property Tags](mapi-property-tags.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e0477-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0477-120">See also</span></span>

- [<span data-ttu-id="e0477-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="e0477-121">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="e0477-122">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="e0477-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

