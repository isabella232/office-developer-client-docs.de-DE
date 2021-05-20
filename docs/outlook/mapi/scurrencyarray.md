---
title: SCurrencyArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SCurrencyArray
api_type:
- COM
ms.assetid: d28852ab-b542-40e1-b2ec-85d20a2eddfd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e9468d0c7fc7e46475afe19f12f225e53196639e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439401"
---
# <a name="scurrencyarray"></a><span data-ttu-id="13012-103">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="13012-103">SCurrencyArray</span></span>

  
  
<span data-ttu-id="13012-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13012-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13012-105">Enthält ein Array von Währungswerten, die zum Beschreiben einer Eigenschaft vom Typ PT_MV_CURRENCY.</span><span class="sxs-lookup"><span data-stu-id="13012-105">Contains an array of currency values that are used to describe a property of type PT_MV_CURRENCY.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="13012-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="13012-106">Header file:</span></span>  <br/> |<span data-ttu-id="13012-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="13012-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a><span data-ttu-id="13012-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="13012-108">Members</span></span>

 <span data-ttu-id="13012-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="13012-109">**cValues**</span></span>
  
> <span data-ttu-id="13012-110">Anzahl der Werte im Array, auf das das **lpcur-Element verweist.**</span><span class="sxs-lookup"><span data-stu-id="13012-110">Count of values in the array pointed to by the **lpcur** member.</span></span> 
    
 <span data-ttu-id="13012-111">**lpcur**</span><span class="sxs-lookup"><span data-stu-id="13012-111">**lpcur**</span></span>
  
> <span data-ttu-id="13012-112">Zeiger auf ein Array von [CURRENCY-Strukturen,](currency.md) die die Währungswerte enthalten.</span><span class="sxs-lookup"><span data-stu-id="13012-112">Pointer to an array of [CURRENCY](currency.md) structures that contain the currency values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="13012-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="13012-113">Remarks</span></span>

<span data-ttu-id="13012-114">Weitere Informationen zu PT_MV_CURRENCY finden Sie [unter List of Property Types](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="13012-114">For information about PT_MV_CURRENCY, see [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="13012-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13012-115">See also</span></span>



[<span data-ttu-id="13012-116">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="13012-116">CURRENCY</span></span>](currency.md)
  
[<span data-ttu-id="13012-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="13012-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="13012-118">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="13012-118">MAPI Structures</span></span>](mapi-structures.md)

