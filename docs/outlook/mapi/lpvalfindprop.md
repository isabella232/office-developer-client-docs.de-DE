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
ms.openlocfilehash: fa1588d4a58824b57c132fc8e66a0abd6e9acd0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357428"
---
# <a name="lpvalfindprop"></a><span data-ttu-id="d87f6-103">LpValFindProp</span><span class="sxs-lookup"><span data-stu-id="d87f6-103">LpValFindProp</span></span>

  
  
<span data-ttu-id="d87f6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d87f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d87f6-105">Sucht nach einer angegebenen Eigenschaft in einem Eigenschaftensatz.</span><span class="sxs-lookup"><span data-stu-id="d87f6-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d87f6-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="d87f6-106">Header file:</span></span>  <br/> |<span data-ttu-id="d87f6-107">mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="d87f6-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d87f6-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="d87f6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d87f6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d87f6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d87f6-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="d87f6-110">Called by:</span></span>  <br/> |<span data-ttu-id="d87f6-111">Client Anwendungen und Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="d87f6-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="d87f6-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d87f6-112">Parameters</span></span>

 <span data-ttu-id="d87f6-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="d87f6-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="d87f6-114">in -Tag für die Eigenschaft, nach der im Eigenschaftensatz gesucht werden soll, angegeben durch den _lpPropArray_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="d87f6-114">[in] Tag for the property to search for in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="d87f6-115">_cValues_</span><span class="sxs-lookup"><span data-stu-id="d87f6-115">_cValues_</span></span>
  
> <span data-ttu-id="d87f6-116">in Die Anzahl der Eigenschaften im Eigenschaftensatz, angegeben durch den _lpPropArray_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="d87f6-116">[in] Count of properties in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="d87f6-117">_lpPropArray_</span><span class="sxs-lookup"><span data-stu-id="d87f6-117">_lpPropArray_</span></span>
  
> <span data-ttu-id="d87f6-118">in Array von **SPropValue** -Strukturen, die die zu durchsuchenden Eigenschaften definieren.</span><span class="sxs-lookup"><span data-stu-id="d87f6-118">[in] Array of **SPropValue** structures that defines the properties to be searched.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d87f6-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d87f6-119">Return value</span></span>

<span data-ttu-id="d87f6-120">Die **LpValFindProp** -Funktion gibt eine **SPropValue** -Struktur zurück, die die Eigenschaft definiert, die mit dem Eingabe Eigenschafts übereinstimmt, oder NULL, wenn keine Übereinstimmung vorliegt.</span><span class="sxs-lookup"><span data-stu-id="d87f6-120">The **LpValFindProp** function returns an **SPropValue** structure that defines the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d87f6-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d87f6-121">Remarks</span></span>

<span data-ttu-id="d87f6-122">Die **LpValFindProp** -Funktion ist identisch mit **PpropFindProp**.</span><span class="sxs-lookup"><span data-stu-id="d87f6-122">The **LpValFindProp** function is identical to **PpropFindProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d87f6-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d87f6-123">See also</span></span>



[<span data-ttu-id="d87f6-124">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="d87f6-124">PpropFindProp</span></span>](ppropfindprop.md)
  
[<span data-ttu-id="d87f6-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d87f6-125">SPropValue</span></span>](spropvalue.md)

