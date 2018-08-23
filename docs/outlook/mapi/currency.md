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
ms.openlocfilehash: b5a2cd09942559167300d8a921987864b8c5e48f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576463"
---
# <a name="currency"></a><span data-ttu-id="30382-103">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="30382-103">CURRENCY</span></span>

  
  
<span data-ttu-id="30382-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30382-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30382-105">Enthält eine 64-Bit-Ganzzahl, die einen Währungswert darstellt.</span><span class="sxs-lookup"><span data-stu-id="30382-105">Contains a signed 64-bit integer representing a currency value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="30382-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="30382-106">Header file:</span></span>  <br/> |<span data-ttu-id="30382-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="30382-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct tagCY
{
  unsigned long Lo;
  long Hi;
} CURRENCY;

```

## <a name="members"></a><span data-ttu-id="30382-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="30382-108">Members</span></span>

 <span data-ttu-id="30382-109">**Lo**</span><span class="sxs-lookup"><span data-stu-id="30382-109">**Lo**</span></span>
  
> <span data-ttu-id="30382-110">Niederwertige 32 Bit der Währungswert.</span><span class="sxs-lookup"><span data-stu-id="30382-110">Low-order 32 bits of the currency value.</span></span> 
    
 <span data-ttu-id="30382-111">**Hallo**</span><span class="sxs-lookup"><span data-stu-id="30382-111">**Hi**</span></span>
  
> <span data-ttu-id="30382-112">Obere 32 Bit der Währungswert.</span><span class="sxs-lookup"><span data-stu-id="30382-112">High-order 32 bits of the currency value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="30382-113">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="30382-113">Remarks</span></span>

<span data-ttu-id="30382-114">Die **Währung** -Struktur ist eine skalierte Ganzzahl Darstellung einer ganzen Zahl mit vier Stellen rechts vom Dezimalkomma.</span><span class="sxs-lookup"><span data-stu-id="30382-114">The **CURRENCY** structure is a scaled integer representation of a decimal number with four digits to the right of the decimal point.</span></span> <span data-ttu-id="30382-115">Beispielsweise ist der gespeicherter Wert 327500, ausgelegt werden als einen Währungswert des 32.7500 darstellt.</span><span class="sxs-lookup"><span data-stu-id="30382-115">For example, a stored value of 327500 is to be construed as representing a currency value of 32.7500.</span></span> 
  
<span data-ttu-id="30382-116">Die **Währung** Struktur wird verwendet, um eine Eigenschaft vom Typ PT_CURRENCY beschrieben.</span><span class="sxs-lookup"><span data-stu-id="30382-116">The **CURRENCY** structure is used to describe a property of type PT_CURRENCY.</span></span> <span data-ttu-id="30382-117">Informationen zu Eigenschaftstypen finden Sie unter [MAPI-Eigenschaft Type Overview](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="30382-117">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="30382-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30382-118">See also</span></span>



[<span data-ttu-id="30382-119">SPropValue</span><span class="sxs-lookup"><span data-stu-id="30382-119">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="30382-120">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="30382-120">MAPI Structures</span></span>](mapi-structures.md)

