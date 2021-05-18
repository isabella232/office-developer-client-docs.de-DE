---
title: SPropProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropProblem
api_type:
- COM
ms.assetid: 55943197-fd11-442d-bb4b-0bff565b846e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b3a0872c94459fc7c24d13e35adf335ef8012182
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407774"
---
# <a name="spropproblem"></a><span data-ttu-id="678d5-103">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="678d5-103">SPropProblem</span></span>

  
  
<span data-ttu-id="678d5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="678d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="678d5-105">Beschreibt einen Fehler, der sich auf einen Vorgang mit einer Eigenschaft bezieht.</span><span class="sxs-lookup"><span data-stu-id="678d5-105">Describes an error that relate to an operation involving a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="678d5-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="678d5-106">Header file:</span></span>  <br/> |<span data-ttu-id="678d5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="678d5-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropProblem
{
  ULONG ulIndex;
  ULONG ulPropTag;
  SCODE scode;
} SPropProblem, FAR *LPSPropProblem;

```

## <a name="members"></a><span data-ttu-id="678d5-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="678d5-108">Members</span></span>

 <span data-ttu-id="678d5-109">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="678d5-109">**ulIndex**</span></span>
  
> <span data-ttu-id="678d5-110">Ein Index in einem Array von Eigenschaftstags.</span><span class="sxs-lookup"><span data-stu-id="678d5-110">An index in an array of property tags.</span></span>
    
 <span data-ttu-id="678d5-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="678d5-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="678d5-112">Property-Tag für die Eigenschaft, die den Fehler hat.</span><span class="sxs-lookup"><span data-stu-id="678d5-112">Property tag for the property that has the error.</span></span>
    
 <span data-ttu-id="678d5-113">**scode**</span><span class="sxs-lookup"><span data-stu-id="678d5-113">**scode**</span></span>
  
> <span data-ttu-id="678d5-114">Fehlerwert, der das Problem mit der Eigenschaft beschreibt.</span><span class="sxs-lookup"><span data-stu-id="678d5-114">Error value describing the problem with the property.</span></span> <span data-ttu-id="678d5-115">Dieser Wert kann ein beliebiger [MAPI-SCODE-Wert](scode.md) sein.</span><span class="sxs-lookup"><span data-stu-id="678d5-115">This value can be any MAPI [SCODE](scode.md) value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="678d5-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="678d5-116">Remarks</span></span>

<span data-ttu-id="678d5-117">Ein Array von **SPropProblem-Strukturen** wird von den folgenden Methoden zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="678d5-117">An array of **SPropProblem** structures is returned from the following methods:</span></span> 
  
- [<span data-ttu-id="678d5-118">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="678d5-118">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
    
- [<span data-ttu-id="678d5-119">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="678d5-119">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
    
- [<span data-ttu-id="678d5-120">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="678d5-120">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
    
- [<span data-ttu-id="678d5-121">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="678d5-121">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="678d5-122">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="678d5-122">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
- [<span data-ttu-id="678d5-123">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="678d5-123">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="678d5-124">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="678d5-124">IPropData::HrAddObjProps</span></span>](ipropdata-hraddobjprops.md)
    
<span data-ttu-id="678d5-125">Eine **SPropProblem-Struktur** enthält einen **SCODE-Fehlerwert,** der aus einem Vorgang resultiert, der versucht, eine MAPI-Eigenschaft zu ändern oder zu löschen.</span><span class="sxs-lookup"><span data-stu-id="678d5-125">An **SPropProblem** structure contains an **SCODE** error value that results from an operation trying to modify or delete a MAPI property.</span></span> 
  
<span data-ttu-id="678d5-126">Weitere Informationen zur Funktionsweise der **SPropProblem-Struktur** mit Fehlern im Zusammenhang mit Eigenschaften finden Sie unter [MAPI Named Properties](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="678d5-126">For more information about how the **SPropProblem** structure works with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="678d5-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="678d5-127">See also</span></span>



[<span data-ttu-id="678d5-128">SCODE</span><span class="sxs-lookup"><span data-stu-id="678d5-128">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="678d5-129">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="678d5-129">SPropProblemArray</span></span>](spropproblemarray.md)


[<span data-ttu-id="678d5-130">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="678d5-130">MAPI Structures</span></span>](mapi-structures.md)

