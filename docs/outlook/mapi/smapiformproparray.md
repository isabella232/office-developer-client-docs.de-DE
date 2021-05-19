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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 50b6581dec8211968a49b204c6d9b1ba1c65bb62
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420066"
---
# <a name="smapiformproparray"></a><span data-ttu-id="01dfd-103">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="01dfd-103">SMAPIFormPropArray</span></span>

  
  
<span data-ttu-id="01dfd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01dfd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01dfd-105">Enthält ein Array von [SMAPIFormProp-Strukturen.](smapiformprop.md)</span><span class="sxs-lookup"><span data-stu-id="01dfd-105">Contains an array of [SMAPIFormProp](smapiformprop.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="01dfd-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="01dfd-106">Header file:</span></span>  <br/> |<span data-ttu-id="01dfd-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="01dfd-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="01dfd-108">Verwandtes Makro:</span><span class="sxs-lookup"><span data-stu-id="01dfd-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="01dfd-109">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="01dfd-109">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cProps;
  ULONG ulPad;
  SMAPIFormProp aFormProp[MAPI_DIM];
} SMAPIFormPropArray, FAR * LPMAPIFORMPROPARRAY;

```

## <a name="members"></a><span data-ttu-id="01dfd-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="01dfd-110">Members</span></span>

 <span data-ttu-id="01dfd-111">**cProps**</span><span class="sxs-lookup"><span data-stu-id="01dfd-111">**cProps**</span></span>
  
> <span data-ttu-id="01dfd-112">Anzahl benannter Eigenschaften im Array im **aFormProp-Element.**</span><span class="sxs-lookup"><span data-stu-id="01dfd-112">Count of named properties in the array in the **aFormProp** member.</span></span> 
    
 <span data-ttu-id="01dfd-113">**ulPad**</span><span class="sxs-lookup"><span data-stu-id="01dfd-113">**ulPad**</span></span>
  
>  <span data-ttu-id="01dfd-114">Acht Bytes Abstand, der verwendet wird, um die richtige Ausrichtung zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="01dfd-114">Eight bytes of padding used to guarantee correct alignment.</span></span> 
    
 <span data-ttu-id="01dfd-115">**aFormProp**</span><span class="sxs-lookup"><span data-stu-id="01dfd-115">**aFormProp**</span></span>
  
> <span data-ttu-id="01dfd-116">Array von Formulareigenschaften.</span><span class="sxs-lookup"><span data-stu-id="01dfd-116">Array of form properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="01dfd-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="01dfd-117">Remarks</span></span>

<span data-ttu-id="01dfd-118">Die **SMAPIFormPropArray-Struktur** wird als Parameter an die folgenden Methoden übergeben:</span><span class="sxs-lookup"><span data-stu-id="01dfd-118">The **SMAPIFormPropArray** structure is passed as a parameter to the following methods:</span></span> 
  
- [<span data-ttu-id="01dfd-119">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="01dfd-119">IMAPIFormInfo::CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md)
    
- [<span data-ttu-id="01dfd-120">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="01dfd-120">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="01dfd-121">IMAPIFormContainer::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="01dfd-121">IMAPIFormContainer::CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a><span data-ttu-id="01dfd-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01dfd-122">See also</span></span>



[<span data-ttu-id="01dfd-123">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="01dfd-123">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md)
  
[<span data-ttu-id="01dfd-124">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="01dfd-124">SMAPIFormProp</span></span>](smapiformprop.md)


[<span data-ttu-id="01dfd-125">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="01dfd-125">MAPI Structures</span></span>](mapi-structures.md)

