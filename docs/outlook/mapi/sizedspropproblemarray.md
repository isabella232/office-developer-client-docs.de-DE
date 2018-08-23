---
title: SizedSPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropProblemArray
api_type:
- COM
ms.assetid: 2fc3febb-8c69-4315-a112-a28eee98013d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bbced8412c2c3438c58af74ef072a46606b59ddc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594614"
---
# <a name="sizedspropproblemarray"></a><span data-ttu-id="bc189-103">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="bc189-103">SizedSPropProblemArray</span></span>

<span data-ttu-id="bc189-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc189-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc189-105">Erstellt eine benannte [SPropProblemArray](spropproblemarray.md) -Struktur, die eine angegebene Anzahl von [SPropProblem](spropproblem.md) Strukturen enthält.</span><span class="sxs-lookup"><span data-stu-id="bc189-105">Creates a named [SPropProblemArray](spropproblemarray.md) structure that contains a specified number of [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bc189-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="bc189-106">Header file:</span></span>  <br/> |<span data-ttu-id="bc189-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bc189-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="bc189-108">Verwandte Struktur:</span><span class="sxs-lookup"><span data-stu-id="bc189-108">Related structure:</span></span>  <br/> |<span data-ttu-id="bc189-109">**SPropProblemArray**</span><span class="sxs-lookup"><span data-stu-id="bc189-109">**SPropProblemArray**</span></span> <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a><span data-ttu-id="bc189-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc189-110">Parameters</span></span>

<span data-ttu-id="bc189-111">__cprob_</span><span class="sxs-lookup"><span data-stu-id="bc189-111">__cprob_</span></span>
  
> <span data-ttu-id="bc189-112">Anzahl der **SPropProblem** Strukturen, die in die neue Struktur eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="bc189-112">Count of **SPropProblem** structures to be included in the new structure.</span></span> 
    
<span data-ttu-id="bc189-113">__Namen_</span><span class="sxs-lookup"><span data-stu-id="bc189-113">__name_</span></span>
  
> <span data-ttu-id="bc189-114">Der Name für die neue Struktur.</span><span class="sxs-lookup"><span data-stu-id="bc189-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bc189-115">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="bc189-115">Remarks</span></span>

<span data-ttu-id="bc189-116">Verwenden Sie das Makro **SizedSPropProblemArray** , um ein Problem Array-Eigenschaft mit expliziten Grenzen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bc189-116">Use the **SizedSPropProblemArray** macro to create a property problem array with explicit bounds.</span></span> <span data-ttu-id="bc189-117">Um die neue Struktur verwenden, die als Zeiger auf eine **SPropProblemArray** -Struktur aus dem Makro **SizedSPropProblemArray** erzeugt, führen Sie die folgende Umwandlung:</span><span class="sxs-lookup"><span data-stu-id="bc189-117">To use the new structure that results from the **SizedSPropProblemArray** macro as a pointer to an **SPropProblemArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a><span data-ttu-id="bc189-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc189-118">See also</span></span>

- [<span data-ttu-id="bc189-119">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="bc189-119">SPropProblemArray</span></span>](spropproblemarray.md)
- [<span data-ttu-id="bc189-120">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="bc189-120">SPropProblem</span></span>](spropproblem.md)
- [<span data-ttu-id="bc189-121">Makros im Zusammenhang mit Strukturen</span><span class="sxs-lookup"><span data-stu-id="bc189-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

