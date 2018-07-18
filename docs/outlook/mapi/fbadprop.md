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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 39e10e9139036cc86ec93ea24a89b98125ea6e83
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791650"
---
# <a name="fbadprop"></a><span data-ttu-id="64b47-103">FBadProp</span><span class="sxs-lookup"><span data-stu-id="64b47-103">FBadProp</span></span>

  
  
<span data-ttu-id="64b47-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="64b47-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="64b47-105">Eine angegebene Eigenschaft überprüft.</span><span class="sxs-lookup"><span data-stu-id="64b47-105">Validates a specified property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="64b47-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="64b47-106">Header file:</span></span>  <br/> |<span data-ttu-id="64b47-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="64b47-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="64b47-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="64b47-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="64b47-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="64b47-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="64b47-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="64b47-110">Called by:</span></span>  <br/> |<span data-ttu-id="64b47-111">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="64b47-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a><span data-ttu-id="64b47-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="64b47-112">Parameters</span></span>

 <span data-ttu-id="64b47-113">_lpprop_</span><span class="sxs-lookup"><span data-stu-id="64b47-113">_lpprop_</span></span>
  
> <span data-ttu-id="64b47-114">[in] Eine [SPropValue](spropvalue.md) -Struktur definieren die-Eigenschaft überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="64b47-114">[in] An [SPropValue](spropvalue.md) structure defining the property to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="64b47-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="64b47-115">Return value</span></span>

<span data-ttu-id="64b47-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="64b47-116">TRUE</span></span> 
  
> <span data-ttu-id="64b47-117">Die angegebene Eigenschaft ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="64b47-117">The specified property is invalid.</span></span> 
    
<span data-ttu-id="64b47-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="64b47-118">FALSE</span></span> 
  
> <span data-ttu-id="64b47-119">Die angegebene Eigenschaft ist gültig.</span><span class="sxs-lookup"><span data-stu-id="64b47-119">The specified property is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="64b47-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64b47-120">Remarks</span></span>

<span data-ttu-id="64b47-121">Ein Dienstanbieter kann für verschiedene Gründe, beispielsweise um einen Anruf an die [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode eine Eigenschaft bei der Vorbereitung die **FBadProp** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="64b47-121">A service provider can call the **FBadProp** function for several reasons, for example to prepare for a call to the [IMAPIProp::SetProps](imapiprop-setprops.md) method setting a property.</span></span> <span data-ttu-id="64b47-122">**FBadProp** überprüft die angegebene Eigenschaft je nach den Eigenschaftentyp.</span><span class="sxs-lookup"><span data-stu-id="64b47-122">**FBadProp** validates the specified property depending on the property type.</span></span> <span data-ttu-id="64b47-123">Angenommen, wenn die Eigenschaft boolescher Wert ist, **FBadProp** , Sures, dass der Wert TRUE ist oder FALSE.</span><span class="sxs-lookup"><span data-stu-id="64b47-123">For example, if the property is Boolean, **FBadProp** make sures that its value is either TRUE or FALSE.</span></span> <span data-ttu-id="64b47-124">Wenn die Eigenschaft binär ist, **FBadProp** überprüft den Zeiger und die Größe und stellt sicher, dass es korrekt zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="64b47-124">If the property is binary, **FBadProp** checks its pointer and size and makes sure that it is allocated correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="64b47-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64b47-125">See also</span></span>



[<span data-ttu-id="64b47-126">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="64b47-126">FBadPropTag</span></span>](fbadproptag.md)

