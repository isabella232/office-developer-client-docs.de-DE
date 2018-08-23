---
title: SBinaryArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinaryArray
api_type:
- COM
ms.assetid: 2d5b7302-cad2-4522-beb1-7c6c711f42e6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e601a59a68a3a7d248165d4e573c5abc34d27e2a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586466"
---
# <a name="sbinaryarray"></a><span data-ttu-id="ced38-103">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="ced38-103">SBinaryArray</span></span>

  
  
<span data-ttu-id="ced38-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ced38-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ced38-105">Enthält ein Array von binären Werten.</span><span class="sxs-lookup"><span data-stu-id="ced38-105">Contains an array of binary values.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ced38-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="ced38-106">Header file:</span></span>  <br/> |<span data-ttu-id="ced38-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ced38-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a><span data-ttu-id="ced38-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="ced38-108">Members</span></span>

 <span data-ttu-id="ced38-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="ced38-109">**cValues**</span></span>
  
> <span data-ttu-id="ced38-110">Anzahl der Werte im Array auf den Member **Lpbin** zeigt.</span><span class="sxs-lookup"><span data-stu-id="ced38-110">Count of values in the array pointed to by the **lpbin** member.</span></span> 
    
 <span data-ttu-id="ced38-111">**lpbin**</span><span class="sxs-lookup"><span data-stu-id="ced38-111">**lpbin**</span></span>
  
> <span data-ttu-id="ced38-112">Zeiger auf ein Array von [SBinary](sbinary.md) -Strukturen, die binäre Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="ced38-112">Pointer to an array of [SBinary](sbinary.md) structures that holds the binary values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ced38-113">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="ced38-113">Remarks</span></span>

<span data-ttu-id="ced38-114">Die Struktur **SBinaryArray** wird verwendet, um Eigenschaften vom Typ PT_MV_BINARY beschreiben.</span><span class="sxs-lookup"><span data-stu-id="ced38-114">The **SBinaryArray** structure is used to describe properties of type PT_MV_BINARY.</span></span> 
  
<span data-ttu-id="ced38-115">Weitere Informationen zu PT_MV_BINARY finden Sie unter [Liste der Eigenschaftentypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="ced38-115">For more information about PT_MV_BINARY, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ced38-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ced38-116">See also</span></span>



[<span data-ttu-id="ced38-117">SBinary</span><span class="sxs-lookup"><span data-stu-id="ced38-117">SBinary</span></span>](sbinary.md)
  
[<span data-ttu-id="ced38-118">SPropValue</span><span class="sxs-lookup"><span data-stu-id="ced38-118">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="ced38-119">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="ced38-119">MAPI Structures</span></span>](mapi-structures.md)

