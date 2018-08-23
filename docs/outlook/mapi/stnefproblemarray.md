---
title: STnefProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STnefProblemArray
api_type:
- COM
ms.assetid: 115d845b-4168-4d49-b880-219ee28baa9a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 924ddbc7c2ad1ed84ce6927ae089b6eb223bfb92
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563506"
---
# <a name="stnefproblemarray"></a><span data-ttu-id="7f924-103">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="7f924-103">STnefProblemArray</span></span>

  
  
<span data-ttu-id="7f924-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f924-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f924-105">Enthält ein Array von **STnefProblem** -Strukturen, die eine oder mehrere Verarbeitung von Problemen, die bei der Codierung aufgetreten oder Decodierung eines Streams Transport Neutral Encapsulation Format (TNEF) beschreiben.</span><span class="sxs-lookup"><span data-stu-id="7f924-105">Contains an array of **STnefProblem** structures describing one or more processing problems that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7f924-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="7f924-106">Header file:</span></span>  <br/> |<span data-ttu-id="7f924-107">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="7f924-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a><span data-ttu-id="7f924-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="7f924-108">Members</span></span>

 <span data-ttu-id="7f924-109">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="7f924-109">**cProblem**</span></span>
  
> <span data-ttu-id="7f924-110">Anzahl der Elemente im Array im **aProblem** -Member angegeben.</span><span class="sxs-lookup"><span data-stu-id="7f924-110">Count of elements in the array specified in the **aProblem** member.</span></span> 
    
 <span data-ttu-id="7f924-111">**aProblem**</span><span class="sxs-lookup"><span data-stu-id="7f924-111">**aProblem**</span></span>
  
> <span data-ttu-id="7f924-112">Array von Strukturen [STnefProblem](stnefproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="7f924-112">Array of [STnefProblem](stnefproblem.md) structures.</span></span> <span data-ttu-id="7f924-113">Jede Struktur enthält Informationen zu einer Eigenschaft oder ein Problem bei der Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="7f924-113">Each structure contains information about a property or attribute processing problem.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7f924-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="7f924-114">Remarks</span></span>

<span data-ttu-id="7f924-115">Wenn Attribut oder Eigenschaft Verarbeitung ein Problem auftritt, wird ein Output-Parameter in der [ITnef::ExtractProps](itnef-extractprops.md) -Methode und in der [ITnef::Finish](itnef-finish.md) -Methode jedes einen Zeiger auf eine **STnefProblemArray** Struktur und **ExtractProps **und der Wert MAPI_W_ERRORS_RETURNED **Ende** jeder zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7f924-115">If a problem occurs during attribute or property processing, an output parameter in the [ITnef::ExtractProps](itnef-extractprops.md) method and in the [ITnef::Finish](itnef-finish.md) method each receive a pointer to an **STnefProblemArray** structure and **ExtractProps** and **Finish** each return the value MAPI_W_ERRORS_RETURNED.</span></span> <span data-ttu-id="7f924-116">Dieser Fehlerwert gibt an, dass ein Problem aufgetreten, während der Verarbeitung ist und eine **STnefProblemArray** -Struktur generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7f924-116">This error value indicates that a problem arose during processing and an **STnefProblemArray** structure was generated.</span></span> 
  
<span data-ttu-id="7f924-117">Wenn eine Struktur **STnefProblem** während der Verarbeitung eines Attribut oder Eigenschaft nicht generiert wird, kann die Client-Anwendung unter der Annahme weiterhin, die die Verarbeitung dieses Attribut oder Eigenschaft erfolgreich waren.</span><span class="sxs-lookup"><span data-stu-id="7f924-117">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the client application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="7f924-118">Die einzige Ausnahme tritt auf, wenn das Problem aufgetreten ist, während der Decodierung eines Blocks Kapselung.</span><span class="sxs-lookup"><span data-stu-id="7f924-118">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="7f924-119">Wenn der Fehler aufgetreten ist, während diese Decodierung, kann als die [SCODE](scode.md) in der Struktur MAPI_E_UNABLE_TO_COMPLETE zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7f924-119">If the error occurred during this decoding, MAPI_E_UNABLE_TO_COMPLETE can be returned as the [SCODE](scode.md) in the structure.</span></span> <span data-ttu-id="7f924-120">In diesem Fall die Decodierung der die entsprechende Komponente für den Block wird angehalten und der Decodierung in einer anderen Komponente fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="7f924-120">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7f924-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f924-121">See also</span></span>



[<span data-ttu-id="7f924-122">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="7f924-122">STnefProblem</span></span>](stnefproblem.md)
  
[<span data-ttu-id="7f924-123">SCODE</span><span class="sxs-lookup"><span data-stu-id="7f924-123">SCODE</span></span>](scode.md)


[<span data-ttu-id="7f924-124">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="7f924-124">MAPI Structures</span></span>](mapi-structures.md)

