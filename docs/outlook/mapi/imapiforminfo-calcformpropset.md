---
title: IMAPIFormInfoCalcFormPropSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.CalcFormPropSet
api_type:
- COM
ms.assetid: cc3ffb8d-9cc4-47d3-9aa9-02c3a5b7775c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7d0c044caf430c944d8912d050e4dbaba659c8b5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582497"
---
# <a name="imapiforminfocalcformpropset"></a><span data-ttu-id="c8ab5-103">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="c8ab5-103">IMAPIFormInfo::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="c8ab5-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8ab5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8ab5-105">Gibt einen Zeiger auf den vollständigen Satz von Eigenschaften, die einem Formular verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c8ab5-105">Returns a pointer to the complete set of properties that a form uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppFormPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="c8ab5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8ab5-106">Parameters</span></span>

 <span data-ttu-id="c8ab5-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c8ab5-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c8ab5-108">[in] Eine Bitmaske aus Flags, die den Typ des zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="c8ab5-108">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="c8ab5-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="c8ab5-109">The following flag can be set:</span></span>
    
<span data-ttu-id="c8ab5-110">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c8ab5-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c8ab5-111">Die zurückgegebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="c8ab5-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="c8ab5-112">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="c8ab5-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="c8ab5-113">_ppFormPropArray_</span><span class="sxs-lookup"><span data-stu-id="c8ab5-113">_ppFormPropArray_</span></span>
  
> <span data-ttu-id="c8ab5-114">[out] Ein Zeiger auf einen Zeiger auf das zurückgegebene [SMAPIFormPropArray](smapiformproparray.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c8ab5-114">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c8ab5-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="c8ab5-115">Return value</span></span>

<span data-ttu-id="c8ab5-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="c8ab5-116">S_OK</span></span> 
  
> <span data-ttu-id="c8ab5-117">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="c8ab5-117">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="c8ab5-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="c8ab5-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="c8ab5-119">Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="c8ab5-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="c8ab5-120">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="c8ab5-120">MFCMAPI reference</span></span>

<span data-ttu-id="c8ab5-121">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c8ab5-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c8ab5-122">**Datei**</span><span class="sxs-lookup"><span data-stu-id="c8ab5-122">**File**</span></span>|<span data-ttu-id="c8ab5-123">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="c8ab5-123">**Function**</span></span>|<span data-ttu-id="c8ab5-124">**Comment**</span><span class="sxs-lookup"><span data-stu-id="c8ab5-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c8ab5-125">MFCOutput.cpp</span><span class="sxs-lookup"><span data-stu-id="c8ab5-125">MFCOutput.cpp</span></span>  <br/> |<span data-ttu-id="c8ab5-126">_OutputFormInfo</span><span class="sxs-lookup"><span data-stu-id="c8ab5-126">_OutputFormInfo</span></span>  <br/> |<span data-ttu-id="c8ab5-127">MFCMAPI (engl.) verwendet die **IMAPIFormInfo::CalcFormPropSet** -Methode auf, wenn Debugausgabe für Formular Informationen-Objekte geschrieben.</span><span class="sxs-lookup"><span data-stu-id="c8ab5-127">MFCMAPI uses the **IMAPIFormInfo::CalcFormPropSet** method when writing debug output for form information objects.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c8ab5-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8ab5-128">See also</span></span>



[<span data-ttu-id="c8ab5-129">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="c8ab5-129">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="c8ab5-130">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c8ab5-130">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


[<span data-ttu-id="c8ab5-131">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="c8ab5-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

