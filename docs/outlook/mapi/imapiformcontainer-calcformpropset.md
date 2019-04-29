---
title: IMAPIFormContainerCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.CalcFormPropSet
api_type:
- COM
ms.assetid: 594e3aac-a00f-422e-8e7a-949e4c9a3f8d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ec1933f80f211c7c381f9de6b15d414932b9a78e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414914"
---
# <a name="imapiformcontainercalcformpropset"></a><span data-ttu-id="eabda-103">IMAPIFormContainer::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="eabda-103">IMAPIFormContainer::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="eabda-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eabda-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eabda-105">Gibt ein Array der Eigenschaften zurück, die von allen in einem Formular Container installierten Formularen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eabda-105">Returns an array of the properties used by all forms installed in a form container.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="eabda-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eabda-106">Parameters</span></span>

 <span data-ttu-id="eabda-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="eabda-107">_ulFlags_</span></span>
  
> <span data-ttu-id="eabda-108">in Eine Bitmaske von Flags, die steuert, wie das Eigenschaftenarray im _ppResults_ -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="eabda-108">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="eabda-109">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="eabda-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="eabda-110">FORMPROPSET_INTERSECTION</span><span class="sxs-lookup"><span data-stu-id="eabda-110">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="eabda-111">Das zurückgegebene Array enthält den Schnittpunkt der Eigenschaften der Formulare.</span><span class="sxs-lookup"><span data-stu-id="eabda-111">The returned array contains the intersection of the forms' properties.</span></span>
    
<span data-ttu-id="eabda-112">FORMPROPSET_UNION</span><span class="sxs-lookup"><span data-stu-id="eabda-112">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="eabda-113">Das zurückgegebene Array enthält die Vereinigung der Eigenschaften der Formulare.</span><span class="sxs-lookup"><span data-stu-id="eabda-113">The returned array contains the union of the forms' properties.</span></span>
    
<span data-ttu-id="eabda-114">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="eabda-114">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="eabda-115">Die im Array zurückgegebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="eabda-115">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="eabda-116">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="eabda-116">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="eabda-117">_ppResults_</span><span class="sxs-lookup"><span data-stu-id="eabda-117">_ppResults_</span></span>
  
> <span data-ttu-id="eabda-118">Out Ein Zeiger auf einen Zeiger auf die zurückgegebene [SMAPIFormPropArray](smapiformproparray.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="eabda-118">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure.</span></span> <span data-ttu-id="eabda-119">Diese Struktur enthält alle Eigenschaften, die von den installierten Formularen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eabda-119">This structure contains all properties used by the installed forms.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="eabda-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eabda-120">Return value</span></span>

<span data-ttu-id="eabda-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="eabda-121">S_OK</span></span> 
  
> <span data-ttu-id="eabda-122">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="eabda-122">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="eabda-123">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="eabda-123">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="eabda-124">Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="eabda-124">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eabda-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eabda-125">Remarks</span></span>

<span data-ttu-id="eabda-126">Client Anwendungen rufen die **IMAPIFormContainer:: CalcFormPropSet** -Methode auf, um ein Array von Eigenschaften abzurufen, die von allen in einem Formular Container installierten Formularen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eabda-126">Client applications call the **IMAPIFormContainer::CalcFormPropSet** method to obtain an array of properties used by all forms installed in a form container.</span></span> <span data-ttu-id="eabda-127">**IMAPIFormContainer:: CalcFormPropSet** funktioniert wie die [IMAPIFormMgr:: CalcFormPropSet](imapiformmgr-calcformpropset.md) -Methode, mit der Ausnahme, dass Sie auf jedem in einem bestimmten Container registrierten Formular ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eabda-127">**IMAPIFormContainer::CalcFormPropSet** works like the [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md) method, except that it operates on every form registered in a particular container.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="eabda-128">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="eabda-128">Notes to implementers</span></span>

<span data-ttu-id="eabda-129">Formularbibliothek Anbieter, die Unicode-Zeichenfolgen nicht unterstützen, sollten MAPI_E_BAD_CHARWIDTH zurückgeben, wenn MAPI_UNICODE übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="eabda-129">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="eabda-130">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="eabda-130">Notes to callers</span></span>

 <span data-ttu-id="eabda-131">**IMAPIFormContainer:: CalcFormPropSet** nimmt entweder eine Schnittmenge oder eine Vereinigung der Eigenschaftensätze der Formulare an, je nach dem im _ulFlags_ -Parameter festgelegten Flag und gibt eine **SMAPIFormPropArray** -Struktur zurück, die die die resultierende Gruppe von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="eabda-131">**IMAPIFormContainer::CalcFormPropSet** takes either an intersection or a union of the forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
<span data-ttu-id="eabda-132">Wenn ein Client das MAPI_UNICODE-Flag in _ulFlags_übergibt, sind alle zurückgegebenen Zeichenfolgen Unicode.</span><span class="sxs-lookup"><span data-stu-id="eabda-132">If a client passes the MAPI_UNICODE flag in  _ulFlags_, all returned strings are Unicode.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="eabda-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eabda-133">See also</span></span>



[<span data-ttu-id="eabda-134">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="eabda-134">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
  
[<span data-ttu-id="eabda-135">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="eabda-135">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="eabda-136">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eabda-136">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)

