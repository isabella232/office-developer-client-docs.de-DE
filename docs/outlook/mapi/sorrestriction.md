---
title: SOrRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SOrRestriction
api_type:
- COM
ms.assetid: 6fee29ce-9a34-4e0c-bb71-03120c3f1117
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9b4ca4628f356142eb5303c064e3916474810fda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345101"
---
# <a name="sorrestriction"></a><span data-ttu-id="de4c3-103">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="de4c3-103">SOrRestriction</span></span>

  
  
<span data-ttu-id="de4c3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de4c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de4c3-105">Beschreibt eine **oder** -Einschränkung, die zum Anwenden einer logischen **or** -Operation auf eine Einschränkung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="de4c3-105">Describes an **OR** restriction which is used to apply a logical **OR** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="de4c3-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="de4c3-106">Header file:</span></span>  <br/> |<span data-ttu-id="de4c3-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="de4c3-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SOrRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SOrRestriction;

```

## <a name="members"></a><span data-ttu-id="de4c3-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="de4c3-108">Members</span></span>

 <span data-ttu-id="de4c3-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="de4c3-109">**cRes**</span></span>
  
> <span data-ttu-id="de4c3-110">Anzahl der Strukturen im Array, auf die durch das **lpRes** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="de4c3-110">Count of structures in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="de4c3-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="de4c3-111">**lpRes**</span></span>
  
> <span data-ttu-id="de4c3-112">Zeiger auf die [SRestriction](srestriction.md) -Struktur, die die zu verbindende Einschränkung mit der logischen **or** -Operation beschreibt.</span><span class="sxs-lookup"><span data-stu-id="de4c3-112">Pointer to the [SRestriction](srestriction.md) structure describing the restriction to be joined using the logical **OR** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="de4c3-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de4c3-113">Remarks</span></span>

<span data-ttu-id="de4c3-114">Weitere Informationen zur **SOrRestriction** -Struktur finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="de4c3-114">For more information about the **SOrRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="de4c3-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de4c3-115">See also</span></span>



[<span data-ttu-id="de4c3-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="de4c3-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="de4c3-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="de4c3-117">MAPI Structures</span></span>](mapi-structures.md)

