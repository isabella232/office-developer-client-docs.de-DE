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
ms.openlocfilehash: 50b6581dec8211968a49b204c6d9b1ba1c65bb62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309513"
---
# <a name="smapiformproparray"></a><span data-ttu-id="1e663-103">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="1e663-103">SMAPIFormPropArray</span></span>

  
  
<span data-ttu-id="1e663-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e663-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e663-105">Enthält ein Array von [SMAPIFormProp](smapiformprop.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="1e663-105">Contains an array of [SMAPIFormProp](smapiformprop.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1e663-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="1e663-106">Header file:</span></span>  <br/> |<span data-ttu-id="1e663-107">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="1e663-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="1e663-108">Zugehöriges Makro:</span><span class="sxs-lookup"><span data-stu-id="1e663-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="1e663-109">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="1e663-109">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cProps;
  ULONG ulPad;
  SMAPIFormProp aFormProp[MAPI_DIM];
} SMAPIFormPropArray, FAR * LPMAPIFORMPROPARRAY;

```

## <a name="members"></a><span data-ttu-id="1e663-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="1e663-110">Members</span></span>

 <span data-ttu-id="1e663-111">**cProps**</span><span class="sxs-lookup"><span data-stu-id="1e663-111">**cProps**</span></span>
  
> <span data-ttu-id="1e663-112">Die Anzahl benannter Eigenschaften im Array im **aFormProp** -Element.</span><span class="sxs-lookup"><span data-stu-id="1e663-112">Count of named properties in the array in the **aFormProp** member.</span></span> 
    
 <span data-ttu-id="1e663-113">**ulPad**</span><span class="sxs-lookup"><span data-stu-id="1e663-113">**ulPad**</span></span>
  
>  <span data-ttu-id="1e663-114">Acht Byte Leerraum, die verwendet werden, um eine korrekte Ausrichtung zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="1e663-114">Eight bytes of padding used to guarantee correct alignment.</span></span> 
    
 <span data-ttu-id="1e663-115">**aFormProp**</span><span class="sxs-lookup"><span data-stu-id="1e663-115">**aFormProp**</span></span>
  
> <span data-ttu-id="1e663-116">Array von Formulareigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1e663-116">Array of form properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1e663-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e663-117">Remarks</span></span>

<span data-ttu-id="1e663-118">Die **SMAPIFormPropArray** -Struktur wird als Parameter an die folgenden Methoden übergeben:</span><span class="sxs-lookup"><span data-stu-id="1e663-118">The **SMAPIFormPropArray** structure is passed as a parameter to the following methods:</span></span> 
  
- [<span data-ttu-id="1e663-119">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="1e663-119">IMAPIFormInfo::CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md)
    
- [<span data-ttu-id="1e663-120">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="1e663-120">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="1e663-121">IMAPIFormContainer::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="1e663-121">IMAPIFormContainer::CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a><span data-ttu-id="1e663-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e663-122">See also</span></span>



[<span data-ttu-id="1e663-123">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="1e663-123">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md)
  
[<span data-ttu-id="1e663-124">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="1e663-124">SMAPIFormProp</span></span>](smapiformprop.md)


[<span data-ttu-id="1e663-125">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="1e663-125">MAPI Structures</span></span>](mapi-structures.md)

