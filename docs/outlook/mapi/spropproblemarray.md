---
title: SPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropProblemArray
api_type:
- COM
ms.assetid: 3fbaa77a-be43-4fce-af67-1826ee101799
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3fd61828cd631c4abc0131da867ca213a3c44d20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795620"
---
# <a name="spropproblemarray"></a><span data-ttu-id="c06da-103">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="c06da-103">SPropProblemArray</span></span>

  
  
<span data-ttu-id="c06da-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c06da-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c06da-105">Enthält ein Array von Strukturen für eine oder mehrere [SPropProblem](spropproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="c06da-105">Contains an array of one or more [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c06da-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c06da-106">Header file:</span></span>  <br/> |<span data-ttu-id="c06da-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c06da-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c06da-108">Verwandte Makros:</span><span class="sxs-lookup"><span data-stu-id="c06da-108">Related macros:</span></span>  <br/> |[<span data-ttu-id="c06da-109">CbNewSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="c06da-109">CbNewSPropProblemArray</span></span>](cbnewspropproblemarray.md) <br/> [<span data-ttu-id="c06da-110">CbSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="c06da-110">CbSPropProblemArray</span></span>](cbspropproblemarray.md) <br/> [<span data-ttu-id="c06da-111">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="c06da-111">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
   
```cpp
typedef struct _SPropProblemArray
{
  ULONG cProblem;
  SPropProblem aProblem[MAPI_DIM];
} SPropProblemArray, FAR *LPSPropProblemArray;

```

## <a name="members"></a><span data-ttu-id="c06da-112">Members</span><span class="sxs-lookup"><span data-stu-id="c06da-112">Members</span></span>

 <span data-ttu-id="c06da-113">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="c06da-113">**cProblem**</span></span>
  
> <span data-ttu-id="c06da-114">Anzahl der [SPropProblem](spropproblem.md) Strukturen in der durch das **aProblem** -Element angegebenen Arrays.</span><span class="sxs-lookup"><span data-stu-id="c06da-114">Count of [SPropProblem](spropproblem.md) structures in the array indicated by the **aProblem** member.</span></span> 
    
 <span data-ttu-id="c06da-115">**aProblem**</span><span class="sxs-lookup"><span data-stu-id="c06da-115">**aProblem**</span></span>
  
> <span data-ttu-id="c06da-116">Array von **SPropProblem** -Strukturen, jeder, einen Eigenschaftsfehler beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c06da-116">Array of **SPropProblem** structures, each describing a property error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c06da-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c06da-117">Remarks</span></span>

<span data-ttu-id="c06da-118">Weitere Informationen zur Funktionsweise von der Strukturen **SPropProblem** und **SPropProblemArray** mit Fehlern im Zusammenhang mit Eigenschaften finden Sie unter [MAPI-Eigenschaften mit dem Namen](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="c06da-118">For more information about how the **SPropProblem** and **SPropProblemArray** structures work with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c06da-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c06da-119">See also</span></span>



[<span data-ttu-id="c06da-120">SCODE</span><span class="sxs-lookup"><span data-stu-id="c06da-120">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="c06da-121">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="c06da-121">SPropProblem</span></span>](spropproblem.md)


[<span data-ttu-id="c06da-122">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="c06da-122">MAPI Structures</span></span>](mapi-structures.md)

