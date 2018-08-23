---
title: FBadProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadProp
api_type:
- HeaderDef
ms.assetid: 929330c8-e6f2-4adf-a36e-fba18fa055d4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2fbff399e088edaf3ad864f0ec7fecda3af6bc8e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578850"
---
# <a name="fbadprop"></a><span data-ttu-id="02d60-103">FBadProp</span><span class="sxs-lookup"><span data-stu-id="02d60-103">FBadProp</span></span>

  
  
<span data-ttu-id="02d60-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02d60-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02d60-105">Eine angegebene Eigenschaft überprüft.</span><span class="sxs-lookup"><span data-stu-id="02d60-105">Validates a specified property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="02d60-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="02d60-106">Header file:</span></span>  <br/> |<span data-ttu-id="02d60-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="02d60-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="02d60-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="02d60-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="02d60-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="02d60-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="02d60-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="02d60-110">Called by:</span></span>  <br/> |<span data-ttu-id="02d60-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="02d60-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a><span data-ttu-id="02d60-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="02d60-112">Parameters</span></span>

 <span data-ttu-id="02d60-113">_lpprop_</span><span class="sxs-lookup"><span data-stu-id="02d60-113">_lpprop_</span></span>
  
> <span data-ttu-id="02d60-114">[in] Eine [SPropValue](spropvalue.md) -Struktur definieren die-Eigenschaft überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="02d60-114">[in] An [SPropValue](spropvalue.md) structure defining the property to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="02d60-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="02d60-115">Return value</span></span>

<span data-ttu-id="02d60-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="02d60-116">TRUE</span></span> 
  
> <span data-ttu-id="02d60-117">Die angegebene Eigenschaft ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="02d60-117">The specified property is invalid.</span></span> 
    
<span data-ttu-id="02d60-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="02d60-118">FALSE</span></span> 
  
> <span data-ttu-id="02d60-119">Die angegebene Eigenschaft ist gültig.</span><span class="sxs-lookup"><span data-stu-id="02d60-119">The specified property is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="02d60-120">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="02d60-120">Remarks</span></span>

<span data-ttu-id="02d60-121">Ein Dienstanbieter kann für verschiedene Gründe, beispielsweise um einen Anruf an die [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode eine Eigenschaft bei der Vorbereitung die **FBadProp** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="02d60-121">A service provider can call the **FBadProp** function for several reasons, for example to prepare for a call to the [IMAPIProp::SetProps](imapiprop-setprops.md) method setting a property.</span></span> <span data-ttu-id="02d60-122">**FBadProp** überprüft die angegebene Eigenschaft je nach den Eigenschaftentyp.</span><span class="sxs-lookup"><span data-stu-id="02d60-122">**FBadProp** validates the specified property depending on the property type.</span></span> <span data-ttu-id="02d60-123">Angenommen, wenn die Eigenschaft boolescher Wert ist, **FBadProp** , Sures, dass der Wert TRUE ist oder FALSE.</span><span class="sxs-lookup"><span data-stu-id="02d60-123">For example, if the property is Boolean, **FBadProp** make sures that its value is either TRUE or FALSE.</span></span> <span data-ttu-id="02d60-124">Wenn die Eigenschaft binär ist, **FBadProp** überprüft den Zeiger und die Größe und stellt sicher, dass es korrekt zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="02d60-124">If the property is binary, **FBadProp** checks its pointer and size and makes sure that it is allocated correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="02d60-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02d60-125">See also</span></span>



[<span data-ttu-id="02d60-126">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="02d60-126">FBadPropTag</span></span>](fbadproptag.md)

