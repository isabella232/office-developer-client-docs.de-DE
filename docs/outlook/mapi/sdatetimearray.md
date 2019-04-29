---
title: SDateTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDateTimeArray
api_type:
- COM
ms.assetid: 6a0dff65-1055-487c-9d15-4cfe336f2ad7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9d9fd04776742383f40c6989bcf588b24b33d84b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406780"
---
# <a name="sdatetimearray"></a><span data-ttu-id="dd366-103">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="dd366-103">SDateTimeArray</span></span>

  
  
<span data-ttu-id="dd366-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd366-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd366-105">Enthält ein Array von Zeitwerten, die zum Beschreiben einer Eigenschaft vom Typ PT_MV_SYSTIME verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd366-105">Contains an array of time values that are used to describe a property of type PT_MV_SYSTIME.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dd366-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="dd366-106">Header file:</span></span>  <br/> |<span data-ttu-id="dd366-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="dd366-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDateTimeArray
{
  ULONG cValues;
  FILETIME FAR *lpft;
} SDateTimeArray;

```

## <a name="members"></a><span data-ttu-id="dd366-108">Members</span><span class="sxs-lookup"><span data-stu-id="dd366-108">Members</span></span>

 <span data-ttu-id="dd366-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="dd366-109">**cValues**</span></span>
  
> <span data-ttu-id="dd366-110">Die Anzahl der Werte im Array, auf die durch das **lpft** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="dd366-110">Count of values in the array pointed to by the **lpft** member.</span></span> 
    
 <span data-ttu-id="dd366-111">**lpft**</span><span class="sxs-lookup"><span data-stu-id="dd366-111">**lpft**</span></span>
  
> <span data-ttu-id="dd366-112">Zeiger auf ein Array von [FILETIME](filetime.md) -Strukturen, die die Zeitwerte enthalten.</span><span class="sxs-lookup"><span data-stu-id="dd366-112">Pointer to an array of [FILETIME](filetime.md) structures that contain the time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="dd366-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd366-113">Remarks</span></span>

<span data-ttu-id="dd366-114">Weitere Informationen zu PT_MV_SYSTIME finden Sie unter [Liste der Eigenschaftstypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="dd366-114">For more information about PT_MV_SYSTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dd366-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd366-115">See also</span></span>



[<span data-ttu-id="dd366-116">FILETIME</span><span class="sxs-lookup"><span data-stu-id="dd366-116">FILETIME</span></span>](filetime.md)
  
[<span data-ttu-id="dd366-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="dd366-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="dd366-118">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="dd366-118">MAPI Structures</span></span>](mapi-structures.md)

