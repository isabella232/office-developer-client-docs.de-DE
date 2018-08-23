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
ms.openlocfilehash: b684309211bbc008856311158c67864d958c96a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573033"
---
# <a name="sshortarray"></a><span data-ttu-id="eb7fa-103">SShortArray</span><span class="sxs-lookup"><span data-stu-id="eb7fa-103">SShortArray</span></span>

  
  
<span data-ttu-id="eb7fa-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb7fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb7fa-105">Enthält ein Array von Werten Ganzzahl ohne Vorzeichen, die verwendet werden, um eine Eigenschaft vom Typ PT_MV_SHORT zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="eb7fa-105">Contains an array of unsigned integer values that are used to describe a property of type PT_MV_SHORT.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eb7fa-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="eb7fa-106">Header file:</span></span>  <br/> |<span data-ttu-id="eb7fa-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eb7fa-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a><span data-ttu-id="eb7fa-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="eb7fa-108">Members</span></span>

 <span data-ttu-id="eb7fa-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="eb7fa-109">**cValues**</span></span>
  
> <span data-ttu-id="eb7fa-110">Anzahl der Werte im Array auf den Member **Lpi** zeigt.</span><span class="sxs-lookup"><span data-stu-id="eb7fa-110">Count of values in the array pointed to by the **lpi** member.</span></span> 
    
 <span data-ttu-id="eb7fa-111">**lpi**</span><span class="sxs-lookup"><span data-stu-id="eb7fa-111">**lpi**</span></span>
  
> <span data-ttu-id="eb7fa-112">Zeiger auf ein Array von Werten Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="eb7fa-112">Pointer to an array of unsigned integer values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eb7fa-113">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="eb7fa-113">Remarks</span></span>

<span data-ttu-id="eb7fa-114">Weitere Informationen zu PT_MV_SHORT und anderer Eigenschaftsarten finden Sie unter [Eigenschaftentypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="eb7fa-114">For more information about PT_MV_SHORT and other property types, see [Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eb7fa-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb7fa-115">See also</span></span>



[<span data-ttu-id="eb7fa-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="eb7fa-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="eb7fa-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="eb7fa-117">MAPI Structures</span></span>](mapi-structures.md)

