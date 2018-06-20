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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c440bb7d8f3d2d3002a4d1a80ca3a671b49f4d2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795474"
---
# <a name="scurrencyarray"></a><span data-ttu-id="fbc4b-103">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="fbc4b-103">SCurrencyArray</span></span>

  
  
<span data-ttu-id="fbc4b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fbc4b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fbc4b-105">Enthält ein Array von Währungswerten, mit denen eine Eigenschaft vom Typ PT_MV_CURRENCY beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fbc4b-105">Contains an array of currency values that are used to describe a property of type PT_MV_CURRENCY.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fbc4b-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="fbc4b-106">Header file:</span></span>  <br/> |<span data-ttu-id="fbc4b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fbc4b-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a><span data-ttu-id="fbc4b-108">Members</span><span class="sxs-lookup"><span data-stu-id="fbc4b-108">Members</span></span>

 <span data-ttu-id="fbc4b-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="fbc4b-109">**cValues**</span></span>
  
> <span data-ttu-id="fbc4b-110">Anzahl der Werte im Array auf den Member **Lpcur** zeigt.</span><span class="sxs-lookup"><span data-stu-id="fbc4b-110">Count of values in the array pointed to by the **lpcur** member.</span></span> 
    
 <span data-ttu-id="fbc4b-111">**lpcur**</span><span class="sxs-lookup"><span data-stu-id="fbc4b-111">**lpcur**</span></span>
  
> <span data-ttu-id="fbc4b-112">Zeiger auf ein Array von [Währung](currency.md) Strukturen, die Währungswerte enthalten.</span><span class="sxs-lookup"><span data-stu-id="fbc4b-112">Pointer to an array of [CURRENCY](currency.md) structures that contain the currency values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fbc4b-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fbc4b-113">Remarks</span></span>

<span data-ttu-id="fbc4b-114">Informationen zu PT_MV_CURRENCY finden Sie unter [Liste der Eigenschaftentypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="fbc4b-114">For information about PT_MV_CURRENCY, see [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fbc4b-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbc4b-115">See also</span></span>



[<span data-ttu-id="fbc4b-116">WÄHRUNG</span><span class="sxs-lookup"><span data-stu-id="fbc4b-116">CURRENCY</span></span>](currency.md)
  
[<span data-ttu-id="fbc4b-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="fbc4b-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="fbc4b-118">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="fbc4b-118">MAPI Structures</span></span>](mapi-structures.md)

