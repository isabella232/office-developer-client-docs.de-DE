---
title: STnefProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STnefProblem
api_type:
- COM
ms.assetid: 3fe651b7-0ddf-42fd-8277-9224505be1a8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 19d20a3fb06f6a0a0671ba4bfd938da314001778
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435180"
---
# <a name="stnefproblem"></a><span data-ttu-id="6ab39-103">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="6ab39-103">STnefProblem</span></span>

  
  
<span data-ttu-id="6ab39-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ab39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ab39-105">Enthält Informationen zu einem Problem bei der Eigenschaft oder Attribut Verarbeitung, das bei der Codierung oder Decodierung eines Transport Neutral Encapsulation Format (TNEF)-Streams aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="6ab39-105">Contains information about a property or attribute processing problem that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6ab39-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="6ab39-106">Header file:</span></span>  <br/> |<span data-ttu-id="6ab39-107">TNEF. h</span><span class="sxs-lookup"><span data-stu-id="6ab39-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblem
{
  ULONG ulComponent;
  ULONG ulAttribute;
  ULONG ulPropTag;
  SCODE scode;
} STnefProblem;

```

## <a name="members"></a><span data-ttu-id="6ab39-108">Members</span><span class="sxs-lookup"><span data-stu-id="6ab39-108">Members</span></span>

 <span data-ttu-id="6ab39-109">**ulComponent**</span><span class="sxs-lookup"><span data-stu-id="6ab39-109">**ulComponent**</span></span>
  
> <span data-ttu-id="6ab39-110">Die Art der Verarbeitung, bei der das Problem aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="6ab39-110">The type of processing during which the problem occurred.</span></span> <span data-ttu-id="6ab39-111">Wenn das Problem während der Nachrichtenverarbeitung aufgetreten ist, wird das **ulComponent** -Element auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6ab39-111">If the problem occurred during message processing, the **ulComponent** member is set to zero.</span></span> <span data-ttu-id="6ab39-112">Wenn das Problem bei der Anlagenverarbeitung aufgetreten ist, wird **ulComponent** auf den Wert **PR_ATTACH_NUM** ([pidtagattachnumber (](pidtagattachnumber-canonical-property.md)) der entsprechenden Anlage festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6ab39-112">If the problem occurred during attachment processing, **ulComponent** is set equal to the corresponding attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) value.</span></span>
    
 <span data-ttu-id="6ab39-113">**ulAttribute**</span><span class="sxs-lookup"><span data-stu-id="6ab39-113">**ulAttribute**</span></span>
  
> <span data-ttu-id="6ab39-114">Attribut, das der vom **ulPropTag** -Element angegebenen Eigenschaft zugeordnet ist, oder, wenn beim Decodieren eines Kapselungs Blocks das TNEF-Verarbeitungsproblem auftritt, einer der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="6ab39-114">Attribute associated with the property indicated by the **ulPropTag** member or, when the TNEF processing problem occurs when decoding an encapsulation block, one of the following values:</span></span> 
    
 <span data-ttu-id="6ab39-115">_attMAPIProps_</span><span class="sxs-lookup"><span data-stu-id="6ab39-115">_attMAPIProps_</span></span>
  
> <span data-ttu-id="6ab39-116">Nachrichtenebene</span><span class="sxs-lookup"><span data-stu-id="6ab39-116">Message level</span></span>
    
 <span data-ttu-id="6ab39-117">_attAttachment_</span><span class="sxs-lookup"><span data-stu-id="6ab39-117">_attAttachment_</span></span>
  
> <span data-ttu-id="6ab39-118">Anlagenebene</span><span class="sxs-lookup"><span data-stu-id="6ab39-118">Attachment level</span></span>
    
 <span data-ttu-id="6ab39-119">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="6ab39-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="6ab39-120">Property-Tag der Eigenschaft, die das TNEF-Verarbeitungsproblem verursacht hat, außer wenn das Problem beim Decodieren eines Kapselungs Blocks auftritt, in diesem Fall **ulPropTag** auf NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6ab39-120">Property tag of the property that caused the TNEF processing problem, except when the problem occurs when decoding an encapsulation block, in which case **ulPropTag** is set to zero.</span></span> 
    
 <span data-ttu-id="6ab39-121">**SCODE**</span><span class="sxs-lookup"><span data-stu-id="6ab39-121">**scode**</span></span>
  
> <span data-ttu-id="6ab39-122">Fehlerwert, der das während der Verarbeitung auftretende Problem angibt.</span><span class="sxs-lookup"><span data-stu-id="6ab39-122">Error value indicating the problem encountered during processing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6ab39-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ab39-123">Remarks</span></span>

<span data-ttu-id="6ab39-124">Wenn während der Verarbeitung eines Attributs oder einer Eigenschaft keine **STnefProblem** -Struktur generiert wird, kann die Anwendung weiterhin davon ausgehen, dass die Verarbeitung dieses Attributs oder dieser Eigenschaft erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="6ab39-124">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="6ab39-125">Die einzige Ausnahme tritt auf, wenn das Problem während der Decodierung eines Kapselungs Blocks auftrat.</span><span class="sxs-lookup"><span data-stu-id="6ab39-125">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="6ab39-126">In diesem Fall wird die Decodierung der Komponente, die dem Block entspricht, angehalten, und die Decodierung wird in einer anderen Komponente fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="6ab39-126">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6ab39-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ab39-127">See also</span></span>



[<span data-ttu-id="6ab39-128">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="6ab39-128">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="6ab39-129">Kanonische Pidtagattachnumber (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6ab39-129">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)


[<span data-ttu-id="6ab39-130">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="6ab39-130">MAPI Structures</span></span>](mapi-structures.md)

