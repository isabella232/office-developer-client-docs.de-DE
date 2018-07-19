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
ms.openlocfilehash: 59911531b6d8f9c094ef8563510aaa176e3a63b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795633"
---
# <a name="sshortarray"></a><span data-ttu-id="867a4-103">SShortArray</span><span class="sxs-lookup"><span data-stu-id="867a4-103">SShortArray</span></span>

  
  
<span data-ttu-id="867a4-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="867a4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="867a4-105">Enthält ein Array von Werten Ganzzahl ohne Vorzeichen, die verwendet werden, um eine Eigenschaft vom Typ PT_MV_SHORT zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="867a4-105">Contains an array of unsigned integer values that are used to describe a property of type PT_MV_SHORT.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="867a4-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="867a4-106">Header file:</span></span>  <br/> |<span data-ttu-id="867a4-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="867a4-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a><span data-ttu-id="867a4-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="867a4-108">Members</span></span>

 <span data-ttu-id="867a4-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="867a4-109">**cValues**</span></span>
  
> <span data-ttu-id="867a4-110">Anzahl der Werte im Array auf den Member **Lpi** zeigt.</span><span class="sxs-lookup"><span data-stu-id="867a4-110">Count of values in the array pointed to by the **lpi** member.</span></span> 
    
 <span data-ttu-id="867a4-111">**lpi**</span><span class="sxs-lookup"><span data-stu-id="867a4-111">**lpi**</span></span>
  
> <span data-ttu-id="867a4-112">Zeiger auf ein Array von Werten Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="867a4-112">Pointer to an array of unsigned integer values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="867a4-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="867a4-113">Remarks</span></span>

<span data-ttu-id="867a4-114">Weitere Informationen zu PT_MV_SHORT und anderer Eigenschaftsarten finden Sie unter [Eigenschaftentypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="867a4-114">For more information about PT_MV_SHORT and other property types, see [Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="867a4-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="867a4-115">See also</span></span>



[<span data-ttu-id="867a4-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="867a4-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="867a4-117">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="867a4-117">MAPI Structures</span></span>](mapi-structures.md)

