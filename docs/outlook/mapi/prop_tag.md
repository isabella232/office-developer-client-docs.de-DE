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
ms.openlocfilehash: 7ab4e4e9e51849037a91a071f16294cfdf10870c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328567"
---
# <a name="proptag"></a><span data-ttu-id="2448c-103">PROP_TAG</span><span class="sxs-lookup"><span data-stu-id="2448c-103">PROP_TAG</span></span>

<span data-ttu-id="2448c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2448c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2448c-105">Gibt ein Eigenschaftentag zurück, das durch Kombinieren eines angegebenen Eigenschaftentyps und Bezeichners erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="2448c-105">Returns a property tag created by combining a specified property type and identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2448c-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="2448c-106">Header file:</span></span>  <br/> |<span data-ttu-id="2448c-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2448c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2448c-108">Zugehörige Struktur:</span><span class="sxs-lookup"><span data-stu-id="2448c-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="2448c-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2448c-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TAG (ulPropType, ulPropID)
```

## <a name="parameters"></a><span data-ttu-id="2448c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2448c-110">Parameters</span></span>

<span data-ttu-id="2448c-111">_ulPropType_</span><span class="sxs-lookup"><span data-stu-id="2448c-111">_ulPropType_</span></span>
  
> <span data-ttu-id="2448c-112">Eigenschafts für das neue Property-Tag.</span><span class="sxs-lookup"><span data-stu-id="2448c-112">Property type for the new property tag.</span></span>
    
<span data-ttu-id="2448c-113">_ulPropID_</span><span class="sxs-lookup"><span data-stu-id="2448c-113">_ulPropID_</span></span>
  
> <span data-ttu-id="2448c-114">Eigenschaftenbezeichner für das neue Property-Tag.</span><span class="sxs-lookup"><span data-stu-id="2448c-114">Property identifier for the new property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2448c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2448c-115">Remarks</span></span>

<span data-ttu-id="2448c-116">Das **Prop\_-Tag** -Makro erstellt ein Property-Tag für eine Eigenschaft vom Typ _ulPropType_ und den in _ulPropID_angegebenen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="2448c-116">The **PROP\_TAG** macro creates a property tag for a property of type  _ulPropType_ and the identifier that is specified in  _ulPropID_.</span></span> <span data-ttu-id="2448c-117">Beispielsweise kann ein Property-Tag für eine Eintrags-ID wie folgt mithilfe des **PROP_TAG** -Makros erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="2448c-117">For example, a property tag for an entry identifier can be created by using the **PROP_TAG** macro as follows:</span></span> 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

<span data-ttu-id="2448c-118">Die niedrigwertigen 16 Bits des zurückgegebenen Property-Tags enthalten den Eigenschaftentyp PT_BINARY, und die hochwertigen 16 Bits enthalten den Eigenschaftenbezeichner 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="2448c-118">The low-order 16 bits of the returned property tag contain the property type, PT_BINARY, and the high-order 16 bits contain the property identifier, 0xFFFF.</span></span>
  
<span data-ttu-id="2448c-119">Weitere Informationen zu Eigenschaftstags finden Sie unter [MAPI property Tags](mapi-property-tags.md).</span><span class="sxs-lookup"><span data-stu-id="2448c-119">For more information about property tags, see [MAPI Property Tags](mapi-property-tags.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2448c-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2448c-120">See also</span></span>

- [<span data-ttu-id="2448c-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2448c-121">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="2448c-122">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="2448c-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

