---
title: SAppTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAppTimeArray
api_type:
- COM
ms.assetid: 5a1ff95a-9862-4165-8a70-bd2eeb7fe683
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: dee1de19ed61fa4f8edab69152315d77545b01b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331696"
---
# <a name="sapptimearray"></a><span data-ttu-id="46c2d-103">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="46c2d-103">SAppTimeArray</span></span>

  
  
<span data-ttu-id="46c2d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46c2d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46c2d-105">Enthält ein Array von Zeitwerten.</span><span class="sxs-lookup"><span data-stu-id="46c2d-105">Contains an array of time values.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="46c2d-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="46c2d-106">Header file:</span></span>  <br/> |<span data-ttu-id="46c2d-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="46c2d-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a><span data-ttu-id="46c2d-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="46c2d-108">Members</span></span>

 <span data-ttu-id="46c2d-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="46c2d-109">**cValues**</span></span>
  
> <span data-ttu-id="46c2d-110">Die Anzahl der Werte im Array, auf die durch das **lpat** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="46c2d-110">Count of values in the array pointed to by the **lpat** member.</span></span> 
    
 <span data-ttu-id="46c2d-111">**lpat**</span><span class="sxs-lookup"><span data-stu-id="46c2d-111">**lpat**</span></span>
  
> <span data-ttu-id="46c2d-112">Zeiger auf ein Array von Anwendungszeit Werten.</span><span class="sxs-lookup"><span data-stu-id="46c2d-112">Pointer to an array of application time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="46c2d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46c2d-113">Remarks</span></span>

<span data-ttu-id="46c2d-114">Die **SAppTimeArray** -Struktur wird verwendet, um Eigenschaften vom Typ PT_MV_APPTIME zu definieren.</span><span class="sxs-lookup"><span data-stu-id="46c2d-114">The **SAppTimeArray** structure is used to define properties of type PT_MV_APPTIME.</span></span> <span data-ttu-id="46c2d-115">Weitere Informationen zu PT_MV_APPTIME finden Sie unter [Liste der Eigenschaftstypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="46c2d-115">For more information about PT_MV_APPTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="46c2d-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46c2d-116">See also</span></span>



[<span data-ttu-id="46c2d-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="46c2d-117">MAPI Structures</span></span>](mapi-structures.md)

