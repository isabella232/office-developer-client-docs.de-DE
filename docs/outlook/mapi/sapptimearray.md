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
ms.openlocfilehash: 834a7141f0e7150140fa27c21d88db422d6f5561
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795417"
---
# <a name="sapptimearray"></a><span data-ttu-id="c2326-103">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="c2326-103">SAppTimeArray</span></span>

  
  
<span data-ttu-id="c2326-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c2326-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c2326-105">Enthält ein Array von Zeitwerte an.</span><span class="sxs-lookup"><span data-stu-id="c2326-105">Contains an array of time values.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c2326-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c2326-106">Header file:</span></span>  <br/> |<span data-ttu-id="c2326-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c2326-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a><span data-ttu-id="c2326-108">Members</span><span class="sxs-lookup"><span data-stu-id="c2326-108">Members</span></span>

 <span data-ttu-id="c2326-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="c2326-109">**cValues**</span></span>
  
> <span data-ttu-id="c2326-110">Anzahl der Werte im Array auf den Member **Lpat** zeigt.</span><span class="sxs-lookup"><span data-stu-id="c2326-110">Count of values in the array pointed to by the **lpat** member.</span></span> 
    
 <span data-ttu-id="c2326-111">**lpat**</span><span class="sxs-lookup"><span data-stu-id="c2326-111">**lpat**</span></span>
  
> <span data-ttu-id="c2326-112">Zeiger auf ein Array von Zeitwerte für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c2326-112">Pointer to an array of application time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c2326-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c2326-113">Remarks</span></span>

<span data-ttu-id="c2326-114">Die Struktur **SAppTimeArray** wird verwendet, um die Eigenschaften des Typs PT_MV_APPTIME definieren.</span><span class="sxs-lookup"><span data-stu-id="c2326-114">The **SAppTimeArray** structure is used to define properties of type PT_MV_APPTIME.</span></span> <span data-ttu-id="c2326-115">Weitere Informationen zu PT_MV_APPTIME finden Sie unter [Liste der Eigenschaftentypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="c2326-115">For more information about PT_MV_APPTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c2326-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2326-116">See also</span></span>



[<span data-ttu-id="c2326-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="c2326-117">MAPI Structures</span></span>](mapi-structures.md)

