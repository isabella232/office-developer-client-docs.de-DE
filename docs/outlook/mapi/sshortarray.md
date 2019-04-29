---
title: SShortArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SShortArray
api_type:
- COM
ms.assetid: 201ceb76-41bc-4d7b-835d-5196bf3dc234
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8ea7d51b15a6e6acd44a3c0b6158378661f311bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429614"
---
# <a name="sshortarray"></a><span data-ttu-id="bffb3-103">SShortArray</span><span class="sxs-lookup"><span data-stu-id="bffb3-103">SShortArray</span></span>

  
  
<span data-ttu-id="bffb3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bffb3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bffb3-105">Enthält ein Array von Ganzzahlwerten ohne Vorzeichen, die zum Beschreiben einer Eigenschaft vom Typ PT_MV_SHORT verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bffb3-105">Contains an array of unsigned integer values that are used to describe a property of type PT_MV_SHORT.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bffb3-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="bffb3-106">Header file:</span></span>  <br/> |<span data-ttu-id="bffb3-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="bffb3-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a><span data-ttu-id="bffb3-108">Members</span><span class="sxs-lookup"><span data-stu-id="bffb3-108">Members</span></span>

 <span data-ttu-id="bffb3-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="bffb3-109">**cValues**</span></span>
  
> <span data-ttu-id="bffb3-110">Die Anzahl der Werte im Array, auf die durch das **LPI** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="bffb3-110">Count of values in the array pointed to by the **lpi** member.</span></span> 
    
 <span data-ttu-id="bffb3-111">**LPI**</span><span class="sxs-lookup"><span data-stu-id="bffb3-111">**lpi**</span></span>
  
> <span data-ttu-id="bffb3-112">Zeiger auf ein Array von Ganzzahlwerten ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="bffb3-112">Pointer to an array of unsigned integer values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bffb3-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bffb3-113">Remarks</span></span>

<span data-ttu-id="bffb3-114">Weitere Informationen zu PT_MV_SHORT und anderen Eigenschaftstypen finden Sie unter [Property Types](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="bffb3-114">For more information about PT_MV_SHORT and other property types, see [Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bffb3-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bffb3-115">See also</span></span>



[<span data-ttu-id="bffb3-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="bffb3-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="bffb3-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="bffb3-117">MAPI Structures</span></span>](mapi-structures.md)

