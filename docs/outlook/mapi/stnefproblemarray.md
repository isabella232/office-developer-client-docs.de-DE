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
ms.openlocfilehash: 721b14f101e87299f654507f94d4a957f905cac1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434263"
---
# <a name="stnefproblemarray"></a><span data-ttu-id="14a16-103">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="14a16-103">STnefProblemArray</span></span>

  
  
<span data-ttu-id="14a16-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="14a16-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="14a16-105">Enthält ein Array von **STnefProblem-Strukturen,** die ein oder mehrere Verarbeitungsprobleme beschreiben, die während der Codierung oder Decodierung eines TNEF-Datenstroms (Transport Neutral Encapsulation Format) aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="14a16-105">Contains an array of **STnefProblem** structures describing one or more processing problems that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="14a16-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="14a16-106">Header file:</span></span>  <br/> |<span data-ttu-id="14a16-107">Tnef.h</span><span class="sxs-lookup"><span data-stu-id="14a16-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a><span data-ttu-id="14a16-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="14a16-108">Members</span></span>

 <span data-ttu-id="14a16-109">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="14a16-109">**cProblem**</span></span>
  
> <span data-ttu-id="14a16-110">Anzahl der Elemente im Array, das im **aProblem-Element angegeben** ist.</span><span class="sxs-lookup"><span data-stu-id="14a16-110">Count of elements in the array specified in the **aProblem** member.</span></span> 
    
 <span data-ttu-id="14a16-111">**aProblem**</span><span class="sxs-lookup"><span data-stu-id="14a16-111">**aProblem**</span></span>
  
> <span data-ttu-id="14a16-112">Array von [STnefProblem-Strukturen.](stnefproblem.md)</span><span class="sxs-lookup"><span data-stu-id="14a16-112">Array of [STnefProblem](stnefproblem.md) structures.</span></span> <span data-ttu-id="14a16-113">Jede Struktur enthält Informationen zu einem Eigenschafts- oder Attributverarbeitungsproblem.</span><span class="sxs-lookup"><span data-stu-id="14a16-113">Each structure contains information about a property or attribute processing problem.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="14a16-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="14a16-114">Remarks</span></span>

<span data-ttu-id="14a16-115">Wenn während der Attribut- oder Eigenschaftenverarbeitung ein Problem auftritt, erhalten ein Ausgabeparameter in der [ITnef::ExtractProps-Methode](itnef-extractprops.md) und in der [ITnef::Finish-Methode](itnef-finish.md) jeweils einen Zeiger auf eine **STnefProblemArray-Struktur** und **ExtractProps** und **Finish** geben jeweils den Wert MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="14a16-115">If a problem occurs during attribute or property processing, an output parameter in the [ITnef::ExtractProps](itnef-extractprops.md) method and in the [ITnef::Finish](itnef-finish.md) method each receive a pointer to an **STnefProblemArray** structure and **ExtractProps** and **Finish** each return the value MAPI_W_ERRORS_RETURNED.</span></span> <span data-ttu-id="14a16-116">Dieser Fehlerwert gibt an, dass während der Verarbeitung ein Problem aufgetreten ist und eine **STnefProblemArray-Struktur** generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="14a16-116">This error value indicates that a problem arose during processing and an **STnefProblemArray** structure was generated.</span></span> 
  
<span data-ttu-id="14a16-117">Wenn während der Verarbeitung eines Attributs oder einer Eigenschaft keine **STnefProblem-Struktur** generiert wird, kann die Clientanwendung unter der Annahme fortfahren, dass die Verarbeitung dieses Attributs oder dieser Eigenschaft erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="14a16-117">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the client application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="14a16-118">Die einzige Ausnahme tritt auf, wenn das Problem während der Decodierung eines Kapselungsblocks auftstand.</span><span class="sxs-lookup"><span data-stu-id="14a16-118">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="14a16-119">Wenn der Fehler während dieser Decodierung aufgetreten ist, MAPI_E_UNABLE_TO_COMPLETE als [SCODE](scode.md) in der Struktur zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="14a16-119">If the error occurred during this decoding, MAPI_E_UNABLE_TO_COMPLETE can be returned as the [SCODE](scode.md) in the structure.</span></span> <span data-ttu-id="14a16-120">In diesem Fall wird die Decodierung der Komponente, die dem Block entspricht, beendet, und die Decodierung wird in einer anderen Komponente fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="14a16-120">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="14a16-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14a16-121">See also</span></span>



[<span data-ttu-id="14a16-122">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="14a16-122">STnefProblem</span></span>](stnefproblem.md)
  
[<span data-ttu-id="14a16-123">SCODE</span><span class="sxs-lookup"><span data-stu-id="14a16-123">SCODE</span></span>](scode.md)


[<span data-ttu-id="14a16-124">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="14a16-124">MAPI Structures</span></span>](mapi-structures.md)

