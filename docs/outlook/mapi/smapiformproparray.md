---
title: SMAPIFormPropArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormPropArray
api_type:
- COM
ms.assetid: bb243bc4-4974-4ad6-aa76-2426c1ebe84b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d907f2e8ecb9b6126898ff35b13427b088af9561
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795579"
---
# <a name="smapiformproparray"></a><span data-ttu-id="ad51c-103">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="ad51c-103">SMAPIFormPropArray</span></span>

  
  
<span data-ttu-id="ad51c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ad51c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ad51c-105">Enthält ein Array von [SMAPIFormProp](smapiformprop.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="ad51c-105">Contains an array of [SMAPIFormProp](smapiformprop.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ad51c-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="ad51c-106">Header file:</span></span>  <br/> |<span data-ttu-id="ad51c-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="ad51c-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="ad51c-108">Verwandte Makro:</span><span class="sxs-lookup"><span data-stu-id="ad51c-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="ad51c-109">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="ad51c-109">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cProps;
  ULONG ulPad;
  SMAPIFormProp aFormProp[MAPI_DIM];
} SMAPIFormPropArray, FAR * LPMAPIFORMPROPARRAY;

```

## <a name="members"></a><span data-ttu-id="ad51c-110">Members</span><span class="sxs-lookup"><span data-stu-id="ad51c-110">Members</span></span>

 <span data-ttu-id="ad51c-111">**cProps**</span><span class="sxs-lookup"><span data-stu-id="ad51c-111">**cProps**</span></span>
  
> <span data-ttu-id="ad51c-112">Anzahl der benannten Eigenschaften im Array in der **aFormProp** Member.</span><span class="sxs-lookup"><span data-stu-id="ad51c-112">Count of named properties in the array in the **aFormProp** member.</span></span> 
    
 <span data-ttu-id="ad51c-113">**ulPad**</span><span class="sxs-lookup"><span data-stu-id="ad51c-113">**ulPad**</span></span>
  
>  <span data-ttu-id="ad51c-114">Acht Bytes an Füllzeichen verwendet, um die richtige Ausrichtung zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="ad51c-114">Eight bytes of padding used to guarantee correct alignment.</span></span> 
    
 <span data-ttu-id="ad51c-115">**aFormProp**</span><span class="sxs-lookup"><span data-stu-id="ad51c-115">**aFormProp**</span></span>
  
> <span data-ttu-id="ad51c-116">Array von Formulareigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ad51c-116">Array of form properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ad51c-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ad51c-117">Remarks</span></span>

<span data-ttu-id="ad51c-118">Die Struktur **SMAPIFormPropArray** wird als Parameter an die folgenden Methoden übergeben:</span><span class="sxs-lookup"><span data-stu-id="ad51c-118">The **SMAPIFormPropArray** structure is passed as a parameter to the following methods:</span></span> 
  
- [<span data-ttu-id="ad51c-119">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="ad51c-119">IMAPIFormInfo::CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md)
    
- [<span data-ttu-id="ad51c-120">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="ad51c-120">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="ad51c-121">IMAPIFormContainer::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="ad51c-121">IMAPIFormContainer::CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a><span data-ttu-id="ad51c-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad51c-122">See also</span></span>



[<span data-ttu-id="ad51c-123">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="ad51c-123">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md)
  
[<span data-ttu-id="ad51c-124">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="ad51c-124">SMAPIFormProp</span></span>](smapiformprop.md)


[<span data-ttu-id="ad51c-125">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="ad51c-125">MAPI Structures</span></span>](mapi-structures.md)

