---
title: LpValFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 67461a38-bb60-467b-901b-39c645e764f7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d7601eb50818fa6f39384a6b024215fc4917e83a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792904"
---
# <a name="lpvalfindprop"></a><span data-ttu-id="7f5e2-103">LpValFindProp</span><span class="sxs-lookup"><span data-stu-id="7f5e2-103">LpValFindProp</span></span>

  
  
<span data-ttu-id="7f5e2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7f5e2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7f5e2-105">Sucht nach einer angegebenen Eigenschaft in einer Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="7f5e2-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7f5e2-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="7f5e2-106">Header file:</span></span>  <br/> |<span data-ttu-id="7f5e2-107">mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="7f5e2-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7f5e2-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="7f5e2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7f5e2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7f5e2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7f5e2-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="7f5e2-110">Called by:</span></span>  <br/> |<span data-ttu-id="7f5e2-111">Clientanwendungen und -Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="7f5e2-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="7f5e2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f5e2-112">Parameters</span></span>

 <span data-ttu-id="7f5e2-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="7f5e2-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="7f5e2-114">[in] Tag für die Eigenschaft in den durch den _LpPropArray_ -Parameter angegebenen Eigenschaftensatz suchen.</span><span class="sxs-lookup"><span data-stu-id="7f5e2-114">[in] Tag for the property to search for in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="7f5e2-115">_cValues_</span><span class="sxs-lookup"><span data-stu-id="7f5e2-115">_cValues_</span></span>
  
> <span data-ttu-id="7f5e2-116">[in] Anzahl der Eigenschaften in den Eigenschaftensatz durch den Parameter _LpPropArray_ angegeben.</span><span class="sxs-lookup"><span data-stu-id="7f5e2-116">[in] Count of properties in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="7f5e2-117">_lpPropArray_</span><span class="sxs-lookup"><span data-stu-id="7f5e2-117">_lpPropArray_</span></span>
  
> <span data-ttu-id="7f5e2-118">[in] Ein Array von **SPropValue** -Strukturen, die die Eigenschaften des zu durchsuchenden definiert.</span><span class="sxs-lookup"><span data-stu-id="7f5e2-118">[in] Array of **SPropValue** structures that defines the properties to be searched.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7f5e2-119">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="7f5e2-119">Return value</span></span>

<span data-ttu-id="7f5e2-120">Die **LpValFindProp** -Funktion gibt eine **SPropValue** -Struktur, die die Eigenschaft, die dem input-Eigenschaftentag übereinstimmt definiert, oder NULL, wenn keine Übereinstimmung vorliegt.</span><span class="sxs-lookup"><span data-stu-id="7f5e2-120">The **LpValFindProp** function returns an **SPropValue** structure that defines the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7f5e2-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7f5e2-121">Remarks</span></span>

<span data-ttu-id="7f5e2-122">Die **LpValFindProp** -Funktion ist identisch mit **PpropFindProp**.</span><span class="sxs-lookup"><span data-stu-id="7f5e2-122">The **LpValFindProp** function is identical to **PpropFindProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7f5e2-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f5e2-123">See also</span></span>



[<span data-ttu-id="7f5e2-124">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="7f5e2-124">PpropFindProp</span></span>](ppropfindprop.md)
  
[<span data-ttu-id="7f5e2-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7f5e2-125">SPropValue</span></span>](spropvalue.md)

