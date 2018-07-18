---
title: IMAPIFormMgrCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.CalcFormPropSet
api_type:
- COM
ms.assetid: ab302bfd-5cff-49b4-b0d2-308ae5af478d
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: abd2a3e2a1a810f902ad977413c89f2e8b0113a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792162"
---
# <a name="imapiformmgrcalcformpropset"></a><span data-ttu-id="80710-103">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="80710-103">IMAPIFormMgr::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="80710-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="80710-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="80710-105">Gibt ein Array von Eigenschaften, die eine Gruppe von Formularen verwendet.</span><span class="sxs-lookup"><span data-stu-id="80710-105">Returns an array of the properties that a group of forms uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="80710-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="80710-106">Parameters</span></span>

 <span data-ttu-id="80710-107">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="80710-107">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="80710-108">[in] Ein Zeiger auf ein Array von Formular Informationen-Objekten, mit denen die Formulare für die Eigenschaften zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="80710-108">[in] A pointer to an array of form information objects that identify the forms for which to return properties.</span></span>
    
 <span data-ttu-id="80710-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="80710-109">_ulFlags_</span></span>
  
> <span data-ttu-id="80710-110">[in] Eine Bitmaske aus Flags, die steuert, wie das Array im Parameter _PpResults_ -Eigenschaft zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="80710-110">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="80710-111">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="80710-111">The following flags can be set:</span></span> 
    
<span data-ttu-id="80710-112">FORMPROPSET_INTERSECTION</span><span class="sxs-lookup"><span data-stu-id="80710-112">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="80710-113">Das zurückgegebene Array enthält die Schnittmenge der Eigenschaften des Formulars.</span><span class="sxs-lookup"><span data-stu-id="80710-113">The returned array contains the intersection of the form's properties.</span></span>
    
<span data-ttu-id="80710-114">FORMPROPSET_UNION</span><span class="sxs-lookup"><span data-stu-id="80710-114">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="80710-115">Das zurückgegebene Array enthält die Union der Eigenschaften des Formulars.</span><span class="sxs-lookup"><span data-stu-id="80710-115">The returned array contains the union of the form's properties.</span></span>
    
<span data-ttu-id="80710-116">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="80710-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="80710-117">Die Zeichenfolgen, die in das Array zurückgegeben werden im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="80710-117">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="80710-118">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="80710-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="80710-119">_ppResults_</span><span class="sxs-lookup"><span data-stu-id="80710-119">_ppResults_</span></span>
  
> <span data-ttu-id="80710-120">[out] Ein Zeiger auf einen Zeiger auf das zurückgegebene [SMAPIFormPropArray](smapiformproparray.md) -Struktur, die Eigenschaften enthält, die die Formularen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="80710-120">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure, which contains the properties that the forms use.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="80710-121">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="80710-121">Return value</span></span>

<span data-ttu-id="80710-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="80710-122">S_OK</span></span> 
  
> <span data-ttu-id="80710-123">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="80710-123">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="80710-124">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="80710-124">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="80710-125">Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="80710-125">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="80710-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="80710-126">Remarks</span></span>

<span data-ttu-id="80710-127">Formular Viewer rufen Sie die **IMAPIFormMgr::CalcFormPropSet** -Methode, um ein Array der Eigenschaften abzurufen, die eine Gruppe von Formularen verwendet.</span><span class="sxs-lookup"><span data-stu-id="80710-127">Form viewers call the **IMAPIFormMgr::CalcFormPropSet** method to obtain an array of the properties that a group of forms uses.</span></span> <span data-ttu-id="80710-128">**CalcFormPropSet** übernimmt entweder eine Schnittmenge oder Kombination dieser Formulare-Eigenschaft festgelegt, je nachdem das Flag festlegen in der _UlFlags_ -Parameter, und es gibt eine **SMAPIFormPropArray** -Struktur, die resultierende Gruppe von enthält Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="80710-128">**CalcFormPropSet** takes either an intersection or a union of these forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="80710-129">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="80710-129">Notes to implementers</span></span>

<span data-ttu-id="80710-130">Wenn ein Formular Viewer die Option MAPI_UNICODE im Parameter _UlFlags_ übergibt, sollten alle Zeichenfolgen als Unicode-Zeichenfolgen zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="80710-130">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings should be returned as Unicode strings.</span></span> <span data-ttu-id="80710-131">Formular Bibliothek Anbieter, die keine für Unicode-Zeichenfolgen Unterstützung sollte MAPI_E_BAD_CHARWIDTH zurückgegeben, wenn der Parameter MAPI_UNICODE übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="80710-131">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="80710-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80710-132">See also</span></span>



[<span data-ttu-id="80710-133">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="80710-133">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="80710-134">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="80710-134">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

