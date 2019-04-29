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
# <a name="imapiformmgrcalcformpropset"></a><span data-ttu-id="ef33d-103">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="ef33d-103">IMAPIFormMgr::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="ef33d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef33d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ef33d-105">Gibt ein Array der Eigenschaften zurück, die eine Gruppe von Formularen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ef33d-105">Returns an array of the properties that a group of forms uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="ef33d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef33d-106">Parameters</span></span>

 <span data-ttu-id="ef33d-107">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="ef33d-107">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="ef33d-108">in Ein Zeiger auf ein Array von Formular Informationsobjekten, die die Formulare identifizieren, für die Eigenschaften zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ef33d-108">[in] A pointer to an array of form information objects that identify the forms for which to return properties.</span></span>
    
 <span data-ttu-id="ef33d-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ef33d-109">_ulFlags_</span></span>
  
> <span data-ttu-id="ef33d-110">in Eine Bitmaske von Flags, die steuert, wie das Eigenschaftenarray im _ppResults_ -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ef33d-110">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="ef33d-111">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="ef33d-111">The following flags can be set:</span></span> 
    
<span data-ttu-id="ef33d-112">FORMPROPSET_INTERSECTION</span><span class="sxs-lookup"><span data-stu-id="ef33d-112">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="ef33d-113">Das zurückgegebene Array enthält den Schnittpunkt der Eigenschaften des Formulars.</span><span class="sxs-lookup"><span data-stu-id="ef33d-113">The returned array contains the intersection of the form's properties.</span></span>
    
<span data-ttu-id="ef33d-114">FORMPROPSET_UNION</span><span class="sxs-lookup"><span data-stu-id="ef33d-114">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="ef33d-115">Das zurückgegebene Array enthält die Vereinigung der Eigenschaften des Formulars.</span><span class="sxs-lookup"><span data-stu-id="ef33d-115">The returned array contains the union of the form's properties.</span></span>
    
<span data-ttu-id="ef33d-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ef33d-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ef33d-117">Die im Array zurückgegebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="ef33d-117">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="ef33d-118">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="ef33d-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="ef33d-119">_ppResults_</span><span class="sxs-lookup"><span data-stu-id="ef33d-119">_ppResults_</span></span>
  
> <span data-ttu-id="ef33d-120">Out Ein Zeiger auf einen Zeiger auf die zurückgegebene [SMAPIFormPropArray](smapiformproparray.md) -Struktur, die die Eigenschaften enthält, die von den Formularen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef33d-120">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure, which contains the properties that the forms use.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ef33d-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef33d-121">Return value</span></span>

<span data-ttu-id="ef33d-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="ef33d-122">S_OK</span></span> 
  
> <span data-ttu-id="ef33d-123">Der Aufruf war erfolgreich, und der erwartete Wert oder die Werte wurden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ef33d-123">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="ef33d-124">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="ef33d-124">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="ef33d-125">Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="ef33d-125">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ef33d-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef33d-126">Remarks</span></span>

<span data-ttu-id="ef33d-127">Formular Betrachter rufen die **IMAPIFormMgr:: CalcFormPropSet** -Methode auf, um ein Array der Eigenschaften abzurufen, die eine Gruppe von Formularen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ef33d-127">Form viewers call the **IMAPIFormMgr::CalcFormPropSet** method to obtain an array of the properties that a group of forms uses.</span></span> <span data-ttu-id="ef33d-128">**CalcFormPropSet** nimmt entweder einen Schnittpunkt oder eine Vereinigung dieser Formulareigenschaften Sätze an, je nach dem im _ulFlags_ -Parameter festgelegten Flag und gibt eine **SMAPIFormPropArray** -Struktur zurück, die die resultierende Gruppe von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ef33d-128">**CalcFormPropSet** takes either an intersection or a union of these forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ef33d-129">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="ef33d-129">Notes to implementers</span></span>

<span data-ttu-id="ef33d-130">Wenn ein Formular Betrachter das MAPI_UNICODE-Flag im _ulFlags_ -Parameter übergibt, sollten alle Zeichenfolgen als Unicode-Zeichenfolgen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ef33d-130">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings should be returned as Unicode strings.</span></span> <span data-ttu-id="ef33d-131">Formularbibliothek Anbieter, die Unicode-Zeichenfolgen nicht unterstützen, sollten MAPI_E_BAD_CHARWIDTH zurückgeben, wenn MAPI_UNICODE übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="ef33d-131">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ef33d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef33d-132">See also</span></span>



[<span data-ttu-id="ef33d-133">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="ef33d-133">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="ef33d-134">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ef33d-134">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

