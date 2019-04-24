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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b3a0872c94459fc7c24d13e35adf335ef8012182
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357848"
---
# <a name="spropproblem"></a><span data-ttu-id="e0bf8-103">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="e0bf8-103">SPropProblem</span></span>

  
  
<span data-ttu-id="e0bf8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0bf8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0bf8-105">Beschreibt einen Fehler, der sich auf einen Vorgang mit einer Eigenschaft bezieht.</span><span class="sxs-lookup"><span data-stu-id="e0bf8-105">Describes an error that relate to an operation involving a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e0bf8-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="e0bf8-106">Header file:</span></span>  <br/> |<span data-ttu-id="e0bf8-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e0bf8-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropProblem
{
  ULONG ulIndex;
  ULONG ulPropTag;
  SCODE scode;
} SPropProblem, FAR *LPSPropProblem;

```

## <a name="members"></a><span data-ttu-id="e0bf8-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="e0bf8-108">Members</span></span>

 <span data-ttu-id="e0bf8-109">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="e0bf8-109">**ulIndex**</span></span>
  
> <span data-ttu-id="e0bf8-110">Ein Index in einem Array von Property-Tags.</span><span class="sxs-lookup"><span data-stu-id="e0bf8-110">An index in an array of property tags.</span></span>
    
 <span data-ttu-id="e0bf8-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="e0bf8-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="e0bf8-112">Property-Tag für die Eigenschaft mit dem Fehler.</span><span class="sxs-lookup"><span data-stu-id="e0bf8-112">Property tag for the property that has the error.</span></span>
    
 <span data-ttu-id="e0bf8-113">**SCODE**</span><span class="sxs-lookup"><span data-stu-id="e0bf8-113">**scode**</span></span>
  
> <span data-ttu-id="e0bf8-114">Fehlerwert, der das Problem mit der Eigenschaft beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e0bf8-114">Error value describing the problem with the property.</span></span> <span data-ttu-id="e0bf8-115">Dieser Wert kann ein beliebiger MAPI- [SCODE](scode.md) -Wert sein.</span><span class="sxs-lookup"><span data-stu-id="e0bf8-115">This value can be any MAPI [SCODE](scode.md) value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e0bf8-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0bf8-116">Remarks</span></span>

<span data-ttu-id="e0bf8-117">Ein Array von **SPropProblem** -Strukturen wird von den folgenden Methoden zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="e0bf8-117">An array of **SPropProblem** structures is returned from the following methods:</span></span> 
  
- [<span data-ttu-id="e0bf8-118">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="e0bf8-118">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
    
- [<span data-ttu-id="e0bf8-119">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="e0bf8-119">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
    
- [<span data-ttu-id="e0bf8-120">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="e0bf8-120">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
    
- [<span data-ttu-id="e0bf8-121">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="e0bf8-121">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="e0bf8-122">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="e0bf8-122">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
- [<span data-ttu-id="e0bf8-123">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="e0bf8-123">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="e0bf8-124">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="e0bf8-124">IPropData::HrAddObjProps</span></span>](ipropdata-hraddobjprops.md)
    
<span data-ttu-id="e0bf8-125">Eine **SPropProblem** -Struktur enthält einen **SCODE** -Fehlerwert, der aus einem Vorgang resultiert, der versucht, eine MAPI-Eigenschaft zu ändern oder zu löschen.</span><span class="sxs-lookup"><span data-stu-id="e0bf8-125">An **SPropProblem** structure contains an **SCODE** error value that results from an operation trying to modify or delete a MAPI property.</span></span> 
  
<span data-ttu-id="e0bf8-126">Weitere Informationen zur Funktionsweise der **SPropProblem** -Struktur mit Fehlern im Zusammenhang mit Eigenschaften finden Sie unter [MAPI Named Properties](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="e0bf8-126">For more information about how the **SPropProblem** structure works with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e0bf8-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0bf8-127">See also</span></span>



[<span data-ttu-id="e0bf8-128">SCODE</span><span class="sxs-lookup"><span data-stu-id="e0bf8-128">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="e0bf8-129">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="e0bf8-129">SPropProblemArray</span></span>](spropproblemarray.md)


[<span data-ttu-id="e0bf8-130">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="e0bf8-130">MAPI Structures</span></span>](mapi-structures.md)

