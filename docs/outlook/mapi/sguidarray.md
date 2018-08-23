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
ms.openlocfilehash: bc0ae6d69db6077c17d2efa66d04a5366f2395a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585570"
---
# <a name="sguidarray"></a><span data-ttu-id="9e3bd-103">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="9e3bd-103">SGuidArray</span></span>

  
  
<span data-ttu-id="9e3bd-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e3bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e3bd-105">Enthält ein Array von [GUID](guid.md) -Strukturen, die verwendet werden, um eine Eigenschaft vom Typ PT_MV_CLSID beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9e3bd-105">Contains an array of [GUID](guid.md) structures that are used to describe a property of type PT_MV_CLSID.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e3bd-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="9e3bd-106">Header file:</span></span>  <br/> |<span data-ttu-id="9e3bd-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9e3bd-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SGuidArray
{
  ULONG cValues;
  GUID FAR *lpguid;
} SGuidArray;

```

## <a name="members"></a><span data-ttu-id="9e3bd-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="9e3bd-108">Members</span></span>

 <span data-ttu-id="9e3bd-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="9e3bd-109">**cValues**</span></span>
  
> <span data-ttu-id="9e3bd-110">Anzahl der Werte im Array auf den Member **x Lpguid** zeigt.</span><span class="sxs-lookup"><span data-stu-id="9e3bd-110">Count of values in the array pointed to by the **lpguid** member.</span></span> 
    
 <span data-ttu-id="9e3bd-111">**x lpguid**</span><span class="sxs-lookup"><span data-stu-id="9e3bd-111">**lpguid**</span></span>
  
> <span data-ttu-id="9e3bd-112">Zeiger auf ein Array von **GUID** -Strukturen, die die Klasse ID-Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="9e3bd-112">Pointer to an array of **GUID** structures that contains the class identifier values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9e3bd-113">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="9e3bd-113">Remarks</span></span>

<span data-ttu-id="9e3bd-114">Weitere Informationen zu PT_MV_CLSID finden Sie unter [Liste der Eigenschaftentypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="9e3bd-114">For more information about PT_MV_CLSID, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9e3bd-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e3bd-115">See also</span></span>



[<span data-ttu-id="9e3bd-116">GUID</span><span class="sxs-lookup"><span data-stu-id="9e3bd-116">GUID</span></span>](guid.md)
  
[<span data-ttu-id="9e3bd-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="9e3bd-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="9e3bd-118">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="9e3bd-118">MAPI Structures</span></span>](mapi-structures.md)

