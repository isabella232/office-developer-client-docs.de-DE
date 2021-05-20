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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bf072aba27c90b7cea80c464e17fafb47524b695
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436426"
---
# <a name="imapiformmgrcalcformpropset"></a><span data-ttu-id="6c36d-103">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="6c36d-103">IMAPIFormMgr::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="6c36d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c36d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c36d-105">Gibt ein Array der Eigenschaften zurück, die von einer Gruppe von Formularen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c36d-105">Returns an array of the properties that a group of forms uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="6c36d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c36d-106">Parameters</span></span>

 <span data-ttu-id="6c36d-107">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="6c36d-107">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="6c36d-108">[in] Ein Zeiger auf ein Array von Formularinformationsobjekten, die die Formulare identifizieren, für die Eigenschaften zurückgeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6c36d-108">[in] A pointer to an array of form information objects that identify the forms for which to return properties.</span></span>
    
 <span data-ttu-id="6c36d-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6c36d-109">_ulFlags_</span></span>
  
> <span data-ttu-id="6c36d-110">[in] Eine Bitmaske mit Flags, die steuert, wie das Eigenschaftenarray im  _ppResults-Parameter_ zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6c36d-110">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="6c36d-111">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="6c36d-111">The following flags can be set:</span></span> 
    
<span data-ttu-id="6c36d-112">FORMPROPSET_INTERSECTION</span><span class="sxs-lookup"><span data-stu-id="6c36d-112">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="6c36d-113">Das zurückgegebene Array enthält die Schnittmenge der Eigenschaften des Formulars.</span><span class="sxs-lookup"><span data-stu-id="6c36d-113">The returned array contains the intersection of the form's properties.</span></span>
    
<span data-ttu-id="6c36d-114">FORMPROPSET_UNION</span><span class="sxs-lookup"><span data-stu-id="6c36d-114">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="6c36d-115">Das zurückgegebene Array enthält die Vereinigung der Eigenschaften des Formulars.</span><span class="sxs-lookup"><span data-stu-id="6c36d-115">The returned array contains the union of the form's properties.</span></span>
    
<span data-ttu-id="6c36d-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6c36d-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6c36d-117">Die im Array zurückgegebenen Zeichenfolgen haben das Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="6c36d-117">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="6c36d-118">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="6c36d-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="6c36d-119">_ppResults_</span><span class="sxs-lookup"><span data-stu-id="6c36d-119">_ppResults_</span></span>
  
> <span data-ttu-id="6c36d-120">[out] Ein Zeiger auf einen Zeiger auf die zurückgegebene [SMAPIFormPropArray-Struktur,](smapiformproparray.md) die die von den Formularen verwendeten Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="6c36d-120">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure, which contains the properties that the forms use.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6c36d-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c36d-121">Return value</span></span>

<span data-ttu-id="6c36d-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="6c36d-122">S_OK</span></span> 
  
> <span data-ttu-id="6c36d-123">Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c36d-123">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="6c36d-124">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="6c36d-124">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="6c36d-125">Entweder wurde MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="6c36d-125">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6c36d-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6c36d-126">Remarks</span></span>

<span data-ttu-id="6c36d-127">Formularbetrachter rufen die **IMAPIFormMgr::CalcFormPropSet-Methode** auf, um ein Array der Eigenschaften zu erhalten, die von einer Gruppe von Formularen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c36d-127">Form viewers call the **IMAPIFormMgr::CalcFormPropSet** method to obtain an array of the properties that a group of forms uses.</span></span> <span data-ttu-id="6c36d-128">**CalcFormPropSet** verwendet je nach dem im  _ulFlags-Parameter_ festgelegten Kennzeichen eine Schnittmenge oder eine Vereinigung der Eigenschaftensätze dieser Formulare und gibt eine **SMAPIFormPropArray-Struktur** zurück, die die resultierende Gruppe von Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="6c36d-128">**CalcFormPropSet** takes either an intersection or a union of these forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6c36d-129">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="6c36d-129">Notes to implementers</span></span>

<span data-ttu-id="6c36d-130">Wenn ein Formularanzeiger das MAPI_UNICODE im  _ulFlags-Parameter_ übergibt, sollten alle Zeichenfolgen als Unicode-Zeichenfolgen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6c36d-130">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings should be returned as Unicode strings.</span></span> <span data-ttu-id="6c36d-131">Formularbibliotheksanbieter, die keine Unicode-Zeichenfolgen unterstützen, sollten MAPI_E_BAD_CHARWIDTH zurückgeben, MAPI_UNICODE übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="6c36d-131">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6c36d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c36d-132">See also</span></span>



[<span data-ttu-id="6c36d-133">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="6c36d-133">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="6c36d-134">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6c36d-134">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

