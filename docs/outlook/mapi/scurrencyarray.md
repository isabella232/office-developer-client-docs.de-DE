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
# <a name="scurrencyarray"></a><span data-ttu-id="c2744-103">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="c2744-103">SCurrencyArray</span></span>

  
  
<span data-ttu-id="c2744-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2744-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c2744-105">Enthält ein Array von Currency-Werten, die zum Beschreiben einer Eigenschaft vom Typ PT_MV_CURRENCY verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2744-105">Contains an array of currency values that are used to describe a property of type PT_MV_CURRENCY.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c2744-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c2744-106">Header file:</span></span>  <br/> |<span data-ttu-id="c2744-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c2744-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a><span data-ttu-id="c2744-108">Members</span><span class="sxs-lookup"><span data-stu-id="c2744-108">Members</span></span>

 <span data-ttu-id="c2744-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="c2744-109">**cValues**</span></span>
  
> <span data-ttu-id="c2744-110">Die Anzahl der Werte im Array, auf die durch das **lpcur** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c2744-110">Count of values in the array pointed to by the **lpcur** member.</span></span> 
    
 <span data-ttu-id="c2744-111">**lpcur**</span><span class="sxs-lookup"><span data-stu-id="c2744-111">**lpcur**</span></span>
  
> <span data-ttu-id="c2744-112">Zeiger auf ein Array von [Währungs](currency.md) Strukturen, die die Währungswerte enthalten.</span><span class="sxs-lookup"><span data-stu-id="c2744-112">Pointer to an array of [CURRENCY](currency.md) structures that contain the currency values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c2744-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2744-113">Remarks</span></span>

<span data-ttu-id="c2744-114">Weitere Informationen zu PT_MV_CURRENCY finden Sie unter [Liste der Eigenschaftentypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="c2744-114">For information about PT_MV_CURRENCY, see [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c2744-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2744-115">See also</span></span>



[<span data-ttu-id="c2744-116">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="c2744-116">CURRENCY</span></span>](currency.md)
  
[<span data-ttu-id="c2744-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c2744-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="c2744-118">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="c2744-118">MAPI Structures</span></span>](mapi-structures.md)

