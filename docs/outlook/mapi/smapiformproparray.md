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
# <a name="smapiformproparray"></a><span data-ttu-id="9f3c7-103">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="9f3c7-103">SMAPIFormPropArray</span></span>

  
  
<span data-ttu-id="9f3c7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f3c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f3c7-105">Enthält ein Array von [SMAPIFormProp](smapiformprop.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="9f3c7-105">Contains an array of [SMAPIFormProp](smapiformprop.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9f3c7-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="9f3c7-106">Header file:</span></span>  <br/> |<span data-ttu-id="9f3c7-107">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="9f3c7-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="9f3c7-108">Zugehöriges Makro:</span><span class="sxs-lookup"><span data-stu-id="9f3c7-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="9f3c7-109">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="9f3c7-109">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cProps;
  ULONG ulPad;
  SMAPIFormProp aFormProp[MAPI_DIM];
} SMAPIFormPropArray, FAR * LPMAPIFORMPROPARRAY;

```

## <a name="members"></a><span data-ttu-id="9f3c7-110">Members</span><span class="sxs-lookup"><span data-stu-id="9f3c7-110">Members</span></span>

 <span data-ttu-id="9f3c7-111">**cProps**</span><span class="sxs-lookup"><span data-stu-id="9f3c7-111">**cProps**</span></span>
  
> <span data-ttu-id="9f3c7-112">Die Anzahl benannter Eigenschaften im Array im **aFormProp** -Element.</span><span class="sxs-lookup"><span data-stu-id="9f3c7-112">Count of named properties in the array in the **aFormProp** member.</span></span> 
    
 <span data-ttu-id="9f3c7-113">**ulPad**</span><span class="sxs-lookup"><span data-stu-id="9f3c7-113">**ulPad**</span></span>
  
>  <span data-ttu-id="9f3c7-114">Acht Byte Leerraum, die verwendet werden, um eine korrekte Ausrichtung zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="9f3c7-114">Eight bytes of padding used to guarantee correct alignment.</span></span> 
    
 <span data-ttu-id="9f3c7-115">**aFormProp**</span><span class="sxs-lookup"><span data-stu-id="9f3c7-115">**aFormProp**</span></span>
  
> <span data-ttu-id="9f3c7-116">Array von Formulareigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9f3c7-116">Array of form properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9f3c7-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f3c7-117">Remarks</span></span>

<span data-ttu-id="9f3c7-118">Die **SMAPIFormPropArray** -Struktur wird als Parameter an die folgenden Methoden übergeben:</span><span class="sxs-lookup"><span data-stu-id="9f3c7-118">The **SMAPIFormPropArray** structure is passed as a parameter to the following methods:</span></span> 
  
- [<span data-ttu-id="9f3c7-119">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="9f3c7-119">IMAPIFormInfo::CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md)
    
- [<span data-ttu-id="9f3c7-120">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="9f3c7-120">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="9f3c7-121">IMAPIFormContainer::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="9f3c7-121">IMAPIFormContainer::CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a><span data-ttu-id="9f3c7-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f3c7-122">See also</span></span>



[<span data-ttu-id="9f3c7-123">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="9f3c7-123">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md)
  
[<span data-ttu-id="9f3c7-124">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="9f3c7-124">SMAPIFormProp</span></span>](smapiformprop.md)


[<span data-ttu-id="9f3c7-125">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="9f3c7-125">MAPI Structures</span></span>](mapi-structures.md)

