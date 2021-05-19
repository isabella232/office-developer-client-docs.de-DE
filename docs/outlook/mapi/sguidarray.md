---
title: SGuidArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SGuidArray
api_type:
- COM
ms.assetid: 2091e5fc-75c8-4ea4-87e9-a9bf508e9c58
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3d20a0932de0fb29ea73e56c37e262c0ccd062c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424924"
---
# <a name="sguidarray"></a><span data-ttu-id="e4ad7-103">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="e4ad7-103">SGuidArray</span></span>

  
  
<span data-ttu-id="e4ad7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4ad7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4ad7-105">Enthält ein Array von [GUID-Strukturen,](guid.md) die zum Beschreiben einer Eigenschaft vom Typ PT_MV_CLSID.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-105">Contains an array of [GUID](guid.md) structures that are used to describe a property of type PT_MV_CLSID.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e4ad7-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="e4ad7-106">Header file:</span></span>  <br/> |<span data-ttu-id="e4ad7-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e4ad7-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SGuidArray
{
  ULONG cValues;
  GUID FAR *lpguid;
} SGuidArray;

```

## <a name="members"></a><span data-ttu-id="e4ad7-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="e4ad7-108">Members</span></span>

 <span data-ttu-id="e4ad7-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="e4ad7-109">**cValues**</span></span>
  
> <span data-ttu-id="e4ad7-110">Anzahl der Werte im Array, auf die das **lpguid-Element** verweist.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-110">Count of values in the array pointed to by the **lpguid** member.</span></span> 
    
 <span data-ttu-id="e4ad7-111">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="e4ad7-111">**lpguid**</span></span>
  
> <span data-ttu-id="e4ad7-112">Zeiger auf ein Array von **GUID-Strukturen,** das die Klassenbezeichnerwerte enthält.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-112">Pointer to an array of **GUID** structures that contains the class identifier values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e4ad7-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e4ad7-113">Remarks</span></span>

<span data-ttu-id="e4ad7-114">Weitere Informationen zu PT_MV_CLSID finden Sie unter [List of Property Types](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="e4ad7-114">For more information about PT_MV_CLSID, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e4ad7-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4ad7-115">See also</span></span>



[<span data-ttu-id="e4ad7-116">GUID</span><span class="sxs-lookup"><span data-stu-id="e4ad7-116">GUID</span></span>](guid.md)
  
[<span data-ttu-id="e4ad7-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="e4ad7-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="e4ad7-118">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="e4ad7-118">MAPI Structures</span></span>](mapi-structures.md)

