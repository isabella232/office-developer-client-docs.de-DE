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
ms.openlocfilehash: 1b262ba9c83e9890719f716a373c566be172ae73
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572452"
---
# <a name="scurrencyarray"></a><span data-ttu-id="d88a5-103">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="d88a5-103">SCurrencyArray</span></span>

  
  
<span data-ttu-id="d88a5-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d88a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d88a5-105">Enthält ein Array von Währungswerten, mit denen eine Eigenschaft vom Typ PT_MV_CURRENCY beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d88a5-105">Contains an array of currency values that are used to describe a property of type PT_MV_CURRENCY.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d88a5-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="d88a5-106">Header file:</span></span>  <br/> |<span data-ttu-id="d88a5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d88a5-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a><span data-ttu-id="d88a5-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="d88a5-108">Members</span></span>

 <span data-ttu-id="d88a5-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="d88a5-109">**cValues**</span></span>
  
> <span data-ttu-id="d88a5-110">Anzahl der Werte im Array auf den Member **Lpcur** zeigt.</span><span class="sxs-lookup"><span data-stu-id="d88a5-110">Count of values in the array pointed to by the **lpcur** member.</span></span> 
    
 <span data-ttu-id="d88a5-111">**lpcur**</span><span class="sxs-lookup"><span data-stu-id="d88a5-111">**lpcur**</span></span>
  
> <span data-ttu-id="d88a5-112">Zeiger auf ein Array von [Währung](currency.md) Strukturen, die Währungswerte enthalten.</span><span class="sxs-lookup"><span data-stu-id="d88a5-112">Pointer to an array of [CURRENCY](currency.md) structures that contain the currency values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d88a5-113">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="d88a5-113">Remarks</span></span>

<span data-ttu-id="d88a5-114">Informationen zu PT_MV_CURRENCY finden Sie unter [Liste der Eigenschaftentypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="d88a5-114">For information about PT_MV_CURRENCY, see [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d88a5-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d88a5-115">See also</span></span>



[<span data-ttu-id="d88a5-116">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="d88a5-116">CURRENCY</span></span>](currency.md)
  
[<span data-ttu-id="d88a5-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d88a5-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="d88a5-118">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="d88a5-118">MAPI Structures</span></span>](mapi-structures.md)

