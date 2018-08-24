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
ms.openlocfilehash: 943dab0141581adc32c184b0042a063a4ec05c3e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582882"
---
# <a name="fbadproptag"></a><span data-ttu-id="f91b3-103">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="f91b3-103">FBadPropTag</span></span>

  
  
<span data-ttu-id="f91b3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f91b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f91b3-105">Überprüft ein Tag für die angegebene Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f91b3-105">Validates a specified property tag.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f91b3-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="f91b3-106">Header file:</span></span>  <br/> |<span data-ttu-id="f91b3-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="f91b3-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="f91b3-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="f91b3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f91b3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f91b3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f91b3-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="f91b3-110">Called by:</span></span>  <br/> |<span data-ttu-id="f91b3-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="f91b3-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="f91b3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f91b3-112">Parameters</span></span>

 <span data-ttu-id="f91b3-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="f91b3-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="f91b3-114">[in] Die Eigenschaftentag überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="f91b3-114">[in] The property tag to be validated.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f91b3-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="f91b3-115">Return value</span></span>

<span data-ttu-id="f91b3-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="f91b3-116">TRUE</span></span> 
  
> <span data-ttu-id="f91b3-117">Das Tag für die angegebene Eigenschaft ist kein gültiges Tag der MAPI-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f91b3-117">The specified property tag is not a valid MAPI property tag.</span></span> 
    
<span data-ttu-id="f91b3-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="f91b3-118">FALSE</span></span> 
  
> <span data-ttu-id="f91b3-119">Das Tag für die angegebene Eigenschaft ist ein gültiges Tag der MAPI-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f91b3-119">The specified property tag is a valid MAPI property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f91b3-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f91b3-120">Remarks</span></span>

<span data-ttu-id="f91b3-121">Die Funktion **FBadPropTag** überprüft das angegebene Eigenschaftstag basierend auf MAPI-Definitionen.</span><span class="sxs-lookup"><span data-stu-id="f91b3-121">The **FBadPropTag** function validates the specified property tag based on MAPI definitions.</span></span> <span data-ttu-id="f91b3-122">Sures, die von der Eigenschaftstyp ist eine der Typen, die durch MAPI und die Bezeichner der wird definiert, um dieses Typs werden, erleichtern.</span><span class="sxs-lookup"><span data-stu-id="f91b3-122">It make sures that the property type is one of the types defined by MAPI and that the property identifier is defined to be of that type.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f91b3-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f91b3-123">See also</span></span>



[<span data-ttu-id="f91b3-124">FBadProp</span><span class="sxs-lookup"><span data-stu-id="f91b3-124">FBadProp</span></span>](fbadprop.md)

