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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9734adff9c9c7526fc8ff46d17ca913752e104b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795464"
---
# <a name="sdatetimearray"></a><span data-ttu-id="8aef8-103">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="8aef8-103">SDateTimeArray</span></span>

  
  
<span data-ttu-id="8aef8-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8aef8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8aef8-105">Enthält ein Array von Zeitwerte, mit denen eine Eigenschaft vom Typ PT_MV_SYSTIME beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8aef8-105">Contains an array of time values that are used to describe a property of type PT_MV_SYSTIME.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8aef8-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="8aef8-106">Header file:</span></span>  <br/> |<span data-ttu-id="8aef8-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8aef8-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDateTimeArray
{
  ULONG cValues;
  FILETIME FAR *lpft;
} SDateTimeArray;

```

## <a name="members"></a><span data-ttu-id="8aef8-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="8aef8-108">Members</span></span>

 <span data-ttu-id="8aef8-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="8aef8-109">**cValues**</span></span>
  
> <span data-ttu-id="8aef8-110">Anzahl der Werte im Array auf den Member **Lpft** zeigt.</span><span class="sxs-lookup"><span data-stu-id="8aef8-110">Count of values in the array pointed to by the **lpft** member.</span></span> 
    
 <span data-ttu-id="8aef8-111">**lpft**</span><span class="sxs-lookup"><span data-stu-id="8aef8-111">**lpft**</span></span>
  
> <span data-ttu-id="8aef8-112">Zeiger auf ein Array von [FILETIME](filetime.md) -Strukturen, die Zeitwerte enthalten.</span><span class="sxs-lookup"><span data-stu-id="8aef8-112">Pointer to an array of [FILETIME](filetime.md) structures that contain the time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8aef8-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8aef8-113">Remarks</span></span>

<span data-ttu-id="8aef8-114">Weitere Informationen zu PT_MV_SYSTIME finden Sie unter [Liste der Eigenschaftentypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="8aef8-114">For more information about PT_MV_SYSTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8aef8-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8aef8-115">See also</span></span>



[<span data-ttu-id="8aef8-116">FILETIME</span><span class="sxs-lookup"><span data-stu-id="8aef8-116">FILETIME</span></span>](filetime.md)
  
[<span data-ttu-id="8aef8-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="8aef8-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="8aef8-118">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="8aef8-118">MAPI Structures</span></span>](mapi-structures.md)

