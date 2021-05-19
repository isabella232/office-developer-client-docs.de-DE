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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9764be2788db8d2649be8708cad4ec67a85af845
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433647"
---
# <a name="fbadproptag"></a><span data-ttu-id="c1828-103">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="c1828-103">FBadPropTag</span></span>

  
  
<span data-ttu-id="c1828-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1828-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1828-105">Überprüft ein angegebenes Eigenschaftstag.</span><span class="sxs-lookup"><span data-stu-id="c1828-105">Validates a specified property tag.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c1828-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="c1828-106">Header file:</span></span>  <br/> |<span data-ttu-id="c1828-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="c1828-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="c1828-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="c1828-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c1828-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c1828-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c1828-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="c1828-110">Called by:</span></span>  <br/> |<span data-ttu-id="c1828-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="c1828-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="c1828-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1828-112">Parameters</span></span>

 <span data-ttu-id="c1828-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="c1828-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="c1828-114">[in] Das zu überprüfende Eigenschaftstag.</span><span class="sxs-lookup"><span data-stu-id="c1828-114">[in] The property tag to be validated.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c1828-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1828-115">Return value</span></span>

<span data-ttu-id="c1828-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="c1828-116">TRUE</span></span> 
  
> <span data-ttu-id="c1828-117">Das angegebene Eigenschaftstag ist kein gültiges MAPI-Eigenschaftstag.</span><span class="sxs-lookup"><span data-stu-id="c1828-117">The specified property tag is not a valid MAPI property tag.</span></span> 
    
<span data-ttu-id="c1828-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="c1828-118">FALSE</span></span> 
  
> <span data-ttu-id="c1828-119">Das angegebene Eigenschaftstag ist ein gültiges MAPI-Eigenschaftstag.</span><span class="sxs-lookup"><span data-stu-id="c1828-119">The specified property tag is a valid MAPI property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c1828-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c1828-120">Remarks</span></span>

<span data-ttu-id="c1828-121">Die **FBadPropTag-Funktion** überprüft das angegebene Eigenschaftstag basierend auf MAPI-Definitionen.</span><span class="sxs-lookup"><span data-stu-id="c1828-121">The **FBadPropTag** function validates the specified property tag based on MAPI definitions.</span></span> <span data-ttu-id="c1828-122">Es wird sichergestellt, dass der Eigenschaftentyp einer der von MAPI definierten Typen ist und dass der Eigenschaftenbezeichner für diesen Typ definiert ist.</span><span class="sxs-lookup"><span data-stu-id="c1828-122">It make sures that the property type is one of the types defined by MAPI and that the property identifier is defined to be of that type.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c1828-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1828-123">See also</span></span>



[<span data-ttu-id="c1828-124">FBadProp</span><span class="sxs-lookup"><span data-stu-id="c1828-124">FBadProp</span></span>](fbadprop.md)

