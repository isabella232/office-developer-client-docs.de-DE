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
ms.openlocfilehash: d277908d3ec96537f63511e4d50488a694696bd5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581223"
---
# <a name="sapptimearray"></a><span data-ttu-id="fa752-103">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="fa752-103">SAppTimeArray</span></span>

  
  
<span data-ttu-id="fa752-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa752-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa752-105">Enthält ein Array von Zeitwerte an.</span><span class="sxs-lookup"><span data-stu-id="fa752-105">Contains an array of time values.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fa752-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="fa752-106">Header file:</span></span>  <br/> |<span data-ttu-id="fa752-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fa752-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a><span data-ttu-id="fa752-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="fa752-108">Members</span></span>

 <span data-ttu-id="fa752-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="fa752-109">**cValues**</span></span>
  
> <span data-ttu-id="fa752-110">Anzahl der Werte im Array auf den Member **Lpat** zeigt.</span><span class="sxs-lookup"><span data-stu-id="fa752-110">Count of values in the array pointed to by the **lpat** member.</span></span> 
    
 <span data-ttu-id="fa752-111">**lpat**</span><span class="sxs-lookup"><span data-stu-id="fa752-111">**lpat**</span></span>
  
> <span data-ttu-id="fa752-112">Zeiger auf ein Array von Zeitwerte für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="fa752-112">Pointer to an array of application time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fa752-113">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="fa752-113">Remarks</span></span>

<span data-ttu-id="fa752-114">Die Struktur **SAppTimeArray** wird verwendet, um die Eigenschaften des Typs PT_MV_APPTIME definieren.</span><span class="sxs-lookup"><span data-stu-id="fa752-114">The **SAppTimeArray** structure is used to define properties of type PT_MV_APPTIME.</span></span> <span data-ttu-id="fa752-115">Weitere Informationen zu PT_MV_APPTIME finden Sie unter [Liste der Eigenschaftentypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="fa752-115">For more information about PT_MV_APPTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fa752-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa752-116">See also</span></span>



[<span data-ttu-id="fa752-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="fa752-117">MAPI Structures</span></span>](mapi-structures.md)

