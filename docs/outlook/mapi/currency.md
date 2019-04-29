---
title: CURRENCY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CURRENCY
api_type:
- COM
ms.assetid: cffc05a0-95e4-4b9f-bf8f-c4272a75afa8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dccb6b19af72d0f748a3a513b7f3d78904ebc789
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431120"
---
# <a name="currency"></a><span data-ttu-id="2756e-103">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="2756e-103">CURRENCY</span></span>

  
  
<span data-ttu-id="2756e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2756e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2756e-105">Enthält eine signierte 64-Bit-Ganzzahl, die einen Währungswert darstellt.</span><span class="sxs-lookup"><span data-stu-id="2756e-105">Contains a signed 64-bit integer representing a currency value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2756e-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="2756e-106">Header file:</span></span>  <br/> |<span data-ttu-id="2756e-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2756e-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct tagCY
{
  unsigned long Lo;
  long Hi;
} CURRENCY;

```

## <a name="members"></a><span data-ttu-id="2756e-108">Members</span><span class="sxs-lookup"><span data-stu-id="2756e-108">Members</span></span>

 <span data-ttu-id="2756e-109">**Lo**</span><span class="sxs-lookup"><span data-stu-id="2756e-109">**Lo**</span></span>
  
> <span data-ttu-id="2756e-110">Low-Order 32 Bits des Currency-Werts.</span><span class="sxs-lookup"><span data-stu-id="2756e-110">Low-order 32 bits of the currency value.</span></span> 
    
 <span data-ttu-id="2756e-111">**Hallo**</span><span class="sxs-lookup"><span data-stu-id="2756e-111">**Hi**</span></span>
  
> <span data-ttu-id="2756e-112">High-Order 32 Bits des Currency-Werts.</span><span class="sxs-lookup"><span data-stu-id="2756e-112">High-order 32 bits of the currency value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2756e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2756e-113">Remarks</span></span>

<span data-ttu-id="2756e-114">Die **Währungs** Struktur ist eine skalierte ganzzahlige Darstellung einer Dezimalzahl mit vier Ziffern rechts vom Dezimaltrennzeichen.</span><span class="sxs-lookup"><span data-stu-id="2756e-114">The **CURRENCY** structure is a scaled integer representation of a decimal number with four digits to the right of the decimal point.</span></span> <span data-ttu-id="2756e-115">Beispielsweise ist ein gespeicherter Wert von 327500 so auszulegen, dass er einen Währungswert von 32,7500 darstellt.</span><span class="sxs-lookup"><span data-stu-id="2756e-115">For example, a stored value of 327500 is to be construed as representing a currency value of 32.7500.</span></span> 
  
<span data-ttu-id="2756e-116">Die **Currency** -Struktur dient zur Beschreibung einer Eigenschaft vom Typ PT_CURRENCY.</span><span class="sxs-lookup"><span data-stu-id="2756e-116">The **CURRENCY** structure is used to describe a property of type PT_CURRENCY.</span></span> <span data-ttu-id="2756e-117">Weitere Informationen zu Eigenschaftstypen finden Sie unter [MAPI property Type Overview](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2756e-117">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2756e-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2756e-118">See also</span></span>



[<span data-ttu-id="2756e-119">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2756e-119">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="2756e-120">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="2756e-120">MAPI Structures</span></span>](mapi-structures.md)

