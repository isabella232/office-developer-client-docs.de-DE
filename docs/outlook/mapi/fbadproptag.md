---
title: FBadPropTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadPropTag
api_type:
- HeaderDef
ms.assetid: 143bd3c6-5a55-4122-8522-9c48473aa781
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9764be2788db8d2649be8708cad4ec67a85af845
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340999"
---
# <a name="fbadproptag"></a><span data-ttu-id="f3277-103">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="f3277-103">FBadPropTag</span></span>

  
  
<span data-ttu-id="f3277-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3277-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3277-105">Überprüft ein angegebenes Property-Tag.</span><span class="sxs-lookup"><span data-stu-id="f3277-105">Validates a specified property tag.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f3277-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="f3277-106">Header file:</span></span>  <br/> |<span data-ttu-id="f3277-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="f3277-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="f3277-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="f3277-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f3277-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f3277-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f3277-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="f3277-110">Called by:</span></span>  <br/> |<span data-ttu-id="f3277-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="f3277-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="f3277-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3277-112">Parameters</span></span>

 <span data-ttu-id="f3277-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="f3277-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="f3277-114">in Das zu überprüfende Property-Tag.</span><span class="sxs-lookup"><span data-stu-id="f3277-114">[in] The property tag to be validated.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f3277-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f3277-115">Return value</span></span>

<span data-ttu-id="f3277-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="f3277-116">TRUE</span></span> 
  
> <span data-ttu-id="f3277-117">Das angegebene Property-Tag ist kein gültiges MAPI-Eigenschafts.</span><span class="sxs-lookup"><span data-stu-id="f3277-117">The specified property tag is not a valid MAPI property tag.</span></span> 
    
<span data-ttu-id="f3277-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="f3277-118">FALSE</span></span> 
  
> <span data-ttu-id="f3277-119">Das angegebene Property-Tag ist ein gültiges MAPI-Eigenschafts.</span><span class="sxs-lookup"><span data-stu-id="f3277-119">The specified property tag is a valid MAPI property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f3277-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3277-120">Remarks</span></span>

<span data-ttu-id="f3277-121">Die **FBadPropTag** -Funktion überprüft das angegebene Property-Tag basierend auf MAPI-Definitionen.</span><span class="sxs-lookup"><span data-stu-id="f3277-121">The **FBadPropTag** function validates the specified property tag based on MAPI definitions.</span></span> <span data-ttu-id="f3277-122">Sie stellen sicher, dass der Eigenschaftentyp einer der von MAPI definierten Typen ist und dass der Eigenschaftenbezeichner für diesen Typ definiert ist.</span><span class="sxs-lookup"><span data-stu-id="f3277-122">It make sures that the property type is one of the types defined by MAPI and that the property identifier is defined to be of that type.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f3277-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3277-123">See also</span></span>



[<span data-ttu-id="f3277-124">FBadProp</span><span class="sxs-lookup"><span data-stu-id="f3277-124">FBadProp</span></span>](fbadprop.md)

