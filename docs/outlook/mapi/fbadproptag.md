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
ms.openlocfilehash: d1503aaa5bddd23a90035219901e1dc232dbd026
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791662"
---
# <a name="fbadproptag"></a><span data-ttu-id="93a16-103">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="93a16-103">FBadPropTag</span></span>

  
  
<span data-ttu-id="93a16-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="93a16-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="93a16-105">Überprüft ein Tag für die angegebene Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="93a16-105">Validates a specified property tag.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="93a16-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="93a16-106">Header file:</span></span>  <br/> |<span data-ttu-id="93a16-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="93a16-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="93a16-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="93a16-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="93a16-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="93a16-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="93a16-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="93a16-110">Called by:</span></span>  <br/> |<span data-ttu-id="93a16-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="93a16-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="93a16-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="93a16-112">Parameters</span></span>

 <span data-ttu-id="93a16-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="93a16-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="93a16-114">[in] Die Eigenschaftentag überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="93a16-114">[in] The property tag to be validated.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="93a16-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="93a16-115">Return value</span></span>

<span data-ttu-id="93a16-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="93a16-116">TRUE</span></span> 
  
> <span data-ttu-id="93a16-117">Das Tag für die angegebene Eigenschaft ist kein gültiges Tag der MAPI-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="93a16-117">The specified property tag is not a valid MAPI property tag.</span></span> 
    
<span data-ttu-id="93a16-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="93a16-118">FALSE</span></span> 
  
> <span data-ttu-id="93a16-119">Das Tag für die angegebene Eigenschaft ist ein gültiges Tag der MAPI-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="93a16-119">The specified property tag is a valid MAPI property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="93a16-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="93a16-120">Remarks</span></span>

<span data-ttu-id="93a16-121">Die Funktion **FBadPropTag** überprüft das angegebene Eigenschaftstag basierend auf MAPI-Definitionen.</span><span class="sxs-lookup"><span data-stu-id="93a16-121">The **FBadPropTag** function validates the specified property tag based on MAPI definitions.</span></span> <span data-ttu-id="93a16-122">Sures, die von der Eigenschaftstyp ist eine der Typen, die durch MAPI und die Bezeichner der wird definiert, um dieses Typs werden, erleichtern.</span><span class="sxs-lookup"><span data-stu-id="93a16-122">It make sures that the property type is one of the types defined by MAPI and that the property identifier is defined to be of that type.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="93a16-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93a16-123">See also</span></span>



[<span data-ttu-id="93a16-124">FBadProp</span><span class="sxs-lookup"><span data-stu-id="93a16-124">FBadProp</span></span>](fbadprop.md)

