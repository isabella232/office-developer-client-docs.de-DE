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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dee1de19ed61fa4f8edab69152315d77545b01b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430385"
---
# <a name="sapptimearray"></a><span data-ttu-id="df753-103">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="df753-103">SAppTimeArray</span></span>

  
  
<span data-ttu-id="df753-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df753-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df753-105">Enthält ein Array von Zeitwerten.</span><span class="sxs-lookup"><span data-stu-id="df753-105">Contains an array of time values.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="df753-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="df753-106">Header file:</span></span>  <br/> |<span data-ttu-id="df753-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="df753-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a><span data-ttu-id="df753-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="df753-108">Members</span></span>

 <span data-ttu-id="df753-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="df753-109">**cValues**</span></span>
  
> <span data-ttu-id="df753-110">Anzahl der Werte im Array, auf das das **lpat-Element verweist.**</span><span class="sxs-lookup"><span data-stu-id="df753-110">Count of values in the array pointed to by the **lpat** member.</span></span> 
    
 <span data-ttu-id="df753-111">**lpat**</span><span class="sxs-lookup"><span data-stu-id="df753-111">**lpat**</span></span>
  
> <span data-ttu-id="df753-112">Zeiger auf ein Array von Anwendungszeitwerten.</span><span class="sxs-lookup"><span data-stu-id="df753-112">Pointer to an array of application time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="df753-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="df753-113">Remarks</span></span>

<span data-ttu-id="df753-114">Die **SAppTimeArray-Struktur** wird verwendet, um Eigenschaften vom Typ PT_MV_APPTIME.</span><span class="sxs-lookup"><span data-stu-id="df753-114">The **SAppTimeArray** structure is used to define properties of type PT_MV_APPTIME.</span></span> <span data-ttu-id="df753-115">Weitere Informationen zu PT_MV_APPTIME finden Sie [unter List of Property Types](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="df753-115">For more information about PT_MV_APPTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="df753-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df753-116">See also</span></span>



[<span data-ttu-id="df753-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="df753-117">MAPI Structures</span></span>](mapi-structures.md)

