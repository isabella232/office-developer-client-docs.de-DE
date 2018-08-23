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
ms.openlocfilehash: 9c6a6d210230fc305aef46371c22f67b3d445a81
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576582"
---
# <a name="imapiformcontainercalcformpropset"></a><span data-ttu-id="08708-103">IMAPIFormContainer::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="08708-103">IMAPIFormContainer::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="08708-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08708-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08708-105">Gibt ein Array der Eigenschaften verwendet, die für alle Formen in einem Formular Container installiert.</span><span class="sxs-lookup"><span data-stu-id="08708-105">Returns an array of the properties used by all forms installed in a form container.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="08708-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="08708-106">Parameters</span></span>

 <span data-ttu-id="08708-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="08708-107">_ulFlags_</span></span>
  
> <span data-ttu-id="08708-108">[in] Eine Bitmaske aus Flags, die steuert, wie das Array im Parameter _PpResults_ -Eigenschaft zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="08708-108">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="08708-109">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="08708-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="08708-110">FORMPROPSET_INTERSECTION</span><span class="sxs-lookup"><span data-stu-id="08708-110">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="08708-111">Das zurückgegebene Array enthält die Schnittmenge der Eigenschaften der Forms.</span><span class="sxs-lookup"><span data-stu-id="08708-111">The returned array contains the intersection of the forms' properties.</span></span>
    
<span data-ttu-id="08708-112">FORMPROPSET_UNION</span><span class="sxs-lookup"><span data-stu-id="08708-112">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="08708-113">Das zurückgegebene Array enthält die Vereinigung der Forms-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="08708-113">The returned array contains the union of the forms' properties.</span></span>
    
<span data-ttu-id="08708-114">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="08708-114">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="08708-115">Die Zeichenfolgen, die in das Array zurückgegeben werden im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="08708-115">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="08708-116">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="08708-116">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="08708-117">_ppResults_</span><span class="sxs-lookup"><span data-stu-id="08708-117">_ppResults_</span></span>
  
> <span data-ttu-id="08708-118">[out] Ein Zeiger auf einen Zeiger auf das zurückgegebene [SMAPIFormPropArray](smapiformproparray.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="08708-118">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure.</span></span> <span data-ttu-id="08708-119">Diese Struktur enthält alle Eigenschaften, die von den installierten Formularen verwendet.</span><span class="sxs-lookup"><span data-stu-id="08708-119">This structure contains all properties used by the installed forms.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="08708-120">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="08708-120">Return value</span></span>

<span data-ttu-id="08708-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="08708-121">S_OK</span></span> 
  
> <span data-ttu-id="08708-122">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="08708-122">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="08708-123">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="08708-123">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="08708-124">Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="08708-124">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="08708-125">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="08708-125">Remarks</span></span>

<span data-ttu-id="08708-126">Clientanwendungen rufen Sie die **IMAPIFormContainer::CalcFormPropSet** -Methode, um ein Array von Eigenschaften, die alle Formen in einem Formular Container installiert abzurufen.</span><span class="sxs-lookup"><span data-stu-id="08708-126">Client applications call the **IMAPIFormContainer::CalcFormPropSet** method to obtain an array of properties used by all forms installed in a form container.</span></span> <span data-ttu-id="08708-127">**IMAPIFormContainer::CalcFormPropSet** funktioniert wie die [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md) -Methode, außer dass sie für jedes Formular, das in einem bestimmten Container registriert ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="08708-127">**IMAPIFormContainer::CalcFormPropSet** works like the [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md) method, except that it operates on every form registered in a particular container.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="08708-128">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="08708-128">Notes to implementers</span></span>

<span data-ttu-id="08708-129">Formular Bibliothek Anbieter, die keine für Unicode-Zeichenfolgen Unterstützung sollte MAPI_E_BAD_CHARWIDTH zurückgegeben, wenn der Parameter MAPI_UNICODE übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="08708-129">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="08708-130">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="08708-130">Notes to callers</span></span>

 <span data-ttu-id="08708-131">**IMAPIFormContainer::CalcFormPropSet** akzeptiert, Schnittmenge oder eine Union-Sätzen für die Formulare-Eigenschaft, je nachdem das Flag in den _UlFlags_ -Parameter festgelegt, und es gibt eine **SMAPIFormPropArray** -Struktur, enthält die resultierende Gruppe von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="08708-131">**IMAPIFormContainer::CalcFormPropSet** takes either an intersection or a union of the forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
<span data-ttu-id="08708-132">Wenn ein Client die Option MAPI_UNICODE _UlFlags_übergibt, werden alle zurückgegebene Zeichenfolgen Unicode.</span><span class="sxs-lookup"><span data-stu-id="08708-132">If a client passes the MAPI_UNICODE flag in  _ulFlags_, all returned strings are Unicode.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="08708-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08708-133">See also</span></span>



[<span data-ttu-id="08708-134">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="08708-134">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
  
[<span data-ttu-id="08708-135">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="08708-135">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="08708-136">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="08708-136">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)

