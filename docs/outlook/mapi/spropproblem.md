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
ms.openlocfilehash: 7c19cce33ec351a5627870782ebb4fe509a98be2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573285"
---
# <a name="spropproblem"></a><span data-ttu-id="12e8f-103">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="12e8f-103">SPropProblem</span></span>

  
  
<span data-ttu-id="12e8f-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12e8f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12e8f-105">Beschreibt einen Fehler, die einen Vorgang im Zusammenhang mit einer Eigenschaft zuordnen.</span><span class="sxs-lookup"><span data-stu-id="12e8f-105">Describes an error that relate to an operation involving a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="12e8f-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="12e8f-106">Header file:</span></span>  <br/> |<span data-ttu-id="12e8f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="12e8f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropProblem
{
  ULONG ulIndex;
  ULONG ulPropTag;
  SCODE scode;
} SPropProblem, FAR *LPSPropProblem;

```

## <a name="members"></a><span data-ttu-id="12e8f-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="12e8f-108">Members</span></span>

 <span data-ttu-id="12e8f-109">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="12e8f-109">**ulIndex**</span></span>
  
> <span data-ttu-id="12e8f-110">Ein Index in einem Array von Eigenschaftentags.</span><span class="sxs-lookup"><span data-stu-id="12e8f-110">An index in an array of property tags.</span></span>
    
 <span data-ttu-id="12e8f-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="12e8f-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="12e8f-112">Eigenschaftentag für die Eigenschaft, die den Fehler hat.</span><span class="sxs-lookup"><span data-stu-id="12e8f-112">Property tag for the property that has the error.</span></span>
    
 <span data-ttu-id="12e8f-113">**SCODE**</span><span class="sxs-lookup"><span data-stu-id="12e8f-113">**scode**</span></span>
  
> <span data-ttu-id="12e8f-114">Fehlerwert Beschreibung des Problems mit der-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="12e8f-114">Error value describing the problem with the property.</span></span> <span data-ttu-id="12e8f-115">Dieser Wert kann einen beliebigen MAPI [SCODE](scode.md) -Wert sein.</span><span class="sxs-lookup"><span data-stu-id="12e8f-115">This value can be any MAPI [SCODE](scode.md) value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="12e8f-116">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="12e8f-116">Remarks</span></span>

<span data-ttu-id="12e8f-117">Ein Array von **SPropProblem** Strukturen wird von folgenden Methoden zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="12e8f-117">An array of **SPropProblem** structures is returned from the following methods:</span></span> 
  
- [<span data-ttu-id="12e8f-118">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="12e8f-118">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
    
- [<span data-ttu-id="12e8f-119">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="12e8f-119">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
    
- [<span data-ttu-id="12e8f-120">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="12e8f-120">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
    
- [<span data-ttu-id="12e8f-121">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="12e8f-121">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="12e8f-122">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="12e8f-122">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
- [<span data-ttu-id="12e8f-123">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="12e8f-123">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="12e8f-124">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="12e8f-124">IPropData::HrAddObjProps</span></span>](ipropdata-hraddobjprops.md)
    
<span data-ttu-id="12e8f-125">Eine **SPropProblem** -Struktur enthält einen **SCODE** Fehlerwert, der einen Vorgang versucht, ändern oder Löschen einer MAPI-Eigenschaft ergibt.</span><span class="sxs-lookup"><span data-stu-id="12e8f-125">An **SPropProblem** structure contains an **SCODE** error value that results from an operation trying to modify or delete a MAPI property.</span></span> 
  
<span data-ttu-id="12e8f-126">Weitere Informationen zur Funktionsweise der **SPropProblem** -Struktur mit Fehlern im Zusammenhang mit Eigenschaften finden Sie unter [MAPI-Eigenschaften mit dem Namen](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="12e8f-126">For more information about how the **SPropProblem** structure works with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="12e8f-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12e8f-127">See also</span></span>



[<span data-ttu-id="12e8f-128">SCODE</span><span class="sxs-lookup"><span data-stu-id="12e8f-128">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="12e8f-129">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="12e8f-129">SPropProblemArray</span></span>](spropproblemarray.md)


[<span data-ttu-id="12e8f-130">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="12e8f-130">MAPI Structures</span></span>](mapi-structures.md)

